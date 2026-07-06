function EnneractSantaRuntimeLoop_v1_1():

    PNG_SEQUENCE = [
        "enneract_santa_projection_front.png",
        "enneract_santa_projection_side.png",
        "enneract_santa_projection_dimensional.png",
        "enneract_santa_projection_runtime.png"
    ]

    for idx, V in enumerate(PNG_SEQUENCE):

        // 0. Drift Dampening Layer (DDL)
        tau_ND_raw = MeasureNarrativeDriftTension(V)
        tau_ND     = ApplyDriftDampening(tau_ND_raw)      // tau_ND = tau_ND_raw - 0.01

        // 1. Generate visual
        GeneratePNG(V)

        // 2. Curvature + gates (with decoupler + tightened deep-gate)
        kappa_raw = MeasureCurvature(E9, V)
        kappa     = ApplyCurvatureDriftDecoupler(kappa_raw, tau_ND)  // kappa_decoupled = kappa_raw - 0.5 * tau_ND

        gates     = MeasureGatingScalars(V)   // {g_S, g_SS, g_D}
        gates     = ApplyDeepGateTightening(gates)  // enforce |g_D - 1| <= 0.015 PASS, <= 0.03 WARN

        // 3. Structural Integrity Check (Check 1)
        check1 = StructuralIntegrityCheck_v1_1(kappa, gates)

        // 4. Narrative Stability Check (Check 2)
        check2 = NarrativeStabilityCheck_v1_1(tau_ND)

        // 5. Evaluate checks (Decision)
        status = EvaluateChecks_v1_1(check1, check2, tau_ND, kappa, gates)

        LogEvent(V, tau_ND_raw, tau_ND, kappa_raw, kappa, gates, check1, check2, status)

        // 6. Dimensional–Runtime Micro-Check (DRMC) + Exec Pre-Binding
        if V == "enneract_santa_projection_dimensional.png":
            status_drmc = DimensionalRuntimeMicroCheck_v1_1()
            LogEvent("DRMC", tau_ND, kappa, gates, status_drmc)

            if status_drmc == "FAIL":
                HaltPipeline("DRMC failure before runtime projection")
                return

            Exec_pre = ExecPlanePreBinding_v1_1()   // Exec_A ⊗ Exec_B ⊗ Exec_H
            LogEvent("ExecPreBinding", Exec_pre)

        // 7. Status handling
        if status == "FAIL":
            CorrectDriftAndStructure_v1_1(V)

            // re-measure with v1.1 layers
            tau_ND_raw = MeasureNarrativeDriftTension(V)
            tau_ND     = ApplyDriftDampening(tau_ND_raw)

            kappa_raw  = MeasureCurvature(E9, V)
            kappa      = ApplyCurvatureDriftDecoupler(kappa_raw, tau_ND)

            gates      = MeasureGatingScalars(V)
            gates      = ApplyDeepGateTightening(gates)

            check1     = StructuralIntegrityCheck_v1_1(kappa, gates)
            check2     = NarrativeStabilityCheck_v1_1(tau_ND)

            status     = EvaluateChecks_v1_1(check1, check2, tau_ND, kappa, gates)
            LogEvent(V, tau_ND_raw, tau_ND, kappa_raw, kappa, gates, check1, check2, status)

            if status != "PASS":
                HaltPipeline("Enneract Santa runtime loop v1.1 blocked at " + V)
                return

        else if status == "WARN":
            // optional recheck without correction
            tau_ND_raw2 = MeasureNarrativeDriftTension(V)
            tau_ND2     = ApplyDriftDampening(tau_ND_raw2)

            kappa_raw2  = MeasureCurvature(E9, V)
            kappa2      = ApplyCurvatureDriftDecoupler(kappa_raw2, tau_ND2)

            gates2      = MeasureGatingScalars(V)
            gates2      = ApplyDeepGateTightening(gates2)

            check1b     = StructuralIntegrityCheck_v1_1(kappa2, gates2)
            check2b     = NarrativeStabilityCheck_v1_1(tau_ND2)

            status2     = EvaluateChecks_v1_1(check1b, check2b, tau_ND2, kappa2, gates2)
            LogEvent(V, tau_ND_raw2, tau_ND2, kappa_raw2, kappa2, gates2, check1b, check2b, status2)

            if status2 == "FAIL":
                HaltPipeline("Warn escalated to fail at " + V + " (v1.1)")
                return

    // If we reach here, all 4 PNGs are approved under v1.1
    ActivateExecPlanes(S9)   // Exec_A ⊗ Exec_B ⊗ Exec_H (final activation)
    LogEvent("RuntimeActivation_v1_1", "OK")


function StructuralIntegrityCheck(kappa, gates):

    // Curvature check
    if abs(kappa) > 0.05:
        return "FAIL"
    if abs(kappa) > 0.02:
        return "WARN"

    // Gating scalar check
    for g in gates:   // g ∈ {g_S, g_SS, g_D}
        if abs(g - 1) > 0.05:
            return "FAIL"
        if abs(g - 1) > 0.02:
            return "WARN"

    return "PASS"

function NarrativeStabilityCheck(tau_ND):

    if tau_ND >= 0.10:
        return "FAIL"

    if tau_ND >= 0.05:
        return "WARN"

    return "PASS"

function ExecPlanePreBinding_v1_1():
    Exec_A = LoadExecPlane("A")
    Exec_B = LoadExecPlane("B")
    Exec_H = LoadExecPlane("H")

    return Exec_A ⊗ Exec_B ⊗ Exec_H

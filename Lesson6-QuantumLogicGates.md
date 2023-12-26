# Lesson 6
## Quantum Logic Gates Introduction
- Quantum Gates manipulate the value of the qubit the gate is applied to. 
    - A quantum gate is a $2^{N} x 2^{N}$, where N represents the number of qubits the gate is acting on. To get the resulting state of the qubit applying the gate, you mutliply the quantum gates matrix by the state vector of the qubit. The example below shows a one qubit gate being applied:
        - $\begin{bmatrix} * && * \\ * && * \end{bmatrix}\begin{bmatrix} a\\b \end{bmatrix} = \begin{bmatrix} a*\\b* \end{bmatrix}$
    - Two Qubit Gate:
        - $\begin{bmatrix} * && * && * && * \\* && * && * && * \\* && * && * && * \\* && * && * && * \\ \end{bmatrix}\begin{bmatrix} a\\b\\c\\d \end{bmatrix} = \begin{bmatrix} a*\\b*\\c*\\d* \end{bmatrix}$
    - Matrices used to describe quantum logic gates are unitary
        - A unitary matrix, is a square matrix $U$ such that $U^{\dagger}U = UU^{\dagger} = I$ (where $U^{\dagger}$ is the conjugate transpose of $U$ and $I$ is the identity matrix)
        - Preserves magnitude when multiplied by state vector. This is essential because the magnitude of the qubit's state vector should be 1(meaning the sum of all the probabilities equals 1)
            - Thus, $||U\ket{\psi}|| = ||\ket{\psi}||$
        - Quantum logic gates are reversible. You can apply an inverse operation to the qubit to find what it was before the initial gate was applied. This cannot be done with classical logic gates
## Pauli Gates
- Quantum Logic gates that operate on a single qubit
     - Pauli X Gate
        - Quantum equivalent of NOT gate for classical computers
        - Single qubit that swaps $\ket{0}$ to $\ket{1} and vice versa$
            - $X = \begin{bmatrix} 0 && 1 \\ 1 && 0 \end{bmatrix}$
            -  So, $X\ket{0} =  \begin{bmatrix} 0 && 1 \\ 1 && 0 \end{bmatrix}\begin{bmatrix} 1\\0 \end{bmatrix} = \begin{bmatrix} 1(0) + 0(1)\\(1)1 + 0(0) \end{bmatrix} = \begin{bmatrix} 0\\1 \end{bmatrix} $
            - In general, if we have $\ket{\psi} = \alpha\ket{0} + \beta\ket{1}$
                - $X\ket{\psi} =  \begin{bmatrix} 0 && 1 \\ 1 && 0 \end{bmatrix}\begin{bmatrix} \alpha\\\beta \end{bmatrix} = \begin{bmatrix} \beta\\\alpha \end{bmatrix} \equiv \alpha\ket{1} + \beta\ket{0}$
        - X gate is it's own inverse
    - Pauli Y Gate
        - Rotation of around $\pi$ degrees around the y-axis
        - $Y = \begin{bmatrix} 0 && -i \\ i && 0 \end{bmatrix}$
        - So, $Y\ket{0} = \begin{bmatrix} 0 && -i \\ i && 0 \end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix} = \begin{bmatrix}0\\i\end{bmatrix} = i\begin{bmatrix}0\\\end{bmatrix} = i\ket{1}$
            - i is the global phase in this situation
            - Also, $P(Y\ket{0} = \ket{0})  = |0|^{2} = 0$
            - And $P(Y\ket{0} = \ket{1})  = |i|^{2} = 1$
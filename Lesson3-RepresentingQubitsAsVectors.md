# Lesson 3
## Dirac Notation(Bra Ket Notation)
- Qubits have two computational basis states which are $\ket{0}$ and $\ket{1}$, which is represented in Dirac Notation as kets.
    - Our two computational base our mutually exclusive and can be written as two dimensional colum vectors and form an orthonormal basis because they are unit vectors and they are orthogonal to each other. 
    $`
    \ket{0} =
    \begin{bmatrix} 
    1\\
    0\\
    \end{bmatrix}
    `$
    $`
    \ket{1} =
    \begin{bmatrix} 
    0\\
    1\\
    \end{bmatrix}
    `$
    - The notation that was used to write these states are Dirac Notation(aka Bra Ket Notation), which is used to describe quantum states
    - The symbol, $`\ket{*}`$, is a ket which denotes a column vector
    - The symbol $`\bra{*}`$, is a bra which denotes a row vector
- Superimposed quantum states can be represented as a linear combination of these two basis states
    - $`\ket{\psi}`$ represents a random quantum state in general
    - So, $`\ket{\psi} = \alpha\ket{0} + \beta\ket{1} = 
    \begin{bmatrix} 
    \alpha\\
    \beta\\
    \end{bmatrix}
    `$, where $`\alpha`$ and $`\beta`$ are complex numbers. If $`\alpha`$ and $`\beta`$ are nonzero that the quantum state is in superposition
- $`\alpha`$ and $`\beta`$ are also probability amplitudes where:
    - $`|\alpha|^{2} = `$ Probability that the measurement outcome is $`\ket{0}`$
    - $`|\beta|^{2} = `$ Probability that the measurement outcome is $`\ket{1}`$
    - Additionally, $`|\alpha|^{2}+|\beta|^{2} = 1`$, which is known as the normalization constraint
    - So, if we have $`\ket{\psi} = \begin{bmatrix}
    0\\
    1
    \end{bmatrix}`$
        - $`P(\ket{\psi} = \ket{0}) = |0|^{2} = 0`$
        - $`P(\ket{\psi} = \ket{1}) = |1|^{2} = 1`$
- The symbol $`\bra{\psi}`$, is a bra which denotes a row vector that is the conjugate transpose of $`\ket{\psi}`$
    - Where, $`\ket{\psi} = \begin{bmatrix}\alpha\\\beta\end{bmatrix}`$ 
    - Thus, $`\bra{\psi} = \ket{\psi}^{\dagger} = \begin{bmatrix} \alpha^{*} && \beta^{*} \end{bmatrix}`$
- Multiplying a bra and ket is the same as doing the inner product of both vectors
     - So, $`\bra{0}\ket{0} = \begin{bmatrix} 1 && 0 \end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix} = 1`$
     - Also, $`\bra{\psi}\ket{\psi}`$, can be written as $`\braket{\psi|\psi}`$
- Also something to note:
    - $`\braket{0|\psi} = \begin{bmatrix} 1 && 0 \end{bmatrix}\begin{bmatrix}\alpha\\\beta\end{bmatrix} = \alpha`$
        - So, $`P(\ket{\psi} = \ket{0}) = |\alpha|^{2} = |\braket{0|\psi}|^{2}`$
    - $`\braket{1|\psi} = \begin{bmatrix} 0 && 1 \end{bmatrix}\begin{bmatrix}\alpha\\\beta\end{bmatrix} = \beta`$
        - So, $`P(\ket{\psi} = \ket{1}) = |\beta|^{2} = |\braket{1|\psi}|^{2}`$
## Representing Qubits on Bloch Sphere
- When using complex numbers, we represent qubit states with the Bloch Sphere( which has three dimensions) and polar coordinates
    - Similar to spherical coordinates in calculus II, we plot quantum states using three variables which are the magnitude of the vector, $`\theta`$, and $`\phi`$(azimuth angle)
        - the magnitude of the vector can be equal or less than 1. The Bloch sphere is like a 3D unit circle
    - To convert the quantum state to  $`\ket{\psi} = \alpha\ket{0} + \beta\ket{1}`$ form we just use the formula:
        - $`\ket{\psi} = \cos(\frac{\theta}{2})\ket{0} + e^{i\phi}\sin(\frac{\theta}{2})\ket{1}`$
        - Using this we can use convert $`\alpha`$ and $`\beta`$ into $`e^{i\theta} = \cos(\theta) + i\sin(\theta)`$ to make $`\alpha`$ and $`\beta`$ into a+bi form. Then you can solve for the probabilities of certain values
    - Example: $`\phi = \frac{3\pi}{8}`$ and $`\theta = \frac{\pi}{4}`$
        - $`\ket{\psi} = \cos(\frac{\pi}{8})\ket{0} + e^{\frac{3i\pi}{8}}\sin(\frac{\pi}{8})\ket{1}`$
             - Converting $`\alpha`$ to a+bi form, since $`\alpha`$ does not have imaginary componenet, assuming that $`\theta`$ is 0.
                -  $`\cos(\frac{\pi}{8})(e^{i(0)} = \cos(0) + i\sin(0)) \equiv \cos(\frac{\pi}{8}) = \cos(\frac{\pi}{8}) + 0i`$
                    - So, $`\alpha = 0.92 + 0i`$
            - Converting $`\beta`$ to a + bi form
                - $`\sin(\frac{\pi}{8})(e^{(\frac{3i\pi}{8})} = \cos(\frac{3\pi}{8}) + i\sin(\frac{3\pi}{8})) \equiv \sin(\frac{\pi}{8})e^{(\frac{3i\pi}{8})} = \sin(\frac{\pi}{8})\cos(\frac{3\pi}{8}) + i(\sin(\frac{\pi}{8})\sin(\frac{3\pi}{8}))`$
                - $`\sin(\frac{\pi}{8})e^{(\frac{3i\pi}{8})} = 0.15 + 0.35i`$
                - So $`\beta = 0.15 + 0.35i`$
        - $`\ket{\psi} = (0.92)\ket{0} + (0.15 + 0.35i)\ket{1}`$
        - Calculating the probability of $`\alpha`$ or $`\beta`$ being measured
             - Calculating $`\alpha`$:
                - $`P(\ket{\psi} = \ket{0}) = |\alpha|^{2} = |0.92|^{2} \approx 0.85 `$
            - Since P($`\alpha`$ being measured) + P($`\beta`$ being measured) = 1 because of the normalization constraint, P($`\beta`$ being measured) = 1- P($`\alpha`$ being measured) is true
                - Thus, $`P(\ket{\psi} = \ket{1}) = 1 - P(\ket{\psi} = \ket{0}) = 1 - 0.85 = 0.15`$
        - There is an 85% chance that $\alpha$ and 15% chance that $\beta$ is measured
### Pure and Mixed States
-Pure state is when the qubit can be represented as a linera combination
-Mixed states require them to represented throug a density matrix
### Global Phase and Relative Phase
- Global Phase is a complex number with a magnitude of 1, cannot be physically observed and connect effect quantum computations
- Relative Phase is the difference between the phase vectors of the two probabilites amplitudes, that effects quantum computations when measuring a qubit, can be physically observed

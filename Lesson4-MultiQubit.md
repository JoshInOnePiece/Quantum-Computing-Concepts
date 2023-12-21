# Lesson 4
## Computational States for Multiple qubits
- The number of computational vector states is $2^{N}$. Where N represents the number of qubits. So, there are four computational basis states for two qubits. These are shown below:
    - --
    - $\ket{00} = \begin{bmatrix}1 \\ 0 \\ 0 \\ 0 \end{bmatrix}$
    - --
    - $\ket{01} = \begin{bmatrix}0 \\ 1 \\ 0 \\ 0 \end{bmatrix}$
    - --
    - $\ket{10} = \begin{bmatrix}0 \\ 0 \\ 1 \\ 0 \end{bmatrix}$
    - --
    - $\ket{11} = \begin{bmatrix}0 \\ 0 \\ 0 \\ 1 \end{bmatrix}$
    - --
- This can be expanded to three qubits which have 8 computational states that follow the same patter. Best way to think about it is like a decoder. The total number of inputs are the amount of qubits, the possible combinations of those inputs are the possible basis states, and the output from that input is the corresponding vector. If you're still confused search 3-to-8 decoder and hopefully that helps.
- Representing multiple qubits in superposition is similar to doing it with just one qubit. It is a linear combination of all the possible states. For example, for two qubits the superposition would be:
    - $\ket{\psi} = a\ket{00} + b\ket{01} + c\ket{10} + d\ket{11} = \begin{bmatrix} a\\b\\c\\d\end{bmatrix}$
- Uniform superposition: every possible outcome has an equal probability when you measure the set of qubits
# How much information can qubits hold
- With all the superposition states that qubits can take up, they can represent a variety of different values during processing. But this is only for processing, since when you measure the data the qubit collapses to a 0 or 1. Thus, in processing there is a lot more you can do with qubits, but for extraction it is exactly the same as a classical computer

# Lesson 1
## Classical v.s Quantum Computers
- For certain types of problems such as large scale permutations, classical computers require an exponential number of resources and work in order to solve a problem. Quantum computers are able to solve these problems more efficiently by evaluating them more efficiently. 
    - An example, would be evaluating seating arrangements for a dinner party. This is a permutation problem where the number of seating arrangements is (# of people)!, the more people the more possibilities you have to evaluate
        - Classical Computer require to look at each permutation one at a time, which would take an exponential amount of time and work to evaluate
        - Qubits superposition will allow for the quantum computer to simulataneously represent all possible outcomes allowing for it to be evaluated faster
- Quantum Computers will not replace Classical Computers. The goal of quantum computer is to solve problems complex problems and simulate complex systems and being integrated into classical computers. Similar to a GPU, as it helps the cpu with processing.
- Quantum bits like classical bits have 0 and 1 states but they also have a superimposed state. The superimposed state is when the state is both 0 and 1. Like schrodingers cat, you only know the result when you observe the qubit. You do this by measuring the qubit. Once you measure the qubit, it destroys the superposition of the qubit. So you usually measure it after the set computations have been run 
- Unlike Classical Computer's bits, measuring a qubit in superposition is random and not deterministic. Essentially, there is a probability that you will get a certain value, and another probability where you will get another value from the superimposed qubit.
    - So, when running quantum registers through a simulator, multiple trials(called shots in Qiskit) are run and the result from each trial is recorded. The goal for these trials is to find the probability of each of the results when measuring the qubit. 
    - More trials will give a more precise answer of the probability but it will result in longer runtimes
- When gates are first initialized, usually the only value measured will be the default value. You only get superposition after applying a gate
    - Below is a simple defintion of one of these gates that can create superposition
        - Hardamad gate (h gate): quantum operation that superimposes qubit where there is a 50% chance of getting a 1 and 50% for a 0 when the qubit is measured.

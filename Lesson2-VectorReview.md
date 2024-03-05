# Lesson 2
## The Basic Math behind Quantum Computers
- Vector is a set of values that represents a quantity that has a magnitude and direction
- Vector dimension defines the space where the vector travels
    - Vectors in this case are written like matrices. Below is a column vector that is three dimensions because it has three rows. A two dimension vector would only have two rows, in this case. 


$$
\begin{bmatrix}
3 \\
5 \\
1 \\
\end{bmatrix}
$$
$$ \begin{bmatrix} 
   a & b & c \\
   c & e & f \\
   g & h & i \\
   \end{bmatrix} $$
- Magnitude of vector B notation: || B ||
- Multiplying a vector by a scalar, proportionally affects the vectors magnitude
- Normalization is just making a vector the unit vector where the magnitude is 1.
    - To do this just divide each of the elements in the vector by the vector's magnitude
- Adding vectors with the same dimension is just finding the sum of the corresponding values
- Inner product is just dot product from calc 3, except you can only do inner product of two vectors of the same dimension and one must be a column vector and the other must be a row vector.
    - If you have a two row or column vectors, you must transpose one of them before you calculate the inner product
        - Notation for transposed vector is the vector letter to the power T
    - Example (one column and one row vector):
    $$
    \vec{C} = 
    \begin{bmatrix} 
    3\\
    1\\
    \end{bmatrix}
    $$
    $$
    \vec{D} = 
    \begin{bmatrix} 
    1&&2
    \end{bmatrix}
    $$
    $$
    \vec{C} \cdot \vec{D}
    \equiv
    (1*3) + (2*1) = 5
    $$
    Example: Two row vectors
    $$
    \vec{C} = 
    \begin{bmatrix} 
    4&&5
    \end{bmatrix}
    $$
    $$
    \vec{D} = 
    \begin{bmatrix}
    3&&7
    \end{bmatrix}
    $$
    Must tranpose either vector C or C, I will do vector D
    <br>Transposing D:
    $$
    \vec{D}^{T} = 
    \begin{bmatrix}
    3\\
    7
    \end{bmatrix}
    $$
    Resulting inner product:
    $$
    \vec{C} \cdot \vec{D}^T
    \equiv
    (4*3) + (5*7) = 12 + 35 = 47
    $$


- Orthonormal basis:
    - Basis: Set of vectors that can be linearly combined to represent any other vector within space
        - Linear Combination: means using multiplication and additon to scale and add vectors together
    - Orthonormal: vectors are unit vectors and orthogonal
    - Orthonormal Basis: two unit vectors that are orthogonal to each other that can be used to represent any vector within a vector space through linear combination. Except, the unit vectors in the orthonormal basis cannot individually represent the other because they are orthogonal (they are linearly independent of each other) 
    - Example of vectors with an orthonormal basis are:
    $$
    \begin{bmatrix}
    0\\
    1\\
    \end{bmatrix}
    and
    \begin{bmatrix}
    1\\
    0\\
    \end{bmatrix}
    $$
- Lineraly Independent: vector that cannot be expressed as a linear combination of other vectors
    - There is no way you can represent <0,1> as <1,0> (this is another way to represent vectors within math in general) since they are orthogonal
        - These two vectors are the most simple and common. They are also used to represent the standard basis states for qubits
- Inner Product of orthogonal vectors is 0
## Complex Numbers
- One way of expressing a complex numbers is through the standard form $z = a + bi$
- Another way is to represent it through polar form as $z = re^{i\theta}$ where r is the magnitude of the vector and $\theta$ is the phase angle from the x-axis (the real number axis)
### Euler's Forumula
- Used to relate these two forms of the complex number where:
- $e^{i\theta} = cos(\theta) + isin(\theta)$
     - Multiplying this formula by r gives you $re^{i\theta} = rcos(\theta) + risin(\theta)$
     - Thus, $a = rcos(\theta)$ and $b = risin(\theta)$ 
     - We use both representations as some problems are easier to solve with a specific representation
### Calculating magnitude
- Calculating the magnitude of standard form is $|z| = \sqrt{a^{2}+b^{2}}$
- Calculating the magnitude of polar form is $|z| = r$
### Complex Conjugate
- Same as complex number but the component for the imaginary number is flipped
    - So, for $z = 1 + 2i$, the complex conjugate is $z^{*} = 1 - 2i$
    - For polar, $z = 3e^{i\frac{\pi}{4}}$, the complex conjugate is $z^{*} = 3e^{-i\frac{\pi}{4}}$
    - The magnitude of the complex number and its complex conjugate are the same
### Conjugate Transpose of Vector
- Also known as the Hermitian Conjugate or Hermitian Transpose
- As the name suggest the conjugate transpose is finding the conjugate of the vector and then transposing it
    - So, $\vec{E}^{\dagger} \equiv (\vec{E}^{T})^{*} \equiv (\vec{E}^{*})^{T}$
        - T represents transposing the vector and * represents the conjugate of the vector
$$
\vec{E} = 
\begin{bmatrix}
2i\\
13\\
6-i
\end{bmatrix}
$$
$$
\vec{E}^{\dagger} = 
\begin{bmatrix}
-2i && 13 && 6+i
\end{bmatrix}
$$
# Lesson 5
## What is a matrix?
- Rectangular array of values. The dimensions are described as "n rows x m columns"
    - An example of a 2 x 3 matrix is shown below:
        - $`\begin{bmatrix} 1 && 2 && 3\\
                           4 && 5 && 6\end{bmatrix}`$
## Matrix Multiplication
- You can multiply two matrices if the columns of the first matrix is equal to the rows of the second matrix
- Tip: Just compare the two inner dimensions when you put the matrices side by side
    - Example: If you want to find the product of a 2x2 matrix and a 2x1 matrix, like the dimnesions like:
     - 2x2 2x1
     - The two inner dimensions are 2, which are the equal meaning that you can multiply these two matrices
     - Also the dimensions of the resulting matrix wil be the two outside dimensions( the number of rows of the first matrix and the columns of the second matrix), so in this example the resulting matrix will be 2 x 1
- Example of multiplying a 2x2 matrix by 2x1 matrix:
    - Essentially multiply each row in the first matrix to each of the columns in the second matrix
    - $`\begin{bmatrix} a && b \\ c && d\end{bmatrix}\begin{bmatrix} x \\ y\end{bmatrix} = \begin{bmatrix} ax + by \\ cx + dy\end{bmatrix}`$
# Identity Matrix
- An identity matrix is a type of matrix where it is an n row by column matrix where the diagonal from the top left to the botom right is all 1s and the rest of the values in the matrix are 0.
    - Example of a 3x3 identity matrix: $`\begin{bmatrix} 1 && 0 && 0\\ 0 && 1 && 0\\ 0 && 0 && 1\end{bmatrix}`$
- What's special about identity matrices, is that if you multiply a identity matrix by another valid matrix, you will get the second matrix:
    - Example:
        -  $`\begin{bmatrix} 1 && 0 && 0\\ 0 && 1 && 0\\ 0 && 0 && 1\end{bmatrix} \begin{bmatrix}a \\ b \\ c\end{bmatrix} = \begin{bmatrix}a \\ b \\ c\end{bmatrix}`$
# Conjugate Transpose of a Matrix
- To make the tranpose a matrix make the rows of the matrix the columns and make the columns of the matrix its rows.
- To find the conjugate of a matrix, just convert each element in the matrix to it's complex conjugate
- To find the conjugate transpose, you have to conjugate and tranpose the matrix. The order in which you do it does not matter, you can do the tranpose and find the conjugate and you will get the same result
- Essentially: $`A^{\dagger} \equiv (A^{T})^{*} \equiv (A^{*})^{T}`$
- Example: $`A = \begin{bmatrix} a && b \\ c && d\end{bmatrix}`$
    - Transpose of A: $`A^{T} = \begin{bmatrix} a && c \\ b && d\end{bmatrix}`$
    - Conjugate of $`A^{T}`$ which gives you the conjugate transpose of A: $`(A^{T})^{*} = A^{\dagger} = \begin{bmatrix} a^{*} && c^{*} \\ b^{*} && d^{*}\end{bmatrix}`$

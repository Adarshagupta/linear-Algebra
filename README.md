# linear-Algebra


##Matrix Inversion 
Sure, let's solve Question 4 in more detail, which involves finding the inverse of matrix \(A\) and its transpose \(A^T\).

Given matrix \(A\):
\[ A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 5 \\ 1 & 0 & 2 \end{pmatrix} \]

### Step 1: Calculate the Determinant of \(A\)

The determinant of a \(3 \times 3\) matrix \(A = \begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}\) is given by:
\[ \text{det}(A) = a(ei - fh) - b(di - fg) + c(dh - eg) \]

For matrix \(A\), this becomes:
\[ \text{det}(A) = 1(3 \cdot 2 - 5 \cdot 0) - 2(2 \cdot 2 - 5 \cdot 1) + 3(2 \cdot 0 - 3 \cdot 1) \]
\[ \text{det}(A) = 1(6) - 2(4 - 5) + 3(-3) \]
\[ \text{det}(A) = 6 + 2 - 9 \]
\[ \text{det}(A) = -1 \]

### Step 2: Find the Adjugate (Adjoint) of \(A\)

The adjugate of \(A\) is the transpose of the cofactor matrix of \(A\). We calculate the cofactor for each element:

For \(a_{11}\) (1):
\[ C_{11} = \text{det}\begin{pmatrix} 3 & 5 \\ 0 & 2 \end{pmatrix} = 6 \]

For \(a_{12}\) (2):
\[ C_{12} = -\text{det}\begin{pmatrix} 2 & 5 \\ 1 & 2 \end{pmatrix} = -(4 - 5) = 1 \]

For \(a_{13}\) (3):
\[ C_{13} = \text{det}\begin{pmatrix} 2 & 3 \\ 1 & 0 \end{pmatrix} = -3 \]

For \(a_{21}\) (2):
\[ C_{21} = -\text{det}\begin{pmatrix} 2 & 3 \\ 0 & 2 \end{pmatrix} = -4 \]

For \(a_{22}\) (3):
\[ C_{22} = \text{det}\begin{pmatrix} 1 & 3 \\ 1 & 2 \end{pmatrix} = -1 \]

For \(a_{23}\) (5):
\[ C_{23} = -\text{det}\begin{pmatrix} 1 & 2 \\ 1 & 0 \end{pmatrix} = 2 \]

For \(a_{31}\) (1):
\[ C_{31} = \text{det}\begin{pmatrix} 2 & 3 \\ 3 & 5 \end{pmatrix} = -1 \]

For \(a_{32}\) (0):
\[ C_{32} = -\text{det}\begin{pmatrix} 1 & 3 \\ 2 & 5 \end{pmatrix} = 1 \]

For \(a_{33}\) (2):
\[ C_{33} = \text{det}\begin{pmatrix} 1 & 2 \\ 2 & 3 \end{pmatrix} = -1 \]

The cofactor matrix is:
\[ \text{Cof}(A) = \begin{pmatrix} 6 & 1 & -3 \\ -4 & -1 & 2 \\ -1 & 1 & -1 \end{pmatrix} \]

The adjugate (transpose of cofactor matrix) is:
\[ \text{adj}(A) = \begin{pmatrix} 6 & -4 & -1 \\ 1 & -1 & 1 \\ -3 & 2 & -1 \end{pmatrix} \]

### Step 3: Calculate the Inverse of \(A\)

The inverse of \(A\) is given by:
\[ A^{-1} = \frac{1}{\text{det}(A)} \text{adj}(A) \]

Since \(\text{det}(A) = -1\):
\[ A^{-1} = \begin{pmatrix} -6 & 4 & 1 \\ -1 & 1 & -1 \\ 3 & -2 & 1 \end{pmatrix} \]

### Step 4: Transpose of \(A\) and its Inverse

The transpose of \(A\) is:
\[ A^T = \begin{pmatrix} 1 & 2 & 1 \\ 2 & 3 & 0 \\ 3 & 5 & 2 \end{pmatrix} \]

Since \((A^T)^{-1} = (A^{-1})^T\), we find the transpose of \(A^{-1}\):
\[ (A^{-1})^T = \begin{pmatrix} -6 & -1 & 3 \\ 4 & 1 & -2 \\ 1 & -1 & 1 \end{pmatrix} \]

Thus, the inverse of \(A^T\) is:
\[ (A^T)^{-1} = \begin{pmatrix} -6 & -1 & 3 \\ 4 & 1 & -2 \\ 1 & -1 & 1 \end{pmatrix} \]

This completes the detailed solution for Question 4.

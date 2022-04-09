## Equivalent Statements
   - For an n * n matrix A
   - A is invertible
   - Ax = 0 has ONLY the TRIVAL solution x = 0
   - The reduced echelon form of A is I_n
   - A is a product of elementary matrices
   - Ax = b is consistent for every b
   - Ax = b has exactly one solution for every b
   - det(A) != 0
   - det(A^-1) = 1 / det(A)


## Lecture 1: LU Decomposition & Graph Theory

### 1. Theorem 1.6.1: LU Decomposition and Lower Triangular
       - If A is a matrix that can be reduced to a row echelon form U WITHOUT row interchanges
       - then A = LU where L is a lower triangular
       
### 2. Algorithm 1.6.2: LU Decomposition
       - Reduce A to row echlon form by Gaussian Eliminations (3 types of row operations) WITHOUT row interchange
       - If NOT possible, then A is NOT LU-Decomposable
       - Let L= E1^-1 * E2^-1 * ... * Ek^-1 where Ei is the elementary matrix corresponding to the ith row operarion used in obtaining U
       
### 3. FALSE: if matrix is A has an LU Decomposition then it is UNIQUE
       - Gaussian Elimination is NOT Unique
       
### 4. Once an LU Decomposition is known for a coefficient matrix A, solving linear systen Ax = b can by
       - solve Ly = b for y using forwarb substitutions
       - solve Ux = y for x using back substitutions
       
### 5. The adjancency matrix of an UNdirected graph is ALWAYS SYMMETRIC

### 6. Definition 1.7.7: Number of walks of length m
       - From vertex vi to vertex vj in G
       - is the (i, j) entruy of M^m
       
## Lecture 2: Economics Application & Determinant

### 1. Consumption Matrix Example
       - produce $1 coal: $0.1 coal + $0.25 steel + $0.1 automobile
       - produce $1 steel: $0.3 coal + $0.2 steel + $0.15 automobile
       - produce $1 automobile: $0.25 coal + $0.45 steel + $0.1 automobile
       - row 1 of Comsumption matrix C = [0.1 0.3 0.25]
       - row 2 of Comsumption matrix C = [0.25 0.2 0.45]
       - row 3 of Comsumption matrix C = [0.1 0.15 0.1]
       
### 2. Definition 1.8.3: Productive Matrix C
       - (I - C) is invertible
       - (I - C) ^ -1 haas non-negative entries
       - clearly, then ((I - C) ^ -1) * d = x will have non-negative entries
       
### 3. Theorem 1.8.4 Productive Comsumption Matrix C Sufficient Condition
       - All its column sums are LESS than 1
       
### 4. Proctive: Theorem 1.8.4 --> Definition 1.8.3

### 5. Definition 2.1.1; Determinant for n*n matrix A
       - n = 1, A = [a], det(A) = a
       - n = 2, row 1 of A = [a b], row 2 of a = [c d], then det(A) = ad - bc
       - n >= 2
         - C_ij(A) = (-1)^(i + j) * M_ij(A)
         - M_ij(A) is the det of A after deleting ith row and jth col
         - det(A) = (A)_11 * C_11(A) + (A)_12 * C_12(A) + ... + (A)_1n * C_1n(A)
         - such cofactor expansion could also be along any row/col
         
### 6. Remark 2.1.5: A has a row/col of 0s
       - Then det(A) = 0
       
       
## Lecture 3

### 1. Lemma 2.2.1: If A is an lower/upper triangular matrix
      - Then det(A) is the product of the main diagonal entries
      - i.e., det(A) = (A)_11 * (A)_22 * ... * (A)_nn
      
### 2. Theorem 2.2.2: det(A) = det(A^T)

### 3. Theorem 2.2.3: Square matrix A and Row Elementary Matrix Operations
       - If B is obtained from A by multiplying single row/col by scalar k, then det(B) = k * det(A)
       - If B is obtained from A by interchanging two rows/cols, then det(B) = - det(A)
       - If B is obtained from A by adding a scalar multiple of one row/col to another row/col, then det(B) = det(A)
       
### 4. Theorem 2.2.6: Elementary Matrix and its Determinant
       - Let E be an elementary matrix of size n * n
       - If E is obtained from I_n by multiplying of rows by a non-zero scalar k, then det(E) = k
       - If E is obtained from I_n by interchanging two rows/cols, then det(E) = -1
       - If E is obtained from I_n by adding a scalar multiple of one row/col to another row/col, then det(E) = 1
       
### 5. Theorem 2.2.7: det(kA)
       - if A is an n * n matrix
       - then det(kA) = k^n * det(A)
       
### 6. Theorem 2.2.8: n * n matrix A and elementary matrix E
       - det(EA) = det(E) * det(A)
       
### 7. Theorem 2.2.9: If A and B are n * n matrices
       - det(AB) = det(A) * det(B)
       

       

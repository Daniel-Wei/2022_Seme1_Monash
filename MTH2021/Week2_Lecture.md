## Equivalent Statements
   - For an n * n matrix A
   - A is invertible
   - Ax = 0 has ONLY the TRIVAL solution x = 0
   - The reduced echelon form of A is I_n
   - A is a product of elementary matrices
   - Ax = b is consistent for every b
   - Ax = b has exactly one solution for every b

## Lecture 1
### 1. Theorem 1.3.10: Linear Combination
       - Let A = [a1 a2 ... an] be an m * n matrix whose j_th column is the m*1 column vector a_j
       - If x is an n*1 column vector
       - Linear Combination: Then Ax = x1a1 + x2a2 + ... + xnan
### 2. Corollary 1.3.11
       - The ith column of A(m*n) is A*e_i
       - e_i = n*1 = [0 0 ... 1(ith) 0 .. 0]
### 3. Theorem 1.3.12: Let A be an m * n matrix
       - If Ax = 0 for all $x \in A$ (n * 1 column vector)
       - Then A = 0
### 4. Theorem 1.3.13
       - Let A = [a1 a2 ... an] (m * n matrix, each ai is a n*1 col vector)
       - Let B = [b1^T b2^T ... bn^T] (n*p matrix, each bi^T is a 1*p row vactor)
       - Then AB = sum of ak * bk^T
### 5. Theorem 1.3.15
       - m1, m2, n1, n2, p1, p2 all positive integers
       - m = m1 + m2, n = n1 + n2, p = p1 + p2
       - For i, j in {1, 2}, A_ij = m_i * n_j matrix, B_ij = n_i * p_j matrix
       - Then AB row 1 = [(A11*B11 + A12*B12) (A11*B12+A12*B22)
### 6. Let A and B be n * n matrices
       - tr(A + B) = tr(A) + tr(B)
       - tr(AB) = tr(BA) = tr(A) * tr(B)
       - proof: sum signal positions can be exchanged
### 7. Theorem 1.4.1 Matrix Arithmetic
       - For all matrices A, B, C of compatible sizes and all scalars a, b, c
       - + is commutative: A + B = B + A
       - + is associative: A + (B + C) = (A + B) + C
       - x is associative: A(BC) = (AB)C
       - Left distributive law: A(B+ C) = AB + AC
       - Right distributive law: (B+C)A = BA + CA
       - a(B + C) = aB + aC
       - (a + b)C = aC + bC
       - a(bC) = (ab)C
       - a(BC) = (aB)C = B(aC)
### 8. Definition: Invertible
       - A square matrix A is called invertible if there is a matrix B such that AB = BA = I
       - if this case B is called the inverse of A and write as B = A^(-1)
       - If no such B exists then A is singular
       
       
## Lecture 2

### 1. Theorem 1.4.3: Invertible then inverses and transposes
       - If B and C are both inverses of A then B = C
       - If A, B invertible and of same sizes, then AB is invertible and (AB)^-1 = B^-1 * A^-1
       - If A is invertible, then so is A^-1, and (A^-1)^-1 = A
       - If A is invertible, then so is A^T, and (A^T)^-1 = (A^-1)^T
### 2. Lemma 1.4.4: Properties of the Transpoose
       - (A^T)^T = A
       - (A + B)^T = A^T + B^T
       - (kA)^T = k*A^T
       - (AB)^T = B^T * A^T
### 3. Definition 1.5.1; Elementary Matrix
       - Can be obtained from the I by performing a SINGLE row operation
       - Multiply of row by a non-zero scalar
       - Interchange two rows
       - Add a multiple of one row to another
### 4. Corollary of Each Row Operarion is INVERTIBLE
       - if u is an elementary row operation
       - then u^-1 exists
       - such that u(A) = B and u^-1(B) = A
### 5. Theorem 1.5.4: row elementary matrix and identity matrix
       - Let u denote an elementary row operarion on m-row matrices
       - Let A be an m * n matrix and I be the m * m matrix
       - E = u(I) then u(A) = EA
### 6. Theorem 1.5.5: Elementary matrix and Inverse
       - Every elementary matrix is invertible
       - Inverse of every elementary matrix is also an elementary matrix
       
## Lecture 3

### 1. Algorithm 1.5.8: Finding Inverse Algorithm
       - For an invertible matrix A
       - Start with the partitioned matrix [A|I]
       - Perform elementary row operattion on [A|I] to [I|B]
       - B = A^-1
       
### 2. Remark 1.5.9: If A is NOT invertible
       - step 2 of algorithm 1.5.8 will show: A row of zeros would appear on the LHS
       
### 3. Theorem 1.5.11: Left and Right Inverse
       - If a square matrix A has either a left inverse (BA = I) or a right inverse (AB = I)
       - then A is invertible and its inverse is B

### 4. Lemma 1.5.12: Not invertible and product
       - if either A or B is NOT invertible
       - then AB is NOT invertible

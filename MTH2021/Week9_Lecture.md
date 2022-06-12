## Lecture 1: 2nd May 2022

## Chapter 5.4 Matrix Representations

### 1. Def 5.4.1: Matrix for T Relative to the Base B and B'
       - Let T: V -> W be a linear transformation
       - B = {v1, v2, ..., v_n} is a basis for V
       - B' = {w1, w2, ..., w_m} is a basis for W
       - Define the Matrix for T Relative to the Base B and B' as
         -- [T]_(B', B) = [[T(v1)]_B', [T(v2)]_B', ..., [T(v_n)]_B']
         
### 2. Theorem 5.4.2: {T}/B'B * {x}/B = {T(x)}/B"
       - Let T: V -> W be a linear transformation
       - B is basis for V and B' is a basis for W
       - [T]_(B', B) = [[T(v1)]_B', [T(v2)]_B', ..., [T(v_n)]_B']
       - x = c1*v1 + c2*v2 + ... cn * vn
       - T(x) = c1*T(v1) + c2*T(v2) + ... + cn * T(vn)
       - T(x)_B' = c1*T(v1)_B', c2*T(v2)_B', ... , cn * T(vn)_B'
       - [x]_B = (c1, c2, ..., cn)
       - [T]_(B', B) = [[T(v1)]_B', [T(v2)]_B', ..., [T(v_n)]_B']
       
### 3. Algorithm 5.4.3: Given x in V, compute T(x)
       - Suppose T: V -> W is a linear transformation
       - V and W have bases B and B' respectively
       - (i): Calculate the coordinate vector [x]_B of x with respect to B
       - (ii): Calculate [T]_B'B the matrix for T relative to B and B'
       - (iii): Compute the matrix product [T]_B'B * [x]_B yielding [T(x)]_B'
       - (iv): Use [T(x)]_B' to find T(x)

### 4. Example 5.4.4: Let T: P2 -> P1 as T(a0 + a_1 * x + a_2 * x^2 = (a_0 + a_1) - (2 * a_1 + 3 * a_2) * x
       - p0(x) = 1, p1(x) = x, p2(x) = x^2
       - T(p0) = 1, T(p1) = 1 - 2x, T(p2) = -3x
       - [T]_B'B = ((1 0), (1 -2), (0 -3)) = ((1 1 0), (0 -2 -3))
       - p(x) = a_0 + a_1 * x + a_2 * x^2
       - p(x)_B = (a_0, a_1, a_2)
       - p(x)_B * [T]_B'B = ((1 1 0), (0 -2 -3)) * (a_0, a_1, a_2) = ((a_0 + a_1), (-2 * a_1 - 3 * a_2))
       - [T(p(x))]_B' = ( (a_0 + a_1), (-(2 * a_1 + 3 * a_2)) ) = ((a_0 + a_1), (-2 * a_1 - 3 * a_2))
       
       
### 5. Theorem 5.4.5: Matrix Representations and Change of Bases
       - B and B' are bases for n-dimensional vec space V
       - I： V -> V is the identity operator on V
       - P_B->B' = [I]_B'B
       
### 6. Theorem 5.4.6: Matrix Representations and Compositions of Linear Transformations
       - If T1: U -> V and T2: V -> W are linear transformations
       - If B, B', B" are bases for U, V and W
       - [T2 * T1]_B'B = [T2]_B'B" * [T1]_B"B


## Lecture 2: 3rd May 2022

### Chapter 6 Eigenvalues & Eigenvectors

## Chapter 6.1 Eigenvalues & Eigenvectors (A&R $5.1)

### 1. Def 6.1.1 Eigenvector/EigenValue of A (n*n matrix)
       - A NON-Zero vector x in R^n is called an eigenvector of A
       - or to say, of the linear operator T_A
       - IF Ax = kx for some k in R
       - The Scalar k is called an eigenvalue of A (or T_A)
       - x is said to be "an eigenvector corresponding to k" 
       
### 2. Theorem 6.1.5 Find All Eigenvalues of A
       - If A is an n*n matrix, then k in R is an eigenvalue of A
       - IFF det(k*I - A) = 0
       - k is an eigenvalue of A ---> Ax = kx for some x!= 0
         ---> (A - k*I)x = 0 for some x!= 0
         ---> As Ax = 0 has ONLY the Trivial Solution when det(A) = 0, det(A - k*I) == 0 

### 3. Lemma 6.1.8 Characteristic Polynomial of A
       - For any n*n matrix A, the quantity det(k*I - A) is a monic(coefficients of the highest degree = 1) polynomial in k of degree n
       - Case n = 2
       - A = row1-(a b), row2-(c d)
       - k*I - A = row1-(k-a, b), row2 - (c, k-d)
       - det(k*I - A) = (k-a)(k-d) - bc = k^2 - (a+d)k + ad - bc
       - Coefficient of k^2 is 1

### 4. FALSE: The eigenvakues of a matrix is equal to the eigenvalues of its reduced row echelon form

### 5. Theorem 6.1.10 If A is an n TRIANGULAR Matrix, then its eigenvalues are the entries on its Main Diagonal
       - As A is an TRI matrix, k*I - A would also be an TRI
       - As det of TRI is the product of its main diagonal entries, det(k*I - A) 
         = (k - A_11) * (k - A_22) * ... * (k - A_nn)
         
### 6. Def 6.1.12 EigenSpace
       - The eigenspace of the square matrix A for the eigenvalue k is
       - Null(k*I - A), the set of all solutions of the homogeneous sys (k*I - A)x = 0

### 7. Theorem 6.1.14 Polynomial Eigenvalue
       - If k is a positive int, w an eigenvalue of A and x is a corresponding eigenvector
       - Then w^k is an eigenvalue of A^k and x is a corresponding eigenvalue
       
### 8. Theorem 6.1.16 A Square matrix A is Invertible IFF k = 0 is NOT an eigenvalue
       - k = 0 is an eigenvalue of a <=> det(-A) = 0 <=> A is NOT invertible
       
### 9. Q: Does there exist a matrix A with Independent Cols and characteristic polynomial det(k*I- A) = k^2 + k
       - NO
       - As det(k*I - A) = 0 = k(k+1) --> k = 0 or k = -1
       - As A with independent cols --> A is invertible --> k = 0 is NOT an eigenvalue of A
       
### 10. Def 6.1.17 Algebraic Multiplicity & Geometric Multiplicity of an Eigenvalue
       - Let alpha be an eigenvalue of a square matrix A
       - Alpha has a Algebraic Multiplicity k IF k is the LARGEST in such that (lambda - alpha) ^k is a factor of the characteristic polynomial det(lambda*I - A)
       - dim of corresponding eigenspace is the Geometric Multiplicty of Alpha
       
### 11. Theorem 6.1.18 For every eigenvakue of a square matrix, its Geometric Multiplicity is Less than or Equal to the Algebraic Multiplicity. 
        


## Lecture 3: 4th May 2022

### Chapter 6.2 Diagonalization

### 1. Def 6.2.2 Similar Matrix
      - A Square Matrix B is Similar to a Square Matrix A (B ~ A)
      - IF there exists an Invertible Matrix P such that B = P^-1 * A * P
      
### 2. Theorem 6.2.3 Suppose A ~ B, Then: 
      - det(A) = det(B)
      - A and B have the Same Characteristic Polynomial
      - The Geometric Multiplicities of Each Eigenvalue are the same
      
### 3. Def 6.2.4 Diagonalizable
       - If Square Matrix A is Similar to a Diagonal Matrix
       - If A = P * D * P^-1 for Diagonal D, then we say P diagonalizes A
       
### 4. Theorem 6.2.5 Equivalent Statements for n^2 Square Matrix A
       - A is Diagonalizable
       - A has n Linearly Independent Eigenvectors
       - For each Eigenvalue, its Geometric Multiplicity equals its Algebraic Multiplicty, and the sum of all Algebraic Multiplicities is n
       - Based on the proof, P is the set of n L.I Eigenvectors
       
### 5. FALSE: IF A is Diagonalizable, then there exists a Unique matrix P such that P^-1 * A * P is Diagonal. 
       - A is Diagonalizable --> A =  P * D * P^-1 
       - --> P^-1 * A * P = D is Diagonal
       - However, P is NOT Unique, as P is the n L.I Set of Eigenvectores
       
### 6. Theorem 6.2.6 If v1, v2, ... vn are eigenvectors of a matrix A corresponding to distinct eigenvalues, then {v1, v2, ... vn} is a L.I set

### 7. Corollary 6.2.7 If an n^2 matrix has n distinct eigenvalues, then A is diagonalizable

### 8. Algorithm 6.2.5 Diagonalization, Let A be an n^2 Matrix
       - Step 1: Find the eigenvakues of A, and then find a basis for each eigenspace of A
       - Step 2: Let S denote the union of all such basis vectors. If S contains Fewer than n vectors, A is NOT Diagonalizable
       - Step 3: If S = {p1, p2, ... pn}, then define P = [p1, p2, ... pn]
       = Step 4: The matrix D = P^-1 * A * P. Its diagonal entries k1, k2, ..., kn are the eigenvalues corresponding to eigenvectors p1, p2, ...,pn

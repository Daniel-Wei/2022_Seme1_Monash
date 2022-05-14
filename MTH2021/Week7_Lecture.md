## Lecture 1

### 1. Corollary 4.7.6 Let V and W be subspaces of Euclidean n-space(R^n)
       - IF V is ORTHOGONAL to W then V + W = V **O+** W aka their sum is DIRECT
       
### 2. Definition 4.7.7 Orthogonal Complement
       - Let W be a subspace of Euclidean n-space
       - The Orthogonal Complement of W is the set W^T* 
       - W^T*: all vectors in R^n that are orthogonal to every vector of W
   
### 3. Theorem 4.7.8 If W is a subspace of R^n THEN SO W^T*
       - Subspace Test
       - 1. Non-Empty: 0 vec is orthogonal to any vec in W so 0 vec in W^T*
       - 2. Closure Under +: Let v1, v2 in W^T* and w in W --- (v1 + v2) . w = 0
       - 3. Closure under scalar x: kv1 . w = k * (v1.w) = 0
       
### 4. Theorem 4.7.9 If W is a subspace of R^n, then their Sum of W and W^T* is Direct and is R^n
       - Example: V is the xz-plane and W is the y-axis in R^3
       - Then R^3 = V O+ W (sum, which is Direct)
       
### 5. Theorem 4.7.10 If A is an m * n matrix then [row(A)]^T* = null(A)
       - Def 4.5.1 Row Space: denoted by row(A), is the subspace of R^n spanned by the rows of A
       - Def 4.5.2 Col Space: denoted by col(A), is the subspace of R^m spanned by the cols of A
       - Def 4.5.3 Null Space: denoted by null(A), is the set of all solutions x in R^n of homogeneous equation Ax = 0
       
### 6. Corollary 4.7.11 Let A be any m * n matrix
       - (a) R^n = row(A) O+ null(A): prove by theorem 4.7.10
       - (b) R^m = col(A) O+ null(A^T)
         Applying (a) to A^T can get R^m = row(A^T) O+ null(A^T)
         Preciously row(A^T) = col(A)

### 7. Proof of Theorem 4.7.10
       - Let A = [r1, r2, ... rm] where ri in R^n
       - Part 1: null(A) is a subset of (row(A)) ^ T*
         (Ax)_i = (sum of j to n) A_ij * x_j = (sum of j to n) (ri)_j * x_j =r_i * x
         If x in null(A) then Ax = 0 ==> ri * x = 0 for all 1 <= i <= m
         So if r in row(A) then x * r = x * [(sum of i to m) c_i * r_i] = (sum of i to m) c_i *(x * r_i) = 0
         ==> x in (row(A)) ^ T*
         ==> null(A) is a subset of (row(A)) ^ T*
         
       - Part 2: (row(A)) ^ T* is a subset of null(A)
         if x in (row(A)) ^ T* then x * r = 0 for all r in null(A)
         so in particular x * r_i = 0 as x * r = x * [(sum of i to m) c_i * r_i] = (sum of i to m) c_i *(x * r_i) = 0
         ==> (Ax)_i = 0 ==> Ax = 0
         ==> x in null(A)
         ==> (row(A)) ^ T* is a subset of null(A)
         
### 8. Theorem 4.7.12 Let A be an m * n matrix 
       - For EVERY b in col(A) there exists a UNIQUE p in row(A)
       - such that the space of all solitions to Ax = b is {x = p + z : z in null(A)}
       - AKA: The linear system Ax = b is CONSISTENT IFF Co-domain is the col(A)
       
       - PROOF
         --- Let x, y in R^n 
             Then by Corallary 4.7.11 ==> x = p + z and y = q + w, where p, q in row(A) and z, w in null(A)
         --- Let b = Ax = A(p + z) = Ap + Az = Ap
             Let b = Ay = A(q + w) = Aq + Aw = Aq
             ==> Ap = Aq ==> A(p - q) = 0 ==> (p - q) in null(A)
         --- But row(A) is a subspace so (p - q) in row(A)
             ==> (p - q) in [row(A) intersect null(A)] aka [row(A) intersect (row(A)) ^ T* == {0}
             ==> So EVERY solution to Ax = b is of the form x = p + z with z in null(A) and the SAME p in row(A)
             
### 9. Theorem 4.7.13 Let A be an m * n matrix. Then Ax = b is CONSISTENT for ALL b in R^m IFF null(A^T) = cokernel of A = coker(A) = {0}
         


## Lecture 2

### 1. Definition 4.8.1 Field F
       - Non-Empty Set, Define two operations: + and *
       - So that for EACH PAIR of a, b in F there exist UNIQUE elements a + b And a * b in F
       - For which the following axioms hold
         F1: Commutativity: a + b = b + a and a * b = b * a for ALL a, b in F
         F2: Associativity: a + (b + c) = (a + b) + c and a(bc) = (ab)c for all a, b, c in F
         F3: Distributivity: a(b + c) = a*b + a*c for all a, b, c in F
         F4: Identities: There exist distince elements 0, 1 in F such that a + 0 = a and 1 * a = a for all a in F
         F5: Additive Inverse: For each a in F there exists -a in F for which a + (-a) = 0
         F6: Multiplicative Inverse: For each a in F\{0} there exists a^-1 in F for which a *  a^_1 = 0
         
### 2. Some Common Fields
       - Q: the rational numbers
       - R: the real numbers
       - C: the complex numbers
       - Z_p: the set of integers modulo a prime number p = {0, 1, 2, ..., p - 1}
       
### 3. Remark 4.8.4 Z_p makes sense for all p in N BUT Z_p NOT a Field UNLESS p is PRIME

## 4.9 Coding Theory

### 4. Number of elements of (Z_p)^n = p^n
         
### 5. Checksum: 1-bit Error Detecting, add one more bit which is (sum of previous bits) mod p

### 6. 4.9.2 Error-Correcting Codes: Hamming(7, 4) Code
       - a method of transmitting 7-bit encodings of 4-bit words
       - allows us to correct 1-bit transmission errors
       - Consider a 4-bit word d = (d1, d2, d3, d4) in (Z_2) ^ 4
       - The Hamming(7,4) code encodes d in a 7-bit word (d1, d2, d3, d4, p1, p2, p3) where
         p1 = d2 + d3 + d4
         p2 = d1 + d3 + d4
         p3 = d2 + d2 + d4
       - Define the GENERATOR MATRIX G by
         row 1: 1 0 0 0 0 1 1
         row 2: 0 1 0 0 1 0 1
         row 3: 0 0 1 0 1 1 0
         row 4: 0 0 0 1 1 1 1
       - Consider each word d in (Z_2)^4 to be a row vector, we can compute the corresponding codeword c in (Z_2)^7 by matrix multiplication c = dG

### 7. Lemma 4.9.3 The Set of Codewords generated by G is row(G)

### 8. Parity Check Matrix H
     - Row 1: 0 0 0 1 1 1 1
     - Row 2: 0 1 1 0 0 1 1
     - Row 3: 1 0 1 0 1 0 1
     - c (in (Z_2)^7 )will be a valid codeword IFF H*c^T = 0
     
### 9. Theorem 4.9.5: Row(G) = Null(H)

### 10. Example c = [1 0 0 1 1 0 0], H * c^T = (2 0 2) = (0 0 0) as in Z_2 ==> c is a valid codeword

### 11. One Error Correction
      - H * y^T = H * (c^T + (e_i)^T) = H * (e_i)^T
      - Which is the i_th Column of H
      - So if H * y^T == i_th col of H, then the error must be in the i_th bit
      - Correction: Flipping the i_th bit
      
      
      
## Lecture 3: 26th April

### Chapter 5: Linear Transformations

### 1. Def 5.1.1 Linear Transformations
       - Let V and W be vec spaces
       - If T: V -> W satisfies T(u + k*v) = T(u) + k*T(v) for all u,v in V and all scalars k
       - Then T is a linear transformation 

### 2. Linear Operators: Linear Transformations with V = W

### 3. Example: Let M_nm be the vec space for all n * m real matrices, show that the transformation T: M_nm -> M_mn defined by T(A) = A^T, A in M_nm is linear
       - Let A, B in M_nm and k in R
       - Transpose of sum is sum of transpose: T(A + kB) = (A + kB)^T = A^T + (kB)^T
       - Transpose of scalar matrix is scalar transpose of matrix: A^T + (kB)^T = A^T + k * B^T
       - So T is linear
       
### 4. Lemma 5.1.3: If T: V -> W is a linear transformation, then T(0) = 0

### 5. Linear Transformations PRESERVE Linear Combinations

### 6. Theorem 5.1.6: Transformation Image of Linear Combinations is Linear Combinations of Transformation Images
       - If T -> V is linear
       - Then T(k1u1 + k2u2 + ... _ k_r * u_r) = k1 * T(u1) + k2 * T(u2) + ... + k_r * T(u_r)
       - for all u1, u2, ..., u_r in V and all scalars k1, k2, ..., k_r in R
       
### 7. Let V, W be vec spaces, let T: V -> W be linear, and let S ba a basis for V
       - Theorem 5.1.6 implies that knowing the value of T(v) for each v in S is SUFFICIENT to completely determine T
       
### 8. Example: Consider the basis S = {v1, v2} for R^2, where v1 = (-2, 1) and v2 = (1, 3). And let T: R^2 -> R^3 be the linear transformation such that T(v1) = (-1, 2, 0) and T(v2) = (0, -3, 5)
       - Find T(-5, -1)
       - (-5, -1) = 2v1 - v2
       - T(-5, -1) = T(2v1 - v2) = 2T(v1) - T(v2) = 2(-1, 2, 0) - (0, -3, 5) = (-2, 7, -5)
       
### 9. Def 5.1.9: Kernel and Range of Linear Transformations
       - If T: V -> W is a linear transformation 
       - Then the set of all v in V mapped to 0 is called the kernel of T, denoted by ker(T)
       - Then the set of all w in W that are images under T of at at leasyt one v in V is called the range of T, denoted by ran(T)
       
### 10. Example 5.1.10: If T_A: R^n -> R^m is a matrix transformation, then ker(T_A) = null(A) and ran(T_A) = col(A) 
        - R^n: n-vec, set of all n-tuples of real numbers, n*1 matrix
        - A has to be m * n (Week 5, Lecture 1)
        - null(A) is Ax = 0, wherex is in R^n
        - Week 6, Lecture 1: Theorem 4.5.5: A Linear System Ax = b is Consistent IFF b in col(A)

### 11. Example 5.1.11: Let P_n denote the vec space of all polynomials of degree at most n and let T: P2 -> P3 be defined by: T[p](x) = x*p(x) for all p in P2
        - Which of the following elements of P2 belongs to the ker(T): p1(x) = x^2 + x, p2(x) = 0, p3(x) = 1 + x
        - T[p1] = x^3 + x^2, NOT in ker(T)
        - T[p2] = 0, IN ker(T) or by Lemma 5.1.3
        - T[p3] = x + x^2, NOT in ker(T)

### 12. Theorem 5.1.12 If T: V -> W is a Linear Transformation, then ker(T) is a subspace of V and ran(T) is a subspace of W
        - Proof of ran(T) is a subspace of W
        - ran(T) = {y in W: y = T(x) for some x in V}
        - Subspace Test 1: Not Empty/ Contains 0: Lemma 5.1.3 == T(0) = )
        - Subspace Test 2: Closure Under +
              - y1 = T(x1) and y2 = T(x2)
              - By Linearity: y1 + y2 = T(x1) + T(x2) = T(x1 + x2)
        - Subspace Test 3: Closure Under Scalar *
              - y1 = T(x1) and k in R
              - ky1 = k * T(x1) = T(k * x1) [Preserve Linear Combinations Special Case]

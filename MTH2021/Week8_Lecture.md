## Lecture 1: 26th April

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


## Lecture 2: 27th April, 2022

### 1. Def 5.1.13: rank(T) and nullity(T)
       - Let T: V -> W be a linear transformation
       - If ran(T) is finite dimensional, then its dimension is rank(T)
       - If the ker(T) is finite dimensional, then its dimension is nullity(T)
      
### 2. Theorem 5.1.14: Rank - Nullity Theorem
       - Let T: V -> W be a linear transformation from an n-dimensional vec space V to a vec space W
       - Then rank(T) + nullity(T) = n
       - Aka: The dim(ran(T)) + dim(ker(T)) = n
      

## Chapter 5.2 Compositions 

### 3. Theorem 5.2.1: Compositions of Linear Transformations 
       - If T1: U -> V and T2: V -> W are linear transformations
       - Then T2 ???T1: U -> W is also Linear
       
       
## Chapter 5.3 Isomorphism ????????????

### 4. Theorem 5.3.1: If T: V -> W is a linear transformation, then T is one-to-one IFF ker(T) = {0}
       - Lemma 5.1.3 ==> T(0) = 0 ==> 0 in ker(T)
       - If T is one-to-one, then nothing else in the ker(T) except 0
       - Conversely, suppose u, v in V and T(u) == T(v)???then T(u) - T(v) = 0, 
         -- And it follows by linearity that T(u - v???= 0, u - v is a linear combinations of u and v so is in V
         -- So if ker(T) = {0}, then u - v = 0, which implies T is one-to-one
         
### 5. Theorem 5.3.2 Let V and W be n-dimensional vec spaces, and Let T: V -> W be a linear transformation. 
       - Then T is one-to-one IFF T is onto
       
### 6. Def 5.3.3 Isomorphism T
       - T: V -> W is a linear transformation, and both one-to-one and onto
       
### 7. Def 5.3.4 V ~= W, V and W are isomorphic
       - If there exists an isomorphism from vec space V to vec space W
      
### 8. Theorem 5.3.5 For Any Vec Spaces U, V and W we have:
       - (i) U ~= U (Reflexivity)
       - (ii) If U ~= V then V ~= U (Symmetry)
       - (iii) If U ~= V and V ~= W then U ~= W (Transitivity)
       
### 9. Show that the linear transformation T: P2 -> R^3 defined by T(a + b*x + c*x^2) = (a, b, c) is an isomorphism
       - One-to-one: p(x) = a + bx + c*x^2 is in ker(T) => T(p) = (a, b, c) = (0, 0, 0). 
         -- Then p(x) is the 0 polynomial, and by theorem 5.3.1, T is one-to-one
       - Onto: Since dim(R^3) = dim(P2) and T is a linear transformation, which implies T is also onto
       
### 10. Theorem 5.3.9 Let U and V be finite-dimensional vec spaces. If dim(U) == dim(V), then U ~= V
        - Let B_U = {u1, u2, ..., u_n) and B_V = {v1, v2, ... v_n} [B = Basis]
        - Define T: U -> V so that for all x1, x2, ..., x_n in R
        - T(sum of x_i * u_i for i from 1 to n) = sum of x_i * v_i for i from 1 to n
        - Need to prove T: is a Linear Transformation & Bijection
        
### 11. Theorem 5.3.10: Isomorphism T: V -> R^n and Basis B for V
        - Let V be an n-dimensional real vec spaces and B be a basis for it
        - Define the map T: V -> R^n via T(v) = [v]_B for all v in V
        - Then T is an isomorphism
        - v in V is sum of c_i * b_i for i for 1 to n (b_i in B and c1, c2, ..., c_n in R)
        - [v]_B = (c1, c2, ..., c_n
        
### 12. Prove a map T: V -> W is an isomorphism
        - Linear Transformation: Prove Linearity, aka, T(v + kw) = T(v) + k * T(w)
        - One-to-one: ker(T) = {0}
        - Onto: dim(V) == dim(W)

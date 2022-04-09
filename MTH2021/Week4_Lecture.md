## Lecture 1

### 1. Definition 3.1.1: n-Space R^n
       - Set of all ordered n-tuples, v = (v1, v2, ... vn), vi is real number
       - together with operations + and scalar x
       - the vector (0 0 ... 0) is called the zero vector

### 2. Unless stated, consider elements of R^n to be column vectors

### 3. Remark 3.1.3: R^n and e_i
       - Every v = (v1 v2 ... vn) can be expressed as v = v1e1 + v2e2 + ... + vnen
       
### 4. Function/Transformation/Map
       - T: D -> C from a set D to a set C
       - is a rule that assigns each x in D to a UNIQUE element T(x) belongs to C
       - D: Domain
       - C: Co-domain
       - T(x): the image of x under T
       - Range of T: { T(x): x in D }, the set of all images
       
### 5. Onto & One to One
       - Onto/Surjective: Ran(T) = c
       - One-to-One/Injective: if x != y, then T(x) != T(y)
       - Bijective: both surjective and injective
       
### 6. Matrix Transformations
       - A: m * n matrix
       - Transformation T_A: R^n -> R^m, is defined by T_A(x) for all x in R^n
       - A is the Standard Matrix for the T_A
       
### 7. Theorem 3.3.4: Unique Standard Matrix
       - Every matrix transformation has a unique standard matrix
       
### 8. Definition 3.3.5: Linear Transformation T: R^n -> R^m
       - if T(u + kv) = T(u) + k*T(v)
       - for all u, v in R^n and any k in R
       
### 9. Theorem 3.3.6: Every Matrix Transformation is LINEAR

### 10. Theorem 3.3.7: Linear Transformations Preserve Linear Combinations
        - Let T: R^n -> R^m be linear
        - Then for any r we have: T(k1u1 + k2u2 + ... + krur) = k1*T(u1) + k2*T(u2) + ... + kr*T(ur)
        
### 11. Theorem 3.3.8: Every Linear Transformation IS a Matrix Transformation
        - IF T: R^n -> R^m is linear, then it is a matrix transformation
        - Its Standard Matrix IS A = [ T(e1), T(e2), ... T(en)]
        
## Lecture 2

### 1. Theorem 3.4.1: Composition of Matrix Transformations
       - If T_A: R^n -> R^k and T_B: R^k -> R^m, with Standard Matrices A and B
       - Then T_B composite T_A = T_BA, i.e., T_B( T_A(x) ) = (B*A) * (x) = T_BA(x)
       
### 2. Theorem 3.4.3: Square Matrix as the Standard Matrix for a Matrix Transformation
       - If A is an n * n square matrix and T_A: R^n -> R^n is the corresponding matrix transformation
       - Then the following statements are EQUIVALENT
         - A is invertible
         - Range of T_A is R^n (surjective)
         - T_A is one to one (injective)
         
### 3. Dot Product, Norm and Distance
       - Euclidean Inner/Dot Product: u.v = u1v1 + u2v2 + ... + unvn
       - The space R^n, together with the E inner product, is called Euclidean n-space
       - Norm/Length = |v| = (v.v)^(1/2)
       - Distance d(u, v) = |u - v|
       - Orthogonal: if u.v = 0
       
### 4. Theorem 3.5.5: Dot Product Equivalence
       - u, v are in R^n, and A is a n*n matrix
       - u.v = u^T . v
       - (A*u).v = u.(A^T*V)
       
### 5. Vector Spaces: Non-empty sets V with operations + and scalar x, following 10 axioms
       - A1: closure under +: if u,v in V, then u + v in V
       - A2: Addittion is communtative: u + v = v + u for all u, v in V
       - A3: + is associative: (u + v) + w = u + (v + w) for all u, v, w in V
       - A4: zero: exists an element 0 in V such that u + 0 = u for all u in V
       - A5: Negatives: For each u in V, exists -v in V, such that u + (-u) = 0
       - A6: Closure under scalar x: k*u in V for all u in V and any k in R
       - A7: Distributivity of vector +: k(u + v) = ku + kv for all u, v in V and k in R
       - A8: Distributivity of scalar +: (k + m) * u = k*u + m * u for any u in V and k, m in R
       - A9: Scalar x is associative: k(m*u) = (k*m)*u for any u in V and k, m in R
       - A10: Scalar Identity: 1*u = u for any u in V
       
      
## Lecture 3

### 1. Theorem 4.1.3: V is a vector space, u, v in V
       - 0 + v = v (A4 is v + 0 = v)
       - -v + v = 0 (A5 is v + -v = 0)
       - if v + w = v, then w = 0
       - if v + w = 0, then w = -v
       
### 2. Notations
       - Zero Vector Space: V = {0}
       - n-space: R^n
       - The Space R^(infinite sign) is of infinite sequences of reals
       - The Space M_mn is of all m * n matrices
       - The Space P_n is of all polynominals of degree at MOST n
       - The Space P_(infinite sign) is of all polynomials of arbitraty degrees
       - The Space C[0, 1] is of all continuous functions f: [0, 1] -> R
       
### 3. Theorem 4.1.6: V is a vector space, u in V and k in R
       - 0u = 0
       - k0 = 0
       - (-1)u = -u
       - if ku = 0 then either k = 0 or u = 0
       
### 4. Definition: Subspace W of a Vector Space V
       - W is an non-empty subset of V
       - Under the same + and scalar x defined on V

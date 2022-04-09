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
         - 
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        

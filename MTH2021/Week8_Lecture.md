## Lecture 1: 27th April, 2022

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
       - Then T2 。T1: U -> W is also Linear
       
       
## Chapter 5.3 Isomorphism 类质同像

### 4. Theorem 5.3.1: If T: V -> W is a linear transformation, then T is one-to-one IFF ker(T) = {0}
       - Lemma 5.1.3 ==> T(0) = 0 ==> 0 in ker(T)
       - If T is one-to-one, then nothing else in the ker(T) except 0
       - Conversely, suppose u, v in V and T(u) == T(v)，then T(u) - T(v) = 0, 
         -- And it follows by linearity that T(u - v）= 0, u - v is a linear combinations of u and v so is in V
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
        
        































































         
         
         
         
         
         
         
         
         
         
         
         
         
         
         

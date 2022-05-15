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
       - Need More Thinking
       
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


























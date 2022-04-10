## Lecture 1

### 1. Theorem 4.3.15: Subset contains n vectors in n-demensional vector space
       - Let V be an n-dimensional vector space and let subset S contain n vectors
       - S is a basis for V IFF S is linearly independent
       - S is a basis for V IFF S Spans V
       
### 2. Theorem 4.3.16: Subspace of a finite-dimensional vector space
       - If W is a subspace of a finite-dimensional vector space V
       - dim(W) <= dim(V)
       - W = V IFF dim(W) = dim(V)
       
### 3. Theorem 4.3.17: Let S be a finite set of vectors in a finite dimensional vector space V
       - If S Spans V, then S contains a subset which is a basis for V
       - If S is linearly independent, then S is a subset of a basis
       
## Chapter 4.4    Coordinates & Change of Basis

### 4. Theorem 4.4.1 Basis Vectors and UNIQUE Linear Combination
       - If B = {v1, v2, ... , vn} is a basis for a vector spoace V
       - then for every vector v in V can be expressed in the form
              v = c1v1 + c2v2 + ... +cnvn
         in EXACTLY ONE way
         
### 5. Definition 4.4.2 Coordinates and Coordinate Vector
       - If B = {v1, v2, ... , vn} is a basis for a vector spoace V
       - And v = c1v1 + c2v2 + ... +cnvn
       - the SCALARS c1, c2, ..., cn are the COORDINATES of v RELATIVE TO B
       - The vector [v]_B = (c1, c2, ..., cn) in R^n is the COORDINATE VECTOR of v RELATIVE TO B
       
### 6. Definition 4.4.6 The Change-of-Basis Matrix from B to B'
       - B = {u1, u2, ..., un}
       - B' = {u1', u2', ..., un'}
       - P_(B -> B') = [[u1]_B', [u2]_B', ..., [un]_B']
       - Where this notation stands for the n * n matrix, 
         whose columns are the col vectors [u1]_B', [u2]_B', ..., [un]_B'
       - The columns of the Change-of-Basis Matrix from an old basi to a new basis
         are the coordinate vectors of the old basis relative to the new
         
### 7. Theorem 4.4.7 Coordinate Vector Under Change-of-Basis
       - Let V be a vector space with bases B and B'
       - Then for any v in V we have: [v]_B' = P_(B -> B')* [v]_B
       
       
## Lecture 2

### 1. Theorem 4.4.8 Transition Matrix & Inverse
       - If P_(B -> B') is a transition matrix, then it is Invertible
       - [P_(B -> B')] ^ (-1) = P_(B' -> B)
       
### 2. Remark 4.4.9 Standard Basis B and Use of Theorem 4.4.8
       - If B is one of the standard bases
       - Then it is easy to find P_(B' -> B)
       - Theorem 4.4.8 can then be used to find P_(B -> B')
       
### 3. E.g. 4.4.10: Example of 4.4.9
       - B = {1, x, x^2}
       - B' = {1+x, 2x, 3x^2}
       - P_(B' -> B): COL_1 = [1 1 0], COL_2 = [0 2 0], COL_3 = [0 0 3]
       - P_(B -> B') = [P_(B' -> B)] ^ (-1): ROW_1 = [1 0 0], ROW_2 = [-1/2 1/2 0], ROW_3 = [0 0 1/3]
       
## Chapter 4.5 Row, Column & Null Space

### 4. Let A be an m * n matrix
       - Def 4.5.1 Row Space: denoted by row(A), is the subspace of R^n spanned by the rows of A
       - Def 4.5.2 Col Space: denoted by col(A), is the subspace of R^m spanned by the cols of A
       - Def 4.5.3 Null Space: denoted by null(A), is the set of all solutions x in R^n of homogeneous equation Ax = 0
       
### 5. Theorem 4.5.4: The Null Space of an m * n matrix is a subspace of R^n


### 6. Theorem 4.5.5: A Linear System Ax = b is Consistent IFF b in col(A)

### 7. Theorem 4.5.7: Matrix and Row Equivalent (After Row Operations)
       - Let A be an m * n matrix and let U be row equivalent to A
       - row(A) = row(U)
       - null(A) = null(U)
       

## Lecture 3

### 1. E.g. 4.5.8: 3 * 4 Matrix A and the Row Equivalent Matrix U
       - A: Row_1 = [2 -1 1 2], Row_2 = [-8 4 -6 -4], Row_3 = [4 -2 3 2]
       - U: Row_1 = [2 -1 1 2], Row_2 = [0 0 -2 4], Row_3 = [0 0 0 0]
       - Find the BASEs for row(A) and null(A)
       - Theorem 4.5.7 --> row(A) = row(U)
         1. The two nonzero rows span row(U)
         2. Linearly Independent: c1 * (2, -1, 1, 2) + c2 * (0, 0, -2, 4) = 0 <=> c1 = c2 = 0
         3. Based on 1 & 2, c1&c2 is a basis for row(U)/row(A)
       - Theorem 4.5.7 --> null(A) = null(U)
         1. Solve Ux = 0 by Back Substitution, set free vars x2 = a & x4 = b
         2. Can get x1 = (-1/2)a - 2b and x3 = 2b
         3. x = a * Col_Vec_[-1/2 1 0 0] + b * Col_Vec_[-2 0 2 1]
         4. null(u) = span(Col_Vec_[-1/2 1 0 0], Col_Vec_[-2 0 2 1])
         5. Col_Vec_[-1/2 1 0 0] and Col_Vec_[-2 0 2 1] is Linearly Independent
         6. Set {Col_Vec_[-1/2 1 0 0], Col_Vec_[-2 0 2 1]} iis a basis for null(U)/ null(A)
         
### 2. Theorem 4.5.9: A - m * n Matrix, U - Row Equivalent Echelon Matrix with r Pivots
       - A basis for the Row Space of A is the set of nonzero rows of U
       - A basis for the Col Space of A is the set of Pivot Columns of A (Columns giving rise to a pivot in U)
       - Solving the system Ax = 0 we find n - r free variables 
         and can write the general solution in the form: x = a1v1 + a2v2 + ... + a_(n-r) * v_(n-r)
         where a1, a2, ..., a_(n-r) are arbitrary constants
       - If r < n, a basis for the null(A) is {v1, v2, ..., v_(n-r)}
       - If r = n, then null(A) = {0}, which has no basis
       

## Chapter 4.6: Rank and Nullity

### 3. Remark 4.6.1: It follows from Theorem 4.5.9 that the num of pivots r, NOT depend on the particular choice of U

### 4. Definitions: Rank, Nullity, Cokernel, Kernel
       - Def 4.6.2 Rank: Num of Pivots r in an echelon form of a matrix A
       - Def 4.6.3 Nullity: Dimension n - r of the null space of a matrix A
       - Def 4.6.4 Cokernel: coker(A) = null(A^T)
       - Def 4.6.4: Kernel: ker(A) := nulll(A)
 
### 5. Theorem 4.6.5: Fundamental Theorem of Linear Algebra, A = m * n of rank r
       - dim(row(A)) = r
       - dim(col(A)) = r
       - dim(ker(A)) = n - r = nullity(A)
       - dim(coker(A)) = m - r = nullity(A^T)
       - For ANY matrix, the num of Linearly Independent Cols = the num of Linearly Independent Rows
       
### 6. 
         
       



















## Lecture 1
### 1. Linear system has more than one solution == has infinitely many solutions
### 2. Consistent: at least one solution(one or infinitely many)
### 3. Inconsistent: NO solution
### 4. Elementary Row operations
       - Multiple one row by non-zero
       - Interchange two rows
       - Add a multiple of one row to another
### 5. Row Echelon Form
       - Any zero rows at the bottom
       - First non-zero entry in each non-zero row(PIVOT) is to the right of pivots in the rows above
### 6. Reduced Row Echelon Form
       - Row Echelon Form
       - Each pivot is 1
       - Each pivot is the only non-zero entry in its COLUMN
       
## Lecture 2
### 1. Echelon Form of a given matrix is NOT Unique
### 2. Reduced Echelon form of a given matrix is UNIQUE
### 3. Leading Variables: Number of COLs containing pivots
### 4. Free Variables: Number of COLs NOT contaning pivots 
### 5. Number of Solutions of Ax = b determined by [U|c] (Echelon Form)
       - NO Solution: Last non-zero row of [U|c] is [0 0 ... 0 0 | c] with c $\neq$ 0
       - Infinitely Many Solutions: Consistent with Free variables
       - Exactly: Consistent and NO Free variables
### 6. Theorem 1.2.8: Consider a linear system of m equations in n vars with r pivots
       - r = n: Either NO or Exactly solutions
       - r < n: Either NO or Infinitely Many Solutions
       - n > m: Either No or Infinitely Many Solutions
       
## Lecture 3
### 1. Homogeneous: A linear system is of the form: Ax = 0
### 2. Theorem 1.2.11: For any homogeneous linear system
       - The system is consistent
       - If more variables than equations, then there are infinitely many solutions
### 3. Theorem 1.2.12: Suppose Ax = b is consistent and P is a solution
       - Then every solutions of Ax = b can be written as x = P + Z
       - Where Z is a solution of the associated homogeneous system Ax = 0
### 4. Basics of matrix
       - A: m * r, B: r * n, AB: m * n, (AB)_ij = \sum_{k=1}^r A_ik * B_kj
       - Square matrix A is SYMMETRIC if A^T = A
       - TRACE of a n*n matrix is the sum of the elements on its main disgonal: tr(A) = $\sigma${i=1}^n A_ii
       - Two matrices are said to be commute if AB = BA
       - Upper Triangular: Square matrix U if U_ij = 0 for any i > j
       - Lower Triangular: Square matrix U if U_ij = 0 for any i < j
### 5. Theorem 1.3.9
       - Product of two lower triangular matrices: lower triangular matrix
       - Product of two upper triangular matrices: upper triangular matrix


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
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         
         

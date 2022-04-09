## Equivalent Statements in terms of SPAN
   - Let S = {w1, w2, ... wr} be a nonempty subset of a vector space V
   - If W is the set of all possible linear combinations of the vectors in S, then
   - W is a subspace of V
   - W is the smallest subspace that contains S
   - W is the SPAN of S, i.e., W = SPAN(S)
   - S Spans W
   - S is the Spanning Set of W

## Lecture 1

### 1. Subspace Examples
       - The Zero Subspace W = {0}
       - Any line through the origin in R^d
       - Planes through the origin in R^d with d >= 2
       - The set of all 2*2 symmetric matrices (A = A^T) is a subspace of M_22
       - P_n is a subspace of P_(infinite sign)
       
### 2. Theorem 4.1.9: Any subspace W of Vector Space V contains the Zero Vector of V

### 3. Definition 4.2.1: Linear Combination
       - A vector v is a linear combination of the vectors w1, w2, ... wr 
       - IF it can be expressed in the form v = k1w1 + k2w2 + ... + krwr
       - for some scalars k1, k2, ... kr, which are coefficients
       
### 4. Theorem 4.2.2: Subset and Scalars
       - Let S = {w1, w2, ... wr} be a nonempty subset of a vector space V
       - Then for any choice a1, a2, ... ar and b1, b2, ... br and b
       - sum of ai*wi is in V
       - (sum of ai*wi) + (sum of bi*wi) is in V
       - B * (sum of ai*wi) = sum of ((B * ai) * wi)
       
### 5. Theorem 4.2.3: Subset, Linear Combinations, Subspace
       - Let S = {w1, w2, ... wr} be a nonempty subset of a vector space V
       - If W is the set of all possible linear combinations of the vectors in S, then
       - W is a subspace of V
       - W is the smallest subspace that contains S
       
### 6. Definition of SPAN
       - Let S = {w1, w2, ... wr} be a nonempty subset of a vector space V
       - The subspace W is of all possible linear combinations of vectors in S
       - W is the SPAN of S, i.e., W = SPAN(S)
       - S Spans W
       - e.g., The span of {1, x, x^2} is P_2, P_2 = span({1, x, x^2})
       - e.g., The set {e1, e2} spans R^2
       

## Lecture 2

### 1. Definition 4.2.6: Linearly Independent
       - A set {v1, v2, ... vn} of vectors is called linearly independent 
       - IFF the only solution to k1v1 + k2v2 + ... knvn = 0 
       - IS the Trivial Solution: k1 = k2 = ... = kn = 0

### 2. Theorem 4.2.8: Linearly Independent & Linear Combination
       - A set S with at least two vectors is
       - Linearly Independent IFF NO Vector in S can be expressed as a linear combination of other vectors in S
       - Liearly Dependent IFF AT LEAST ONE Vector can be expressed as a linear combination of other vectors in S
       
### 3. Whether vectors spans R^n: depends on whether related matrix A is invertible/det(A) != 0, then Ax = b for any b in R^n

### 4. Definition 4.3.1: Basic
       - A set S = {v1, v2, ... vn} of vectors in a vector space V is called a basic for V
       - If S is linearly independent AND S Spans V
       
### 5. Definitions in Conslusion
       - Subset: contains some/zero elements of a set
       - Subspace: non-empty subset of a vector space, closed under same + and scalar x
       - Span: A subspace W of V is the span of a subset S of V, or to say, S spans W, W = span(S)
               if it contains all possible linear combinations of vectors in S. 
               Meanwhile, it is the SMALLEST Subspace in V that contains S
       - Linearly Independent: == 0 has only the trivial solution
       - Basis: A subset S that spans W and is linearly independent
       
### 6. Examples of Standard Basis
       - The set {e1, e2, ... en} is the standard basis for R^n
       - The set {1, x, x^2, .. x^n} is the standard basis for P_n
       - The set {[1 0 / 0 0], [0 1 / 0 0] [0 0 / 1 0], [0 0 / 0 1]} is the standard basis for M_22
       

## Lecture 3

### 1. Definition 4.3.7: Finite Dimensional
       - A vector is said to be finite dimensional if it can be spanned by finitely mant vectors
       
### 2. Theorem 4.3.8: Finite Dimensional Vector Space & Its Basis
       - Let V be a finite dimensional vector space and B = {v1, v2, ... vn} is a basis of it
       - If subset S of V has more than n vectors, then S is NOT Linearly Independent
       - If subset S of V has less than n vectors, then S can NOT Span V
       
### 3. Theorem 4.3.9 Dimensional Theorem
       - Let V be a finite dimensional vector space
       - EVERY Basis of V contains the SAME NUM of Vectors
       
### 4. Definition 4.3.10: Dimension of a Finite Dimensional Vector Space V
       - Denoted by dim(V)
       - The num of vectors in its basis
       - The dimension of the zero space is 0

### 5. Examples of Dimensions
       - dim(R^n) = n
       - dim(P_n) = n + 1
       - dim(M_mn) = m * n

### 6. Theorem 4.3.12: Span(S) & Linearly Independent
       - Let S be a nonempry subset of vectors in a vector space V
       - If S is linearly independent and if v in V not in span(S), then the set (S and {v}) is linearly independent
       - If v in S can be expressed as a linear combination of the other vectors in S, 
         then span(S / {v})= span(S)
  

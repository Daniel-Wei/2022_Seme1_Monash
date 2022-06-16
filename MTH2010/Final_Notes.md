# Topics

#### 1. Level Curves: how to draw and interpret them
#### 2. Check whether the limit exists or not
#### 3. Check the differentiability of multivariable functions
#### 4. Finding the normal vector and the tangent plane of surfaces
#### 5. Polar coordinate and integration
#### 6. Cylindrical coordinate and integration
#### 7. Spherical coordinate and integration
#### 8. Line integrals, work done by a force field, and conservative Vector Field
#### 9. Finding critical points and the minimum.
#### 10. Properties of gradient and the Lagrange multiplier method
#### 11. Jacobian and the change of variables for a multivariable function.
#### 12. Fubini theorem
#### 13. Finding the total charge on a surface
#### 14. Green's Theorem
#### 15. Stoke's theorem
#### 16. Divergence theorem


## Own Summary 

#### 2. Check whether the limit exists or not
* (x, y) |-> (0, 0): Check whether the limits of (t, 0) |-> (0, 0) and (0, t) |-> (0, 0) are the same
* (x, y) |-> (a, b): Dominator at (a, b) != 0, while both the numerator and dominator are polynomials, so limit of f(x, y) at (a, b) is f(a, b)
* (x, y) |-> (a, b): Dominator at (a, b) == 0, but numerator could factorises at other points, do the factorization and get g(x, y). Limit of f(x, y) at (a, b) is g(a, b)
* Squeeze Theorem: 0 <= |f(x, y) - L| <= g(x, y) |-> 0: |x| / |y| <= sqar root of (x^2 + y^2)
* Continuity: f(x, y) is continuous at (a, b) IFF limit of f(x, y) at (a, b) == f(a, b)


#### 3. Check the differentiability of multivariable functions
* Linearization of f(x, y) at (x0, y0): L(x, y) = f(x0, y0) + f_x(x0, y0) * (x - x0) + f_y(x0, y0) * (y - y0)
* Relative Error of f(x, y) at (x0, y0): |f(x, y) - L(x, y)| / |(x, y) - (x0, y0)|
* Differentiability of f(x, y) at (x0, y0): Limit of Relative Error = 0 when (x, y) |-> (x0, y0)


#### 4. Finding the normal vector and the tangent plane of surfaces
* Implicit Differentiation_1: F(x, y) == 0 --> dy/dx = -Fx/Fy
* Implicit Differentiation_2: For x^2 - y^2 + z^2 - 2z = 4, use implicit differentiation to find dz/dy: treant x like a constant and z like a function of y, then partially differentiate both sides of the given equation with respect to y
* Implicit Differentiation_3: check the existentce of f(x) such that f(2) = -2 and F(x, f(x)) == 0: F(2, -2) == 0 and F_y(2, -2) != 0
* Gradient of a differential f(x, y) at (x0, y0) is (f_x(x0, y0), f_y(x0, y0))
* Directional Derivative of a differential f(x, y) at (x0, y0) in the direction of vector u is: (unit vector of u) * gredient of f(x, y) at (x0, y0)
* Important Fact: If f(x, y) is differentiable at (x0, y0) and its gradient at (x0, y0) != 0, then its gradient at (x0, y0) is orthogonal to the level curve of f(x, y) that passes through the point (x0, y0)
* Find the vector tangent to the curve of the intersection of two functions at the point (x0, y0, z0): n1 x n2, where n1, n2 are the gradients of f1, f2 at (x0, y0, z0)


#### 4'. Maximum & Minimum Values
* Classifying Critical Points of f(x, y) at (a, b)
..* f(x, y) is C^2 on Ball(a, b)

* If D in R^2, Closed & Bounded, f(x, y) is con

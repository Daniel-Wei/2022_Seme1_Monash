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
* (x, y) |-> (a, b)
  - Dominator at (a, b) != 0, while both the numerator and dominator are polynomials, so limit of f(x, y) at (a, b) is f(a, b)
  - Dominator at (a, b) == 0, but numerator could factorises at other points, do the factorization and get g(x, y). Limit of f(x, y) at (a, b) is g(a, b)

* Squeeze Theorem: 0 <= |f(x, y) - L| <= g(x, y) |-> 0: |x| / |y| <= sqar root of (x^2 + y^2)

* Continuity: f(x, y) is continuous at (a, b) IFF limit of f(x, y) at (a, b) == f(a, b)


#### 3. Check the differentiability of multivariable functions
* Linearization of f(x, y) at (x0, y0): L(x, y) = f(x0, y0) + f_x(x0, y0) * (x - x0) + f_y(x0, y0) * (y - y0)
* Relative Error of f(x, y) at (x0, y0): |f(x, y) - L(x, y)| / |(x, y) - (x0, y0)|
* Differentiability of f(x, y) at (x0, y0): Limit of Relative Error = 0 when (x, y) |-> (x0, y0)


#### 4. Finding the normal vector and the tangent plane of surfaces
* Normal Vector to the Tangent Plane of Surfaces: (-f_x, f_y, 1)
* Algebraic Representation of a Tangent Plane of Surfaces at point (x0, y0, f(x0, y0))
  - f_x(x0, y0) * (x - x0) + f_y(x0, y0) * (y - y0) + (z - f(x0, y0)) = 0


#### 5. Polar coordinate and integration
* Jacobian for Polar Coordinates: r. J(T) > 0 as r > 0

* x = r * cos(theta), y = r * sin(theta)

* Area Element = Integral of r drd(theta) on the region T(D)
  - 4 Leaved Rose r = abs(cos(2*theta))
  - Integral of <-pi/4, pi/4> <0, cos(2 * theta)> r drd(theta)
  - cos(2* theta) = (1 + cos(4 * theta)) / 2

* When to use Polar Coordinates for Integration
  - Simplifies the Domian of Integration: e.g., D is the region in the 1st quadrant being inside the disk x^2 + y^2 <= a^2 and under the line y = x
  - Simplifies the Function being Integrated: e.g., f(x, y) = ln(x^2 + y^2 + 1)


#### 9. Finding critical points and the minimum.
* Classifying Critical Points of f(x, y) at (a, b)

  - f(x, y) is C^2 on Ball(a, b)
  - Gradient of f(x, y) at (a, b) is 0
  - A = f_xx(a, b), B = f_xy = f_yx(a, b), C = f_yy(a, b)
  - Local Min: AC > B^2 & A > 0
  - Local Max: AC > B^2 & A < 0
  - Saddle Point: AC < B^2
  - No Info: AC = B^2

* Absolute Maxima & Minima

  - D is in R^2, Closed & Bounded
  - f(x, y) is continuous on D
  - Then there exist points where f(x, y) achieves an abs maxima/minima on D


#### 10. Properties of gradient and the Lagrange multiplier method
* Implicit Differentiation 
  - F(x, y) == 0 --> dy/dx = -Fx/Fy
  - For x^2 - y^2 + z^2 - 2z = 4, use implicit differentiation to find dz/dy: treant x like a constant and z like a function of y, then partially differentiate both sides of the given equation with respect to y
  - check the existentce of f(x) such that f(2) = -2 and F(x, f(x)) == 0: F(2, -2) == 0 and F_y(2, -2) != 0
  
* Gradient of a differential f(x, y) at (x0, y0) is (f_x(x0, y0), f_y(x0, y0))

* Directional Derivative of a differential f(x, y) at (x0, y0) in the direction of vector u is: (unit vector of u) * gredient of f(x, y) at (x0, y0)

* Important Fact: If f(x, y) is differentiable at (x0, y0) and its gradient at (x0, y0) != 0, then its gradient at (x0, y0) is orthogonal to the level curve of f(x, y) that passes through the point (x0, y0)

* Find the vector tangent to the curve of the intersection of two functions at the point (x0, y0, z0): n1 x n2, where n1, n2 are the gradients of f1, f2 at (x0, y0, z0)

* Lagrange Multiplies
  - Determine the abs extrema of f(x, y) subject to a constraint g(x, y) = 0
  - Find all values for {f_x = k * g_x, f_y = k * g_y, g(x, y) = 0}


#### 11. Jacobian and the change of variables for a multivariable function.
* Jacobian of a Differentiable Map
  - F: D in R^2 |-> R^2: (u, v) |-> f(u, v) = (f1(u, v), f2(u, v))
  - J(f) = f1_u * f2_v - f1_v * f2_u

* Area Element
  - Area(T(R)) = |J(T)(u0, v0) * delta(u) * delta(v)|

* Change of Variables Formula
  - Intergral of f(x, y) dxdy on the region T(D) = integral of f(T(u, v)) * |J(T) (u, v)| dudv on the region D 
  - T: D -> R^2: (u, v) |-> T(u, v) = (T1(u, v), T2(u, v))


#### 12. Fubini theorem
* Simplest Region in R^2 is bothe x-simple & y-simple
* Integral of f(x, y) on dA = f(x, y) dxdy = f(x, y) dydx <Free to Change the Integral Calculation Order> 
  
#### 13. Finding the total charge on a surface
* Mass Density: p(x, y)

* Mass = integral of p(x, y) dA on the region D
  - Mass Region = [ (Min p(x, y) on D) * Area(D), (Max p(x, y) on D) * Area(D) ]

* Centre of Mass: (x', y') 
  - x' = (1 / m) * integral of x * p(x, y) dA on the region D
  - y' = (1 / m) * integral of y * p(x, y) dA on the region D

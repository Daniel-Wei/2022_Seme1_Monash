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


#### 6. Cylindrical coordinate and integration
* x = r * (cos(theta)), y = r * (sin(theta)), z = z

* Theta: Closewise Angle to X - axis

* Volume Element 
  - integral of dV on the region D
  - integral of r drd(theta)dz on the region T(D)

* Integration Formula
  - integral of f(x, y, z) dV on the region T(E)
  - integral of f(T(r, theta, z)) r drd(theta)dz on the region E
  - T(r, theta, z) = (r * (cos(theta)), r * (sin(theta)), z)
  - |J(T)| = r

#### 7. Spherical coordinate and integration
* x = p * sin(Psi) * cos(theta), y = p * sin(Psi) * sin(theta), z = cos(Psi)

* Angle Theta
  - image in the x-y plane, at the anticlosewise angle to X - axis
  - Range: [0, 2 * pi]

* Angle Psi
  - Rotation angle to Z - axis
  - Range: [0, pi]

* Length p
  - Distance to the origin (0, 0)
  - Range: [0, +inf]

* Volume Element 
  - integral of dV on the region D
  - integral of p^2 * sin(Psi) dpd(theta)d(psi) on the region T(D)

* Integration Formula
  - integral of f(x, y, z) dV on the region T(E)
  - integral of f(T(p, Psi, Theta)) p^2 * sin(Psi) dpd(theta)d(psi) on the region E
  - T(r, theta, z) = (p * sin(Psi) * cos(theta), p * sin(Psi) * sin(theta), cos(Psi))
  - |J(T)| = p^2 * sin(Psi)


#### 8. Line integrals, work done by a force field, and conservative Vector Field
* Vector Field: map F
  - On region D in R^2: F: D in R^2 |-> R^2: (x, y) |-> F(x, y) = (F_1(x, y), F_2(x, y))
  - On region E in R^3: F: E in R^3 |-> R^3: (x, y, z) |-> F(x, y, z) = (F_1(x, y, z), F_2(x, y, z), F_3(x, y, z))

* Conservative Vector Field F
  - exist f: E -> R such that F = gradient of f
  - NOT every vector field F is conservative
  - Condition 1: 
    - in R^2: F = (F_1, F_2) & F1_y = F2_x
    - in R^3: F = (F_1, F_2, F_3) & F1_y = F2_x, F1_z = F3_x, F2_z = F3_y
  - Condition 2: Region D/E has no holes
 
* Length of Curves in R^2
  - The Length of a C^1 parametric curve that is parameterized by r(t) = (x(t), y(t))
  - Range of t: [a, b]
  - Curve Length e = integral of [a, b] | (d(r(t))) / (dt) | dt
    - => integral of [a, b] (square root of ((dx/dt)^2 + (dy/dt)^2)) dt

* Line Integrals in R^2
  - Function along Parametric Curve
    - The line integral of a C^0 function f(x, y) along a C^1 parametric curve t 
    - t is a curve parametrized by r(t) = (x(t), y(t)), t in [a, b]
    - integral of f(x, y) dS on C = integral of f(r(t)) * |(dr) / d(t)| dt on [a, b]
    - dS is the length element
    - => integral of f(x(t), y(t)) * (square root of ((dx/dt)^2 + (dy/dt)^2)) dt on [a, b]
  
  - Orientation & Representation
    - A parametrization r(t) = (x(t), y(t)), t in [a, b] of a curve defines an orientation of the curve
    - By Assigning a direction to it given by the motion(移动) of r(t) increases as t increases
    - Opposite Reverse Orientation of r(t): r'(t) = r(b - (t-a))
    - Line integrals of r(t) and r'(t) on the same line & same t range are SAME
    - Line integrals of (integral of (f dS) in C) and (integral of (f dS) in -C) are OPPOSITE

  - Along Piecewise Curves
    - C is a curve that can be decomposed into a disgoint union
    - Line integral of integral of (f dS) on C = sum of (i in [1, n]) of (integral of (f dS) on C_i)

  - Of Vector Fields in R^2
    - Line integral of a C^0 vector field along a C^1 parametric curve C
    - r(t) = (x(t), y(t))
    - F = (p(x,y), q(x, y))
    - t in [a, b]
    - Line integral = integral of (F dr) on curve C = integral of (F TdS) on curve C
    - T = (1 / (|dr / dt|)) * (dr / dt), dS = (|dr / dt| ) * dt
    - => integral of (F TdS) on curve C = integral of (F * (dr / dt) dt) on t range [a, b]
    - => integral of (p(x(t), y(t)) (dx/dt) dt) on [a, b] + integral of (q(x(t), y(t)) (dy/dt) dt) on [a, b]

    - The Work done by a force field F(x, y) = (F_1(x, y), F_2(x, y)) in moving an object along a curve C: W = integral of (F dr) on curve C
    - Opposite orientation of r(t) has Opposite work done

* Line Integrals in R^3
  - C is a C^1 Curve parameterized by r(t) = (x(t), y(t), z(t)), t in [a, b]
  - Length of Curves
    - Length(C) = integral of ds on Curve C
    - == integral of | (dr) / (ds) | * dt on [a, b]
    - == Integral of (square root of ( (dx/dt) ^ 2 + (dy/dt) ^ 2 + (dz/dt) ^ 2 ) ) * dt on [a, b]
  - Line Integrals of Functions
    - Line Integral of f(x, y, z) along C == Integral of f dS on Curve c
    - == Integral of f(r(t)) * | dr / dt | dt on [a, b]
    - == Integral of f(x(t), y(t), z(t)) * (square root of ( (dx/dt) ^ 2 + (dy/dt) ^ 2 + (dz/dt) ^ 2 ) ) * dt on [a, b]
  - Line Integrals of Vector Fields
    - F(x, y, z) = (P(x, y, z), Q(x, y, z), R(x, y, z))
    - Integral of F dr on Curve C = Integral of F(r(t)) * (dr/dt) dt on [a, b]
    - == Integral of Pdx + Qdy + Rdz on Curve C
    - == Integral of P dx/dt + Q dy/dt + R dz/dt on [a, b]

* Fundamental Theorem for Line Integrals: For Conservative Vector Fields
  - Suppose C is a C^1 Curve that is parameterized by r(t)
  - t in [a. b]
  - f is a C^1 Function on C
  - Integral of gradient of f dr on Curve C = f(r(b)) - f(r(a))

* Path Independance Theorem
  - Path Connected
    - An Open Set U in R^n is called path connected
    - IF for every points p, q in U, there exists a piecewise C^1 Curve C that connects p to q
    - That is, if r(t), t in [a, b], IS a Parameterization of C 
    - Then r(a) = p, r(b) = q
  
  - Let D in R^2 or R^3 be an open and path connected set and F is a C^0 vector field on D, then the following statements are equivalent
    - F is conservative in D
    - Integral of F dr on C is 0, for every closed, piecewise C^1 Curve C that lies in D
    - For any two piceswise C^1 curve C1 and C2 that connects p to q, p & q in D, Integral of F dr on C1 == Integrla of F dr on C2 

  - Application - Show Line Integral of a Vector Field is Path Independent: Show the Vector Field is Conservative, aka, find its antiderivative

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
  
* Example: Integral of [0, pi] [0, 2 * pi] [0, 1] e^(p^3) * p^2 * sin(Psi) dpd(theta)d(Psi)
  - => [Integral of [0, 1] e^(p^3) * p^2] * [Integral of [0, 2 * pi] 1 d(theta)] * [Integral of [0, pi] sin(Psi) d(Psi)] 
  - => ((1/3) * (e - 1)) * (2 * pi) * 2
  
#### 13. Finding the total charge on a surface
* Mass Density: p(x, y)

* Mass = integral of p(x, y) dA on the region D
  - Mass Region = [ (Min p(x, y) on D) * Area(D), (Max p(x, y) on D) * Area(D) ]

* Centre of Mass: (x', y') 
  - x' = (1 / m) * integral of x * p(x, y) dA on the region D
  - y' = (1 / m) * integral of y * p(x, y) dA on the region D
  
#### 14. Green's Theorem
* Integral of F dr on Curve C = Integral of Pdx + Qdy on C = Double Integral of (dQ/dx - dP/dy) dA on D
  - Curve C is a Closed, Simple, Positive(Anticlockwise) Oriented Curve in R^2
  - D is the Region Enclosed by Curve C
  - F = (P, Q) is a C^1 Vector Field defined in the Region D U C (Area U Boundary)
  
* Simple Curve: No Intersecrions between its end points
  
* Area(D) = (1/2) * Integral of (xdy - ydx) on C
  
* Non-Simple Connected Ones: Line Integral of F dr on (C1 U C2) = curl(F) dA on D
  - C1, outer boundary, positive(anticlockwise) oriented
  - C2, inner boundary, negative(clockwise) oriented
  
* Test for Conservative Vector Fields on R^2
  - Suppose F(x, y) = (P(x, y), Q(x, y)) is a C^1 vector field on an Open & Simply Connected domain(NO Holes) D in R^2
  - dP/dy = dQ/dx <=> curl F = 0 in D <=> F is Conservative 
  
  - If D is NOT Simply Connected, then dP/dy == dQ/dx NOT Necesserily imply that F is Conservative
  

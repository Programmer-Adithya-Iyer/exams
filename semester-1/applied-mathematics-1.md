# 📘 Complete Formula Bank – Advanced Calculus & Linear Algebra

---

## 1. Differential Calculus
- **Partial Derivatives**: ∂f/∂x , ∂f/∂y
- **Chain Rule**: dz/dt = (∂z/∂x)(dx/dt) + (∂z/∂y)(dy/dt)
- **Implicit Differentiation**: dy/dx = -Fx/Fy
- **Exact Differentials**: ∂M/∂y = ∂N/∂x
- **Hessian Determinant**: H = | fxx  fxy |  
                             | fyx  fyy |
- **Lagrange Multipliers**: ∇f = λ∇g

---

## 2. Differentiation Under Integral Sign
- **Leibniz Rule**:  
  d/dx ∫[a(x) → b(x)] f(t,x) dt  
  = f(b(x),x)·b'(x) - f(a(x),x)·a'(x) + ∫[a(x) → b(x)] ∂f/∂x (t,x) dt

---

## 3. Jacobian & Coordinate Transformations
- **Jacobian Determinant**:  
  J = ∂(x,y)/∂(u,v) =  
  | ∂x/∂u   ∂x/∂v |  
  | ∂y/∂u   ∂y/∂v |

---

## 4. Ordinary Differential Equations (ODEs)
- **Euler’s Method**: y_{n+1} = y_n + h f(x_n,y_n)
- **Separable ODEs**: ∫ dy/h(y) = ∫ g(x) dx
- **Exact ODEs**: M dx + N dy = 0, with ∂M/∂y = ∂N/∂x
- **Integrating Factor**: μ(x) = e^(∫P(x) dx)
- **Bernoulli Equation**: dy/dx + P(x)y = Q(x)y^n
- **Homogeneous Linear ODEs**: ay'' + by' + cy = 0 → ar² + br + c = 0
- **Euler–Cauchy Equation**: x²y'' + axy' + by = 0
- **Wronskian**: W(y1,y2) = y1y2' - y2y1'
- **Variation of Parameters**: y_p = u1y1 + u2y2
- **Mass–Spring Oscillations**: mẍ + kx = 0 → ω = √(k/m)

---

## 5. Special Functions
- **Gamma Function**: Γ(n) = ∫₀^∞ x^(n-1) e^(-x) dx ; Γ(n+1) = nΓ(n)
- **Beta Function**: B(m,n) = ∫₀^1 x^(m-1)(1-x)^(n-1) dx ; B(m,n) = Γ(m)Γ(n)/Γ(m+n)
- **Bessel Function**: J_n(x) = Σ [(-1)^k / (k! Γ(n+k+1))] (x/2)^(2k+n)
- **Legendre Polynomial**: P_n(x) = (1/2^n)(d^n/dx^n)(x²-1)^n
- **Hermite Polynomial**: H_n(x) = (-1)^n e^(x²) (d^n/dx^n)(e^(-x²))
- **Laguerre Polynomial**: L_n(x) = e^x/n! (d^n/dx^n)(x^n e^(-x))

---

## 6. Linear Algebra
- **Determinant (2×2)**: |a  b| |c  d| = ad - bc
- **Cramer’s Rule**: xi = det(Ai)/det(A)
- **Rank**: Number of non-zero rows in row-reduced form
- **Eigenvalue Equation**: det(A - λI) = 0
- **Eigenvector**: (A - λI)x = 0
- **Orthogonal Matrix**: AᵀA = I
- **Quadratic Form**: Q(x) = xᵀAx
- **Canonical Form (Quadratic)**: Diagonalize A → Q(x) = Σ λi yi²

---

## 7. Vector Calculus
- **Gradient**: ∇f = (∂f/∂x, ∂f/∂y, ∂f/∂z)
- **Divergence**: ∇·F = ∂Fx/∂x + ∂Fy/∂y + ∂Fz/∂z
- **Curl**: ∇×F = | i   j   k |  
                   | ∂/∂x ∂/∂y ∂/∂z |  
                   | Fx   Fy   Fz |
- **Line Integral**: ∫C F·dr
- **Double Integral**: ∬R f(x,y) dA
- **Triple Integral**: ∭V f(x,y,z) dV
- **Green’s Theorem**: ∮C (M dx + N dy) = ∬R (∂N/∂x - ∂M/∂y) dA
- **Stokes’ Theorem**: ∮C F·dr = ∬S (∇×F)·n dS
- **Gauss Divergence Theorem**: ∬S F·n dS = ∭V (∇·F) dV

---

## 8. Curvature & Torsion (Differential Geometry)
- **Curvature (κ)**:  
  κ = |dT/ds| = |r'(t) × r''(t)| / |r'(t)|³
- **Radius of Curvature (ρ)**:  
  ρ = 1/κ
- **Torsion (τ)**:  
  τ = ( (r'(t) × r''(t)) · r'''(t) ) / |r'(t) × r''(t)|²
- **Frenet–Serret Formulas**:  
  dT/ds = κN  
  dN/ds = -κT + τB  
  dB/ds = -τN

---

## 9. Leftover Topics (from your list)
- **Orthogonal Trajectories**: slope m₁·m₂ = -1
- **Population Dynamics (Logistic Growth)**:  
  dy/dt = ry(1 - y/K)
- **Direction Fields**: slope = f(x,y)
- **Power Series Method (ODEs)**:  
  y(x) = Σ a_n x^n
- **Recurrence Relations (General)**:  
  a_{n+1} = f(n, a_n, a_{n-1}, …)

---

# ⚡ Quick Recall Table

| Topic              | Formula |
|--------------------|---------|
| Curvature κ        | |r'(t) × r''(t)| / |r'(t)|³ |
| Torsion τ          | ((r'×r'')·r''') / |r'×r''|² |
| Radius of Curvature| ρ = 1/κ |
| Frenet–Serret      | dT/ds = κN ; dN/ds = -κT+τB ; dB/ds = -τN |
| Logistic Growth    | dy/dt = ry(1 - y/K) |
| Eigenvalue Eqn     | det(A - λI) = 0 |
| Gamma Function     | Γ(n) = ∫₀^∞ x^(n-1)e^(-x) dx |
| Beta Function      | B(m,n) = Γ(m)Γ(n)/Γ(m+n) |
| Green’s Theorem    | ∮C (M dx + N dy) = ∬R (∂N/∂x - ∂M/∂y) dA |
| Stokes’ Theorem    | ∮C F·dr = ∬S (∇×F)·n dS |
| Gauss Theorem      | ∬S F·n dS = ∭V (∇·F) dV |

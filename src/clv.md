# Covariant Lyapunov Vector

Equation of motion
\\[
x_{m+1} = F(x_m)
\\]
We denote an invariant set of this equation by \\(M\\) and its tangent space at \\(x_m\\) by \\(T_m M\\).
QR-decomposition of the Jacobian of \\(F\\) at the state \\(x_m\\)
\\[
J_m Q_m = Q_{m+1} R_{m+1},
\\]
with \\(Q_0\\) is set to an identity matrix \\(I\\).
We can calculate the Lyapunov exponent from this forward iteration:
\\[
\lambda_i = \lim_{m \to \infty} \frac{1}{m} \sum_{n=1}^m \log {\left(R_n\right)}_{ii}
\\]
The definition of the \\(i\\)-th covariant Lyapunov vector \\(v^i_m \in T_m M\\) is following two conditions:

- Jacobian-invariant \\[ J_m v_m^i = d_m^i v_{m+1}^i \\] where \\(d_m^i\\) is a scalar value, and normalized \\(\| v_m^i \| = 1\\).
- Asymptotic growth rate equals to the Lyapunov exponent \\[ \lambda_i = \lim_{m \to \infty} \frac{1}{m} \log \| J_{m-1} J_{m-2} \ldots J_0 v_0^i \| \\]

Consider a subspace of \\(T_m M\\),  \\(U_m^l = \Span \{ v_m^1, \ldots, v_m^l \}\\)
and \\(E_m^l = \Span \{ q_m^1, \ldots, q_m^l \}\\),
where \\(Q_m = \left( q_m^1, \ldots, q_m^d \right)\\),
\\(E_m^l\\) asymptotically approximate \\(U_m^l\\) because the direction of \\(U_m^l\\) has larger growth rate.
Hence, there is a upper triangle matrix \\(C_m\\) satisfying
\\[
V_m = Q_m C_m,
\\]
where \\(V_m = (v_m^1, \ldots, v_m^d )\\).
The Jacobian-invariance  deduces
\\[
R_m C_{m-1} = C_m
\\]
The last condition of \\(C_m\\) is , but it cannot be written explicitly.
To separate the directions in \\(E_m^l\\), we can use a backward iteration:
\\[
C_m = R_{m+1}^{-1} \cdots R_M^{-1} C_M,
\\]
where \\(M\\) is a large number for the convergence.
Then, we use \\(C_M = I\\) as an initial matrix of this iteration to be forgotten like \\(Q_0 = I\\):
\\[
C_m = R_{m+1}^{-1} \cdots R_M^{-1}.
\\]
For a finite \\(M\\), this is an approximation.
These forward  and backward  iterations calculates the covariant Lyapunov vector (CLV).


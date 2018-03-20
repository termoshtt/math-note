# Forward algorithm

Fix a large \\(M\\).
Generate \\((Q_m, R_m)\\) up to \\(M\\) by  from \\(Q_0 = I\\) with an extra matrix:
\\[
B_{m+1} =  B_m R_m^{-1} = R_1^{-1} \cdots R_m^{-1}.
\\]
This yields \\(Q_M\\) and \\(B_M\\), and other matrices are trashed.
We call this is an agent \\(A_1\\)
Then, we start another agent \\(A_0\\) from \\(Q_0=I\\).
Since \\(C_0\\) is already calculated as \\(B_M\\), we get \\(V_0 = Q_0 C_0\\).
We execute an iteration \\((Q_0, C_0, Q_M) \mapsto (Q_1, C_1, Q_{M+1})\\) as following:
\begin{align}
J_0 Q_0 &= Q_1 R_1, \\\\
J_M Q_M &= Q_{M+1} R_{M+1}, \\\\
C_1 &= R_1 C_0 R_{M+1}^{-1} 
\end{align}
We can drop \\(R_1\\) and \\(R_{M+1}\\) after calculating \\(C_1\\).
This algorithm does not include backward iteration and we need not to save \\(Q_m\\) or \\(R_m\\)
while the calculation cost is twice larger.

It should be noted that this update of \\(C_m\\) in  is different
from  with an extra multiplication of \\(R_{M+1}^{-1}\\).
This is due to the assumption about \\(M\\) is enough large.
In other words, this difference become negligible for enough large \\(M\\).



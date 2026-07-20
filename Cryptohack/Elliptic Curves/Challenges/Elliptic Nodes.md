# Encryption

Standard ECC encryption but with the $a, b$ parameters of the curve kept in secret.

Known:
- Prime field number
- Generator points
- Point $Q = [FLAG] G$
Knowing two points on the same curve is enough to retrieve the parameters of the curve.

# Solution

Given the Weierstrass equation
$$Y^2 = X^3 + aX + b$$
We can acquire the parameters by solving for $a$ and $b$.
$$\begin{align}
Y_1^2 - X_1^3 &= aX_1 + b &\bmod p\\
Y_2^2 - X_2^3 &= aX_2 + b &\bmod p
\end{align}$$
Using sage, it is found out that with the $a, b$ the constructed elliptic curve is singular, so the correct approach is to use an ecdlp for singular curve script.
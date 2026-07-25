
# Encryption

The interesting part is the generation of $d$
$$(3d)^4 > N$$
Which is the constraint set up for boneh-durfee attack.
$$d < 3\sqrt[4]{N}$$

# Solution

Since the implementations for boneh-durfee I found online keep failing, I chose to make my own.

Consider standard RSA $e, d$ relationship.
$$\begin{align}
ed &\equiv 1 &\bmod \varphi(N) \\
1 &= ed - 2k_0\frac{\varphi(N)}{2} \\
1 &= ed - k\frac{\varphi(N)}{2} \\\\
k &= 2k_0
\end{align}$$
Because RSA's totient function can be expressed as
$$\begin{align}
\varphi(N) &= (p-1)(q-1) \\
\varphi(N) &= pq - p - q + 1 \\
\varphi(N) &= N - p - q + 1
\end{align}$$

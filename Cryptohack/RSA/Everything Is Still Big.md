
# Encryption

The interesting part is the generation of $d$
$$(3d)^4 > N$$
Which is the constraint set up for boneh-durfee attack.
$$d < 3\sqrt[4]{N}$$

# Solution

Since the implementations for boneh-durfee I found online keep failing, I chose to make my own.

Consider standard RSA $e, d$ relationship.
$$\begin{align}
ed &\equiv 1 &\bmod \phi(N) \\
1 &= ed + k\phi(N)
\end{align}$$
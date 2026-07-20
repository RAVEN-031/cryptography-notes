# Process & Formula

Given prime $p$ and generator $g$
Alice picks private key $a$ and computes
$$A = g^{a} \bmod p$$
and sends it to Bob.

Bob picks private key $b$ and computes the Shared Secret.
$$\begin{align}S = A^b &\bmod p \\
S = g^{ab} &\bmod p\end{align}$$
# Challenges

- [[The Matrix Reloaded]]
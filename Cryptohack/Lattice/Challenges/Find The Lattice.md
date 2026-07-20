# Note: Fix solution
# Key Generation

- q : 512 bit prime
- upper bound : $\sqrt{\frac{q}{2}} \approx 256$ bit int
- lower bound  : $\sqrt{\frac{q}{4}} \approx 255$ bit int
- f : $[1, 256]$ bit int
- g : \[lower bound, upper bound\] random bit int
- gcd(f, g) = 1
- $h \equiv f^-1 * g \pmod{q}$

- Public key : (q, h)
- Private key : (f, g)
# Encryption

- m < upper bound
- r : random integer \[1, upper bound] bits

$$
\begin{aligned}
e &\equiv r*h + m &\bmod{q} \\
e &\equiv (rf^{-1}g) + m &\bmod{q}
\end{aligned}$$

# Decryption

$$
\begin{align}
a &\equiv f * e &\bmod{q} \\
a &\equiv f * (r f^{-1} g + m) &\bmod{q}\\
a &\equiv rg + fm &\bmod{q}\\
\end{align}
$$
Note: Due to size restriction of $f$ and $g$, $rg + gm < q$. Means  that a is its actual value unreduced by modulus
$$
\begin{aligned}
m &\equiv f^{-1} a  &\bmod{g} \\
m &\equiv f^{-1}(rg + fm)  &\bmod{g} \\
m &\equiv m &\bmod{g}
\end{aligned}
$$
Note: $rg$ is gone because the operation is done with modulus g and $rg$ is a multiple of g

# Lattice?
$$
\begin{align}
h &\equiv f^-1 * g &\bmod{q} \\
fh-g &\equiv 0 &\bmod{q}\\
fh - g &= qk_{1}\\\\
e &\equiv r*h + m &\bmod{q} \\
e - rh - m &\equiv 0 &\bmod{q} \\
e - rh - m &= qk_{2}
\end{align}$$
Constructing the lattice with the first equation to form a 2 dimensional lattice.
$$
\begin{align}
fh - g &= qk_{1} \\
\end{align}$$
$$
\begin{pmatrix}
f & g
\end{pmatrix}
=
\begin{pmatrix}
f & k_{1}
\end{pmatrix}
\begin{pmatrix}
1 & h \\
0 & -q
\end{pmatrix}
$$
Using gaussian reduction results in a key pair that still requires to be divided by the gcd of the key pair to acquire the actual key
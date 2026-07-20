# Encryption

- 64 bit private key
- 256 bit prime field
- EC parameters = (1, 4)
# Solution

64 bit for a private key size is feasible to compute with pollard's kangaroo which solves dlp over cyclic group given a known interval with $r$ being the interval
$$\mathcal{O}(r) = \sqrt{r}$$
In comparison, the standard pollard rho's algorithm solves dlp with the time complexity with $n$ being the order of the cyclic group
$$\mathcal{O}(n) = \sqrt{n}$$
32 bit for an ecdlp problem is highly feasible to compute
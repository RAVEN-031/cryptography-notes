I've found a super fast way to generate primes from my secret list.

# Encryption

RSA with primes p & q generated using mersenne's number

# Solution

Mersenne's number is any number written in the form of 
$$2^a - 1$$
This means that the bit size of the prime number is more or less the same as the exponent of the number. Considering that the bit size of the modulus is 4484, roughly $2^{13}$, bruteforcing the factors is trivial.
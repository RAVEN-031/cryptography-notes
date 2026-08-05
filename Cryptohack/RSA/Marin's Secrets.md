I've found a super fast way to generate primes from my secret list.

# Encryption

RSA with primes p & q generated using mersenne's number

# Solution

Mersenne's number is any number written in the form of 
$$2^a - 1$$
If $a$ is prime, the resulting number may be prime, such is called the mersenne's prime. 
Primality of  a mersenne's number is computed using the Lucas-Lehmer Test. The source script doesn't seem to be checking for if the number is prime or not.

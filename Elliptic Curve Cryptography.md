
Elliiptic Curves are often described with the Weierstrass equations which are of the form
$$E:Y^2 = X^3 + aX + b$$
Elliptic Curves form an Abelian group featuring an operation called "Point Addition". This operation takes two points, draws a straight line through both points until it intersects with the curve again producing a third point.
![[Pasted image 20260719174144.png]]
>Image taken from [Cryptohack's Elliptic Curve Course](https://cryptohack.org/courses/elliptic/)

Point $O$ is the point at infinity which acts as the identity operator of the group.

The constants $a, b$ have to satisfy the relation
$$4a^3 + 27b^2 \ne 0$$

# Challenges

- [[Micro Transmission]] (Small private key size attack)
- [[Elliptic Nodes]] (Singular elliptic curve)
- [[A Twisted Mind]]
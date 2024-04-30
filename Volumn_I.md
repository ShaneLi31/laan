# Ring
## [Property] a0 = 0 = 0a.

Proof.
```
a0 = a(0 + 0) = a0 + a0 => a0 = 0,
0a = (0 + 0)a = 0a + 0a => 0a = 0. []
```
##  [Property] a(-b) = -ab = (-a)b.

Proof.
```
a0 = a(b + (-b)) = ab + a(-b) => a(-b) = -ab,
0b = (a + (-a))b = ab + (-a)b => (-a)b = -ab. []
```
## [Property] a(b - c) = ab - ac.

Proof.
```
a(b - c) = a(b + (-c)) = ab + a(-c) = ab - ac. []
```
## [Property] For any integer n, n(ab) = (na)b = a(nb).

Proof.
```
n(ab) = ab + ... + ab = (((ab + ab) + ab) + ab) + ... + ab
        └─────┬─────┘ = (((a + a)b + ab) + ab) + ... + ab
              n       = (((2a)b + ab) + ab) + ... + ab
                      = ...
                      = (na)b,
```
```
n(ab) = ab + ... + ab = (((ab + ab) + ab) + ab) + ... + ab
        └─────┬─────┘ = ((a(b + b) + ab) + ab) + ... + ab
              n       = ((a(2b) + ab) + ab) + ... + ab
                      = ...
                      = a(nb). []
```
## [Property] Let A be a system which satisfied all the conditions for a ring except commutativity of addition. If A contains an element c that can be left cancelled in the sense that ca = cb implies a = b, then A is a ring.

Proof.
```
(c + c)(a + b) = c(a + b) + c(a + b) = ca + cb + ca + cb,
(c + c)(a + b) = (c + c)a + (c + c)b = ca + ca + cb + cb,
```
then
```
cb + ca = ca + cb => c(b + a) = c(a + b) => b + a = a + b. []
```
## [Property] A ring is an integral domain if and only if the restricted cancellation laws of multiplication hold, that is, ab = ac, a ≠ 0 imply b = c and ba = ca, a ≠ 0 imply b = c.

Proof.
For "=>", since a ≠ 0, a is not zero-divisor,
```
ab = ac => ab - ac = 0 => a(b - c) = 0 => b - c = 0 => b = c,
ba = ca => ba - ca = 0 => (b - c)a = 0 => b - c = 0 => b = c.
```
For "<=", a ≠ 0,
```
ab = 0 => ab = a0 => b = 0,
ba = 0 => ba = 0a => b = 0. []
```
## [Property] If a is a unit in a ring with an identity, then so is -a. (-a)^(-1) = -a^(-1).

Proof.
```
(-a)(-a^(-1)) = -a(-a^(-1)) = -(-aa^(-1)) = 1,
(-a^(-1)(-a)) = -a^(-1)(-a) = -(-a^(-1)a) = 1. []
```
## [Property] If a finite ring has one element a ≠ 0, a is not zero-divisor, then the ring has a identity.

Proof. There exists two positive integers n and m (n > m) such that a^n = a^m. Since a is not zero-divisor,
```
a^n = a^m => a^n - a^m = 0         => a(a^(n-1) - a^(m-1)) = 0
          => a^(n-1) - a^(m-1) = 0 => a(a^(n-2) - a^(m-2)) = 0
          => ...
          => a^(n-m+1) - a = 0
          => a = a^(n-m+1),
```
where n-m+1 >= 2. For any x in the ring,
```
0 = x0 = x(a - a^(n-m+1)) = xa - xa^(n-m+1) = (x - xa^(n-m))a => x - xa^(n-m) = 0 => x = xa^(n-m),
0 = 0x = (a - a^(n-m+1))x = ax - a^(n-m+1)x = a(x - a^(n-m)x) => x - a^(n-m)x = 0 => x = a^(n-m)x.
```
Therefor, a^(n-m) is the identity. []

## [Property] Any finite integral domain is a division ring.

Proof. For any a ≠ 0, a is not zero-divisor, so a^(n-m) = 1, where n-m >= 1. If n-m = 1, a = 1 is unit. If n-m > 1,
```
1 = a^(n-m) = aa^(n-m-1),
1 = a^(n-m) = a^(n-m-1)a,
```
a is also unit. []

## [Property] If an integral domain A has an idempotent element e ≠ 0 (e^2 = e), then e is an identity for A.

Proof. Since e is not zero-divisor, for any x in A,
```
0 = x0 = x(e - e^2) = xe - xe^2 = (x - xe)e => x - xe = 0 => x = xe,
0 = 0x = (e - e^2)x = ex - e^2x = e(x - ex) => x - ex = 0 => x = ex. []
```

## [Property] An element z of a ring is called nilpotent if z^n = 0. The only nilpotent element of an integral domain is z = 0.

Proof. Assume that z ≠ 0. Then
```
z                  is not zero-divisor =>
z^2 = zz       ≠ 0 is not zero-divisor =>
z^3 = zz^2     ≠ 0 is not zero-divisor =>
...
z^n = zz^(n-1) ≠ 0 is not zero-divisor =>
...
```
z is no way nilpotent. []

## [Property] If a ring R has only one left identity 1l, then 1l is an identity (two-sided).

Proof. For any a, b in R,
```
(a1l - a + 1l)b = a1lb - ab + 1lb = ab - ab + b = b.
```
So a1l-a+1l is another left identiry, then
```
a1l - a + 1l = 1l => a1l = a. []
```

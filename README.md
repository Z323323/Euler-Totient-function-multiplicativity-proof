# Totient mult. demon.
**$\phi(xy) = \phi(x)\phi(y) $**
## Example
<p>
Let's start with an example with 2 simple primes. The example looks stupid but it's easily formalizable and works for every pair of primes.<br>
$2*5 = 10$ <br>
$\phi(10) = \phi(2)\phi(5) = 4$ <br>
$\phi(5) = 4 = \{1, 2, 3, 4\}$ <br>
$\phi(2) = 1 = \{1\}$ <br>
</p>

![Scheme](Scheme.png)

<p>
- 5 numbers share the '2' divisor with whole group <br>
- 2 numbers share the '5' divisor with whole group <br>
Since the two conditions above coexist, the group can be divided 5 + 2 times (by 5 + 2 numbers). <br>
From this reasoning we have to remove 1 element because '10' is considered twice (2(5), 5(2)) then: <br>

$5 * 2 - \(5 + 2 - 1\) = 4$ <br>
$\phi(10) = 4 = \{1, 3, 7, 9\}$ <br>
</p>

## Formalization
<p>
We take 2 primes m,n, then: <br>
**$\phi(mn) = m * n - \(m + n -1\) $** <br>
**$m * n - m - n + 1 = \(m - 1\)\(n - 1\) $ _** <br>
where <br>
$\phi(m) = m - 1$ <br>
$\phi(n) = n - 1$ <br>
</p>

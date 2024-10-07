# Totient mult. demon.
**$\phi(xy) = \phi(x)\phi(y) $**
## Example

<p>Let's start with an example with 2 simple primes. The example looks stupid but it's easily formalizable and works for every pair of primes.<br>
$2*5 = 10$ <br>
$\phi(10) = \phi(2)\phi(5) = 4$ <br>
$\phi(5) = 4 = \{1, 2, 3, 4\}$ <br>
$\phi(2) = 1 = \{1\}$ <br>
</p>

![Scheme](Scheme2.png)


- 5 numbers share the '2' divisor with whole group
- 2 numbers share the '5' divisor with whole group
<p>Since the two conditions above coexist, there are 5 + 2 numbers which share either '2' or '5' as divisor. <br>
From this reasoning we have to remove 1 element because '10' is considered twice (2(5), 5(2)) then: <br>
$5 * 2 - (5 + 2 - 1) = 4$ <br>
$\phi(10) = 4 = \{1, 3, 7, 9\}$ <br>
</p>

## Formalization

<p>We take 2 primes m,n, then: <br>
$\phi(mn) = m * n - (m + n -1)$ <br>
$m * n - m - n + 1 = (m - 1)(n - 1)$ _ <br>
where <br>
$\phi(m) = m - 1$ <br>
$\phi(n) = n - 1$ <br>
</p>

## Further refinition
<p> The scheme above looks a little bit messy, and seems like it does not follow a structured rule, let's refine it taking another example.
</p>
## New. ex. $\phi(3*7)
<p> Before delving into the nex example, let's refine the scheme above to make it more structured and understand my point.<br>

  
</p>

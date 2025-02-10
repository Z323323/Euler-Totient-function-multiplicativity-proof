# Totient multiplicativity proof for primes

**$\phi(xy) = \phi(x)\phi(y)$**

### Definition

$\phi(n)$ is defined as the function which calculates the number of coprimes of $n$ which are $< n$, that is, every number $< n$ which doesn't share cofactors with $n$. We could have the exact same definition by implying that $\phi(n)$ is the number of coprimes of $n$ which are $\leq n$, and since $n$ is never coprime with itself it follows trivially that we are computing the number of coprimes of $n$ which are $< n$.

### Example

<p>
  
  Let's start with an example with $2$ simple primes. It looks stupid but it's easily formalizable and works for every pair of primes.
  
$10 = 2 \cdot 5$<br>
$\phi(5) = |\\{ 1, 2, 3, 4 \\}| = 4$<br>
$\phi(2) = |\\{ 1 \\}| = 1$<br>
$->$<br>
$\phi(10) = |\\{1, 3, 7, 9 \\}| = \phi(2)\phi(5) = 1 \cdot 4 = 4$ <br>
</p>

![Scheme](Scheme2.png)


- $5$ numbers share the $2$ divisor with whole group
- $2$ numbers share the $5$ divisor with whole group
<p>
  Since the two conditions above coexist, there are $5 + 2$ numbers which share either $2$ or $5$ as divisor. From this reasoning we have to remove $1$ element because $10$ is considered twice $(2(5), 5(2))$ then
  
$5 \cdot 2 - (5 + 2 - 1) = 4$<br>
$->$<br>
$\phi(10) = 4$

</p>

## Formalization

<p>We take 2 primes $m,n$ then
  
$\phi(mn) = m \cdot n - (m + n - 1)$<br>
$->$<br>
$m \cdot n - m - n + 1 = (m - 1)(n - 1)$

where

$\phi(m) = m - 1$ <br>
$\phi(n) = n - 1$

</p>

### Further refinition

<p> The scheme above looks a little bit messy, and seems like it does not follow a structured rule, let's refine it taking another example.
</p>

### Example 2: $\phi(3 \cdot 7)$

<p> Before delving the next example, let's refine the scheme above to make it more structured and understand my point.<br></p>

![2_5](2*5_fixed.png)

<p>Here the structure follows a structured reasoning, but our first $5$ non-coprime element is not positioned in the last line, does this breaks our proof? Here we could simply swap that element with $[2(4)+1]$ and the game would be done. But what would happen when we have more than $1$ co-factor i.e in $3 \cdot 7$? We know that there will be $3$ elements which share $7$ as co-factor, does this break our formalization? Because having $2$ elements to remove around and not removing the last line would mean to rebuild the formalization.<br>
It turns out that following the structure of the schemes proposed, it's always possible to swap every co-factor in the last line, breaking the structured format of the scheme but preserving formalization.<br>
Taken $a, b$ where $b > a$ there will be $a$ elements which share the $b$ cofactor, this means that they will always be positionable in the last line (of $a$ elements). This will be even more clear looking at the $3 \cdot 7$ example. <br></p>

![3_7](3*7.png)
  


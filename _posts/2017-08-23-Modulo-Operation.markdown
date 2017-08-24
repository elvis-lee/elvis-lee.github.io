---
layout: post
title:  "Modulo Operation"
date:   2017-08-23 16:00:00 -0800
categories: Java
---
The definition of modulo operation varies from languages to languages, but why?

In nearly all computing systems, the quotient q and the remainder r of a divided by n satisfy:

$$
q \in \Bbb Z \\\\
a = nq + r \\\\
|r| < |n| 
$$

However, this still leaves a sign ambiguity if the remainder is nonzero: two possible choices for the remainder occur, one negative and the other positive, and two possible choices for the quotient occur. [Modulo operation Wiki page][mod wiki]

[mod wiki]: https://en.wikipedia.org/wiki/Modulo_operation

There are three ways to implement modulo operation:

* Truncated division (`%` operator in Java)

  $$
  r = a - n\ \text{trunc} \left(\frac{a}{n}\right)
  $$

  The remainder would have same sign as the dividend. 

* Floored division (`Math.floorMod` method in Java)

  $$
  r = a - n\ \lfloor \frac{a}{n}\rfloor
  $$

  The remainder would have same sign as the divisor. 

* Euclidean division

  $$
  n > 0 \Rightarrow a - n\ \lfloor \frac{a}{n}\rfloor \\\\
  n < 0 \Rightarrow a - n\ \lceil \frac{a}{n}\rceil

  $$

  The remainder is nonnegative always.


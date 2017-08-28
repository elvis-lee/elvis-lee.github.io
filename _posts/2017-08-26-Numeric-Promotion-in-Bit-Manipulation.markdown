---
layout: post
title:  "Numeric Promotion in Bit Manipulation in Java"
date:   2017-08-26 15:49:00 -0700
categories: Java
---
How would you invert all bits in a byte? Most of people might come out with a simple line of code

```java
byte b = 1; b ~= b;
```

When you compile, an error will occur

> 1 error found:
File: /Users/ElvisLee/Dropbox/workspace/drjava_workspace/other/Playground.java  [line: 6]
Error: incompatible types: possible lossy conversion from int to byte

<br><br>
## **Why?**

Unary (such as ~) and binary operators in Java subject their operands to ["unary numeric promotion" (JLS, Section 5.6.1)](http://docs.oracle.com/javase/specs/jls/se7/html/jls-5.html#jls-5.6.1) and ["binary numeric promotion" (JLS, Section 5.6.2)](http://docs.oracle.com/javase/specs/jls/se7/html/jls-5.html#jls-5.6.2), respectively, fancy terms for "promote things to at least `int` first".

Specifically, for unary numeric promotion, quoting the JLS section linked above:
> if the operand is of compile-time type byte, short, or char, it is promoted to a value of type int by a widening primitive conversion ([§5.1.2](http://docs.oracle.com/javase/specs/jls/se7/html/jls-5.html#jls-5.1.2)).

(Binary numeric promotion is similar, operating on both operands.)

So, even if `b` is a `byte`, `~b` is an `int`, because `b`'s value was promoted to an `int` first.
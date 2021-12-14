---
published: true
layout: post
categories: misc
permalink: '/:categories/3'
title: '[Excursions] III'
---
{% include katex.html %}

Here, we wish to prove that for any \\( n\in \mathbb{N} \\), if \\( a^n \mid b^n \\) then we must have \\( a \mid b \\). 

> Note that the proof is immediate when \\( a=1 \\), thus, throughout this post we will be assuming that \\( a>1 \\). 

Although this may seem easy, the proof is rather complicated and requires us to do a lot of prerequisite work. The first of which is to be aware of FTA, the "Fundamental Theorem of Arithmetic",

> Theorem. [Fundamental Theorem of Arithmetic] Any integer \\( n>1 \\) can be represented uniquely as a product of prime powers, i.e,
\\[ n=p_1^{n_1}p_2^{n_2}\cdots p_k^{n_k} \\]
where \\( p_1<p_2<\cdots<p_k \\) are primes and \\( n_1,n_2,\ldots,n_k \\) are positive integers.

This is a pretty well known theorem so I will not include its proof here, I'm sure it is easy to find elsewhere. Let us use FTA to prove the following lemma

> Lemma 1. If \\( a \nmid b \\) then there exists a prime number \\( p \\) and a positive integer \\( t \\) such that \\( p^t \\) divides \\( a \\), but not \\( b \\).

Proof. Suppose the contrary, i.e, that if there is a pair \\( p,t \\) for which \\( p^t \mid a \\), then it must be that \\( p^t \mid b \\). This is incorporated into the second rule of the game:

- Two numbers, \\( a,b\in \mathbb{N} \\) are chosen so that \\( a\nmid b \\).

- Whenever Kwan finds a prime number \\( p \\) and a positive integer \\( t \\) that satisfies \\( p^t \mid a \\), he may conclude that \\( p^t \mid b \\).

- Kwan wins if he can create a contradiction.

By FTA, Kwan can decompose \\( a \\) into a product of prime powers. Suppose

\\[ a=p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_r^{\alpha_r} \tag{1}\\]

It is clear that \\( p_k^{\alpha_k} \mid a, \ (k=1,2,\ldots,r) \\), thus Kwan concludes that \\( p_k^{\alpha_k} \mid b, \ (k=1,2,\ldots,r) \\). By definition, this means that there exists numbers \\( m_1,m_2,\ldots,m_r\in \mathbb{N} \\) such that \\( b=m_kp_k^{\alpha_k}, \ (k=1,2,\ldots,r) \\). 

Multiplying (1) by \\( m_1m_2\cdots m_r \\) gives

\\[ am_1m_2\cdots m_r=b^r \quad \Longrightarrow \quad m_1m_2\ldots m_r=\frac{b}{a}b^{r-1}. \\]

Since \\( a \nmid b \\), the right hand side is not a whole number, but this is a contradiction because the left hand side definitely is. \\( \Box \\)

Now let us prove the next lemma,

> Lemma 2. If \\( a\nmid b \\), then \\( a^n \nmid b^n \\) where \\( n\in \mathbb{N} \\).

Proof. By lemma 1, we know that there exists a prime number \\( p \\) and a positive integer \\( t \\) such that \\( p^t\mid a \\) and \\( p^t \nmid b \\). Clearly \\( p^{tn} \mid a^n \\), now suppose \\( p^{tn} \mid b^n \\), then \\( b^n=kp^{tn} \\) for some \\( k \\). If \\( b \\) has the decomposition

\\[ b=p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_r^{\alpha_r} \tag{2}\\]

then the unique decomposition of \\( b^n \\) is

\\[ b^n=p_1^{n\alpha_1}p_2^{n\alpha_2}\cdots p_r^{n\alpha_r}=kp^{tn} \\]

This means that one of \\( p_1^{n\alpha_1},p_1^{n\alpha_2},\ldots, p_1^{n\alpha_r} \\) is equal to \\( p^{tn} \\) (while \\( k \\) is the rest), WLOG suppose \\( p_1^{n\alpha_1}=p^{tn} \\), thus \\( p_1^{\alpha_1}=p^t \mid b \\) (look at (2)). This is a contradiction, thus, \\( p^{tn} \nmid b^n \\).

\\( a^n \mid b^n \\) is impossible because \\( p^{tn} \mid a^n \\) and \\( \mid \\) is transitive. Thus we must have \\( a^n \nmid b^n \\) as desired.

> Theorem 3. Let \\( n\in \mathbb{N} \\), if \\( a^n \mid b^n \\), then \\( a\mid b \\). 

Proof. Assume that \\( a^n\mid b^n \\) but \\( a\nmid b \\), then lemma 2 tells us that \\( a^n \nmid b^n \\), this contradicts our initial assumption. \\( \Box \\)

Theorem 3 aside, lemma 2 also gives another interesting result:

> Theorem 4. For any \\( x,y\in \mathbb{N} \\), \\( x^{1/y} \\) is either irrational or an integer.

Proof. If \\( x^{1/y} \\) is neither irrational nor an integer then we can write \\( x^{1/y}=\frac{b}{a} \\) where \\( a\nmid b \\). However,

\\[ x=(x^{1/y})^y=\frac{b^y}{a^y} \\] 

is a contradiction. Lemma 2 tells us that \\( a^y \\) does not divide \\( b^y \\) so the far right hand side is not a whole number (while the far left hand side clearly is). \\( \Box \\)

Since \\( \sqrt{2} \\) is clearly not an integer, theorem 4 gives us a proof that \\( \sqrt{2} \\) is irrational, one that is different from the classic proof by contradiction.


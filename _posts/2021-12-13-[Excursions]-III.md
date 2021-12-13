---
published: true
layout: post
categories: misc
permalink: '/:categories/3'
title: '[Excursions] III'
---
{% include katex.html %}

Here, we wish to prove that for any \\( a,b\in \mathbb{N} \\), if \\( a^2 \mid b^2 \\) then we must have \\( a \mid b \\). 

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

It is clear that for each \\( k=1,2,\ldots,r \\), \\( p_k^{\alpha_k} \mid a \\), thus Kwan concludes that \\( p_k^{\alpha_k} \mid b \\) for each \\( k=1,2,\ldots,r \\). By definition, this means that there exists numbers \\( m_1,m_2,\ldots,m_r\in \mathbb{N} \\) such that \\( b=m_kp_k^{\alpha_k} \\) for each \\( k=1,2,\ldots,r. \\) 

Multiplying (1) by \\( m_1m_2\cdots m_r \\) gives

\\[ am_1m_2\cdots m_r=b^r \quad \Longrightarrow \quad m_1m_2\ldots m_r=\frac{a}{b}b^{r-1}. \\]

Since \\( a \nmid b \\), the right hand side is not a whole number, but this is a contradiction because the left hand side definitely is. \\( \Box \\)

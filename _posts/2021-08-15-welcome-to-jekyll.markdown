---
layout: post
title: 'Chapter 1.1, The Archemedean Property'
date: '2021-08-15 15:56:07 +0700'
categories: Metric Space Topology
published: true
permalink: '/:categories/1'
---
{% include katex.html %}

The Archemedean Property states that for any real number, \\(r\\), there exists a natural number \\(n\\) such that \\(x<n\\). Although this result is most certainly true and simple, it can be derived from the basic axioms which govern the set of real numbers, \\( \mathbb{R} \\).

One of the axioms involved is known as the least upper bound property, it states that any subset of \\( \mathbb{R} \\) that is bounded above has a least upper bound. Some of these words may seem unfamiliar to you so we shall define them.

> Definition 1.1 \\( \ x\in \mathbb{R}\\) is said to be an upper bound of a subset \\( A\subseteq\mathbb{R} \\) if for all \\( a\in A\\), we have \\( a\leq x\\).

For example, if \\( A=\{2,4,7\} \\), then \\( 8 \\) is an upper bound of \\( A \\) because \\( 8 \\) is greater than all the points contained within the set \\( A \\).

- List down some other upper bounds of \\( A \\), can \\( 7 \\) be put in this list?

It is believable to think that \\( 7 \\) is the smallest possible upper bound we can find for the set \\( A \\), in which case, we would say that \\( 7 \\) is the least upper bound of \\( A \\). We shall define this more formally:

> Definition 1.2 \\( \ x\in \mathbb{R} \\) is said to be the least upper bound of a subset \\( A\subseteq\mathbb{R} \\) if in addition to \\(x \\) being an upper bound of \\(A\\), it also satisfies \\( x<c \\) for all other upper bounds \\(c\\) of \\( A \\).
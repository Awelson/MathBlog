---
layout: post
title: 'Chapter 1.1, The Archemedean Property'
date: '2021-08-15 15:56:07 +0700'
categories: Metric-Space-Topology
published: true
permalink: '/:categories/1'
---
{% include katex.html %}

The Archemedean property states that for any real number, \\(r\\), there exists a natural number \\(n\\) such that \\(x<n\\). Although this result is most certainly true and simple, it can be derived from the basic axioms which govern the set of real numbers, \\( \mathbb{R} \\).

One of the axioms involved is known as the least upper bound property, it states that any subset of \\( \mathbb{R} \\) that is bounded above has a least upper bound. Some of these words may seem unfamiliar to you so we shall define them.

> Definition 1.1.1 \\( \ x\in \mathbb{R}\\) is said to be an upper bound of a subset \\( A\subseteq\mathbb{R} \\) if for all \\( a\in A\\), we have \\( a\leq x\\).

For example, if \\( A=\lbrace 2,4,7 \rbrace \\), then \\( 8 \\) is an upper bound of \\( A \\) because \\( 8 \\) is greater than or equal to all the points contained within the set \\( A \\).

\\[ \fbox{\text{List down some other upper bounds of } A, \text{ can }7 \text{ be put in this list?}} \\]

It is believable to think that \\( 7 \\) is the smallest possible upper bound we can find for the set \\( A \\), in which case, we would say that \\( 7 \\) is the least upper bound of \\( A \\). We shall define this more formally below,

> Definition 1.1.2 \\( \ x\in \mathbb{R} \\) is said to be the least upper bound of a subset \\( A\subseteq\mathbb{R} \\) if in addition to being an upper bound of \\(A\\), it also satisfies \\( x\leq c \\) for any upper bound \\(c\\) of \\( A \\). We will sometimes denote the least upper bound of \\( A \\) with \\( \text{sup }A \\).

- It is clear from the definition that given any subset \\( A\subseteq \mathbb{R} \\), the least upper bound of \\( A \\) is unique. Even if this result is obvious, I encourage you to prove it yourself!

Given a subset \\( A\subseteq \mathbb{R} \\), it is easy to guess what it's least upper bound should be, for example, we may guess the number \\( x\in \mathbb{R} \\), however, actually proving that \\( x=\text{sup }A \\) will prove to be more difficult. We have two things to show:

1. Show that \\( x \\) is an upper bound of \\( A \\)
2. Show that \\( x\leq c \\) for any upper bound \\( c \\) of \\( A \\)

Step 1 is super easy. Step 2 is equivalent to showing that there is no upper bound less than \\( x \\), i.e, we need to show that \\( \ \ c<x \ \Longrightarrow \ "c \\) is not an upper bound of \\( A" \\) (the arrow means "implies"). Reformulating step 2 this way will make things much easier (trust me).

As an example, we shall prove that given \\( A=\\{2,4,7\\} \\), we have \\( \text{sup }A=7 \\). The first step (showing that 7 is an upper bound of \\( A \\)) is immediate. For the second step, assume that \\( c<7 \\). In order for \\( c \\) to be an upper bound of \\( A \\), it needs to be greater than or equal to \\( 7 \\), this however, is not possible because \\( c<7 \\), thus, \\( c \\) cannot be an upper bound of \\( A \\). This councludes our proof that \\( \text{sup }A=7 \\).

A more complicated example would be \\( A=(0,1) \\). A reasonable guess would be \\( \text{sup }A=1 \\). We shall skip to the second step. It is beneficial to split cases. Case 1: \\( -1<c<1 \\). Case 2: \\( c\leq -1 \\). In either case, we need to show that \\( c \\) is not an upper bound of \\( A \\).

Case 1: To show that \\( c \\) is not an upper bound of \\( A \\), we will show that there exists an \\( a\in A \\) such that \\( c<a \\) (why does this imply that \\( c \\) is not an upper bound of \\( A \\)?) We propose letting \\( a \\) be the midpoint between \\(c \\) and \\( 1 \\), i.e, \\( a=\frac{c+1}{2} \\). Notice that \\( c<a \\) is immediate, further, since we already know that \\( \ a<1 \\), it suffices to show that \\( 0<a \\) in order to show that \\( a\in A \\). This is easy,

\\[ -1<c \ \Longrightarrow \ 0<c+1 \ \Longrightarrow \  0<\frac{c+1}{2}=a \\]

Case 2: This is really easy, so I will have you fill in the details yourself.

- Using more or less the same argument, show that \\( \text{sup }\[0,1\]=1 \\)

Before moving on, let us answer an important question: do all subsets of \\( \mathbb{R} \\) have an upper bound? Try to answer this question and provide your reasonings. 

The correct answer is no, for example, the subset \\( \mathbb{R}\subeteq \mathbb{R} \\) itself has no upper bounds. Suppose \\( c\in \mathbb{R} \\) is an upper bound of \\( \mathbb{R} \\), then \\( c<c+1 \\) but \\( c+1\in \mathbb{R} \\), this contradicts the fact that \\( c \\) is an upper bound of \\( \mathbb{R} \\). Next question: if \\( \mathbb{R} \\) has no upper bounds, does it have a least upper bound, in other words, does \\( \text{sup }\mathbb{R} \\) exist?

The answer is no, obviously.

> Definition 1.1.3 A subset \\( A\subseteq \mathbb{R} \\) is said to be bounded above if an upper bound for \\( A \\) exists. Conversely, if an upper bound for \\( A \\) does not exist, then \\( A \\) is said to be unbounded above.

We have seen examples of sets that are unbounded above, \\( \mathbb{R} \\), and sets that are bounded above, \\( \ \\{2,4,7\\} \\). The following should make sense:

> Theorem 1.1.4 If a subset \\( A\subseteq \mathbb{R} \\) is unbounded above, then \\( \text{sup }A \\) does not exist.

But what about its counterpart: If a subset \\( A\subseteq \mathbb{R} \\) is bounded above, then \\( \text{sup }A \\) exists.

Is this statement true? Can we prove it? If you have a good memory, you should remember from the beginning of this blog post that this statement is an axiom. It is a fundamental property of the real numbers, and therefore, need not be proven. Remember that the concept of real numbers are something we humans constructed for ourselves, and conveniently, we constructed the real numbers so that the least upper bound property holds true.

As we shall see, the least upper bound property can be used to prove the Archemedean property. Before getting to that, let's talk about the counterpart of upper bounds, lower bounds.

### Lower Bounds

> Definition 1.1.5 \\( \ x\in \mathbb{R}\\) is said to be a lower bound of a subset \\( A\subseteq\mathbb{R} \\) if for all \\( a\in A\\), we have \\( x\leq a\\).

For example, \\( 1 \\) is a lower bound of \\( \\{2,4,7\\} \\). It makes no sense to ask what the lowest lower bound is, so instead, we ask what the greatest lower bound is. 

- What is the greatest lower bound of the set from the example above?
- Write a formal definition for the greatest lower bound, just like we did in Definition 1.1.2 for the least upper bound. Note: we use the symbol \\( \text{inf }A \\) to denote the greatest lower bound of a set \\( A \\).
- Create a two step process (just like we did for the least upper bound) to prove that a number is indeed the greatest lower bound.
- What do you think it should mean for a set to be bounded/unbounded below?
- Provide an example of a set that is unbounded below, does this set have a greatest lower bound?
- If a set \\( A \\) is bounded below, does \\( \text{inf }A \\) exist? The answer is yes!

> Definition 1.1.6 A subset \\(A \subseteq \mathbb{R} \\) is said to be bounded if it is both bounded above and bounded below. It is clear that a bounded set has both a least upper bound and a greatest lower bound.

A relationship between least upper bound and greatest lower bound can be described as follows:

> Theorem 1.1.7 Let \\( A\subseteq \mathbb{R} \\) be a bounded set. If \\(B=\\{-a \ \vert \ a\in A\\} \\), then \\( \text{inf }B=-\text{sup }A \\).

Proof. Set \\( x=\text{sup }A \\), then we need to show that \\( -x \\) is the greatest lower bound of \\( B \\). First, we show that \\( -x \\) is a lower bound of \\( B \\): We know that \\( a\leq x \\) for all \\( a\in A \\), multiplying this inequality by negative one gives \\( -x\leq -a \\) for all \\( a\in A \\), i.e, \\( -x \\) is a lower bound of \\( B \\).

Next, we show that \\( c\leq -x \\) for all lower bounds \\( c \\) of \\( B \\). Let \\( c \\) be a lower bound of \\( B \\), this means that \\( c\leq -a \\) for all \\( a\in A \\), multiplying by negative one gives \\( a\leq -c \\) for all \\( a\in A \\), i.e, \\( -c \\) is an upper bound of \\( A \\). Because \\( x=\text{sup }A \\), we have \\( x\leq -c \\), multiplying by negative one again gives \\( c\leq -x \\) as desired. \\( \Box \\)



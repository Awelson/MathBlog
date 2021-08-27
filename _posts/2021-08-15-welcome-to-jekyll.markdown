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

A more complicated example would be \\( A=(0,1) \\). A reasonable guess would be \\( \text{sup }A=1 \\). We shall skip to the second step. It is beneficial to split cases. Case 1: \\( 0<c<1 \\). Case 2: \\( c\leq 0 \\). In either case, we need to show that \\( c \\) is not an upper bound of \\( A \\).

Case 1: To show that \\( c \\) is not an upper bound of \\( A \\), we will show that there exists an \\( a\in A \\) such that \\( c<a \\) (why does this imply that \\( c \\) is not an upper bound of \\( A \\)?) Let \\( a \\) be the midpoint between \\(c \\) and \\( 1 \\), i.e, \\( a=\frac{c+1}{2} \\). Since \\( a \\) is the midpoint between \\( c \\) and \\( 1 \\), we have the following inequality,

\\[ 0<c<a<1 \\]

Thus, \\( a\in A \\) and \\( c<a \\) are both satisfied. 

Case 2: This is really easy, so I will have you fill in the details yourself.

- Using more or less the same argument, show that \\( \text{sup }\[0,1\]=1 \\)

Before moving on, let us answer an important question: Do all subsets of \\( \mathbb{R} \\) have an upper bound? Try to answer this question and provide your justification.

The correct answer is no, for example, the subset \\( \mathbb{R}\subseteq \mathbb{R} \\) itself has no upper bounds. Suppose \\( c\in \mathbb{R} \\) is an upper bound of \\( \mathbb{R} \\), then \\( c<c+1 \\) but \\( c+1\in \mathbb{R} \\), this contradicts the fact that \\( c \\) is an upper bound of \\( \mathbb{R} \\). If \\( \mathbb{R} \\) has no upper bounds, does it have a least upper bound, in other words, does \\( \text{sup }\mathbb{R} \\) exist?

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

- What is the greatest lower bound of the set from the above example?
- Write a formal definition for the greatest lower bound, just like we did in Definition 1.1.2 for the least upper bound. Note: we write \\( \text{inf }A \\) to denote the greatest lower bound of a set \\( A \\).
- Show that \\( \text{inf }(0,1)=0 \\).
- What should it mean for a set to be bounded/unbounded below?
- If a set \\( A \\) is bounded below, does \\( \text{inf }A \\) exist? In other words, does the least upper bound property translate over to greatest lower bounds as well? The answer is yes!

> Definition 1.1.6 A subset \\(A \subseteq \mathbb{R} \\) is said to be bounded if it is both bounded above and bounded below. It is clear that a bounded set has both a least upper bound and a greatest lower bound. If a set is not bounded we say that it is unbounded.

After completing the exercises above, you will notice that the concept of greatest lower bounds is not dissimilar to that of least upper bounds, in fact, a relationship between least upper bound and greatest lower bound can be described as follows:

> Theorem 1.1.7 Let \\( A\subseteq \mathbb{R} \\) be a bounded set. If \\(B=\\{-a \ \vert \ a\in A\\} \\), then \\( \text{inf }B=-\text{sup }A \\).

Proof. Set \\( x=\text{sup }A \\), then we need to show that \\( -x \\) is the greatest lower bound of \\( B \\). First, we show that \\( -x \\) is a lower bound of \\( B \\): We know that \\( a\leq x \\) for all \\( a\in A \\), multiplying this inequality by negative one gives \\( -x\leq -a \\) for all \\( a\in A \\), i.e, \\( -x \\) is a lower bound of \\( B \\).

Next, we show that \\( c\leq -x \\) for all lower bounds \\( c \\) of \\( B \\). Let \\( c \\) be a lower bound of \\( B \\), this means that \\( c\leq -a \\) for all \\( a\in A \\), multiplying by negative one gives \\( a\leq -c \\) for all \\( a\in A \\), i.e, \\( -c \\) is an upper bound of \\( A \\). Because \\( x=\text{sup }A \\), we have \\( x\leq -c \\), multiplying by negative one again gives \\( c\leq -x \\) as desired. \\( \Box \\)

### The Archemedean Property

We are now ready to prove the Archemedean Property. We will restate it again:

> Theorem 1.1.8 For any \\( x\in \mathbb{R} \\), there exists an \\( n\in \mathbb{N} \\) such that \\( x<n \\). 

Proof. We prove by contradiction, so assume \\( \exists x\in \mathbb{R}, \forall n\in \mathbb{N}, n\leq x \\). This means that \\( \mathbb{N} \\) is bounded above. By the least upper bound property, \\( \text{sup }\mathbb{N} \\) exists, lets call it \\( c \\). 

Notice that \\( c-1 \\) cannot be an upper bound of \\( \mathbb{N} \\) since \\( c \\) is the *least* upper bound of \\( \mathbb{N} \\). This means that there exists an \\( n\in \mathbb{N} \\) such that \\( c-1<n \\). In other words, \\( c<n+1 \\), but \\( n+1 \\) is a natural number (obviously), this tells us that \\( c \\) fails to be an upper bound of \\( \mathbb{N} \\), this is a contradiction. \\( \Box \\).

Although the Archemedean Property itself is obvious and straightforward, it is integral in the proofs of some less obvious facts. For instance, it leads to the proof that a rational number exists between any two distinct real numbers. This will require a bit of prep work. First, we introduce another axiom 

> \[The Well-Ordering Principle\] Every non-empty subset of \\( \mathbb{N} \\) has a well defined minimum.

Next, we shall prove two corollaries of the archemedean property,

> Corollary 1.1.8.1 For any \\( x\in \mathbb{R} \\), there exists an \\( n\in \mathbb{Z} \\) such that \\( n-1\leq x < n \\). 

Proof. Assume that \\( x\geq 0 \\). Let
\\[ A=\\{ n\in \mathbb{N} \ \vert \ x<n \\}. \\]
The Archemedean Property tells us that \\( A \\) is non-empty, therefore, by the well-ordering principle, \\( \text{min }A \\) exists, let's call it \\( c \\). If \\( c=1 \\), then \\( 0\leq x< 1 \\), and there is nothing left to show. Now assume that \\( c\geq 2 \\), then \\( c-1 \\) is a natural number (if \\( c=1 \\), then \\( c-1=0 \\) is not a natural number). \\( x<c \\) is already true, so we just need to show that \\( c-1\leq x \\). We prove by contradiction, suppose that \\( x<c-1 \\), then since \\( c-1\in \mathbb{N} \\) is also true, we must have \\( c-1\in A \\), but this contradicts \\( c \\) being the minimum of \\( A \\).

Now assume that \\( x<0 \\). This means that \\( 0<-x \\), and by the above, there exists an \\( n\in \mathbb{N} \\) such that \\( n-1\leq -x < n \\). This means that \\( -n < x \leq 1-n \\). Notice that we can write \\( -n=z-1 \\) for some \\( z\in \mathbb{Z} \\), substitution then gives \\( z-1< x \leq z \\). This is not exactly the inequality we are looking for (but it's close!), the finishing touch is easy, so I will leave it to you. \\( \Box \\)

> Corollary 1.1.8.2 Given any \\( y>0 \\), there exists an \\( n\in \mathbb{N} \\) such that \\( \frac{1}{n}<y \\). 

Proof. Notice that \\( 1/y \\) is a real number, the Archemedean Property tells us that there exists an \\( n\in \mathbb{N} \\) such that \\( \frac{1}{y}<n \\). Multiplying this inequality by \\( \frac{y}{n} \\) ( \\( notice that \frac{y}{n}>0 \\) because \\( y>0 \\)), we obtain \\( \frac{1}{n}<y \\) as needed. \\( \Box \\).

We are now ready for the main punchline,

> Theorem 1.1.9 Given \\( x,y\in \mathbb{R} \\) with \\( x<y \\), there exists a \\( q\in \mathbb{Q} \\) such that \\( x<q<y \\).

Proof. We need to find two integers, \\( n,m \\) such that \\( x<\frac{m}{n}<y \\). Via corollary 1.1.8.2, we can choose an \\( n\in \mathbb{N} \\) which satisfies \\( \frac{1}{n}<y-x \\). With \\( n \\) already chosen, we use corollary 1.1.8.1 to choose an \\( m\in \mathbb{Z} \\) which satisfies \\( m-1\leq nx < m \\). Dividing the inequality by \\( n \\) gives \\( x<\frac{m}{n} \\), so now it suffices to show that \\( \frac{m}{n}<y \\). 

This time, add one to the inequality, this gives \\( m\leq nx+1 \\). Remember that we chose \\( n \\) so that \\( \frac{1}{n}<y-x \\) is satisfied. Dividing the inequality by \\( n \\) now gives

\\[ \frac{m}{n}\leq x+\frac{1}{n}<x+(y-x)=y. \\]

This finishes the proof. \\( \Box \\)

Aside from telling us that there exists a rational number between any two distinct real numbers, theorem 1.1.9 also gives us a method to construct such a rational number.

**Example.** Say we wish to find a rational number between \\( e \\) and \\( \pi \\). We can do this by choosing an \\( n\in \mathbb{N} \\) which satisfies \\( \frac{1}{n}<\pi-e \\). It is easy to see that \\( n=10 \\) satisfies this condition. Next, we choose an \\( m\in \mathbb{Z} \\) which satisfies \\( m-1\leq 10e < m \\). Quick calculation tells us that \\( m \\) should equal 28. By theorem 1.1.9, \\( \frac{28}{10} \\) is a rational number between \\( e \\) and \\( \pi \\), this can be easily verified.

Here is a nice corollary of theorem 1.1.9:

> Corollary 1.1.9.1 Given any two real numbers, \\( x \\) and \\( y \\), with \\( x<y \\). There exists an irrational number between \\( x \\) and \\( y \\).

Proof. By theorem 1.1.9, we are able to find a rational number between \\( x-\sqrt{2} \\) and \\( y-\sqrt{2} \\), i.e, there exists a \\( q\in \mathbb{Q} \\) satisfying

\\[ x-\sqrt{2}<q<y-\sqrt{2}. \\]

Adding by \\( \sqrt{2} \\) gives \\( x<q+\sqrt{2}<y \\). Since \\( q+\sqrt{2} \\) is irrational, the proof is complete. \\( \Box \\)

### Extension to Infinity

The set \\( A=\\{1,2,\ldots\\} \\) is clearly unbounded above, so \\( \text{sup }A \\) does not exist, however, it wouldn't be inaccurate if we were to say that \\( \text{sup }A=\infty \\) because this statement conveys the idea that \\( A \\) is unbounded above. Similarly, if \\( A \\) is unbounded below, it also wouldn't be inaccurate to say that \\( \text{inf }A=-\infty \\). 

This gives us two different conventions, for example, for a set that is unbounded above, we may either state that its supremum does not exist, or we may state that its supremum is infinity. We shall switch between these two conventions whenever it suits us.

If we would like to implement the latter convention, we will state something along the lines of 'we shall allow the supremum(or infimum) to take infinite values', alternatively, the statement '\\( \text{sup }A( \\)or \\( \text{ inf }A )\in \mathbb{R}^\* \\)' (where \\( \mathbb{R}^\*=\mathbb{R}\cup \\{\infty,-\infty\\} \\)) conveys the same meaning. 

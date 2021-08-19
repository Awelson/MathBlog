---
published: true
layout: post
title: An Elementary Inequality
date: '2021-08-19 15:56:07 +0700'
categories: Misc
permalink: '/:categories/1'
---
{% include katex.html %}

We will be proving the following inequality,

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x\|}+\frac{\|y\|}{1+\|y\|}, \quad x,y\in \mathbb{R}.\\]

Note that these fractions are always defined because the denominators are always non-zero. Assume that \\( \|x+y\|\leq \|x\| \\). This means that

\\[ \|x+y\|+\|x\|\|x+y\|\leq \|x\|+\|x\|\|x+y\| \quad \Longrightarrow \quad \|x+y\|(1+\|x\|)\leq \|x\|(1+\|x+y\|). \\]

After diving both sides by \\( \frac{1}{(1+\|x\|)(1+\|x+y\|)} \\), we obtain:

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x\|}. \\]

Since \\( \frac{\|y\|}{1+\|y\|} \\) is positive, this gives

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x\|}+\frac{\|y\|}{1+\|y\|} \\]

as required.

Now assume that \\( \|x+y\|\leq \|y\| \\), so we have

\\[ \|x+y\|+\|y\|\|x+y\|\leq \|y\|+\|y\|\|x+y\| \quad \Longrightarrow \quad \|x+y\|(1+\|y\|)\leq \|y\|(1+\|x+y\|). \\]

After diving both sides by \\( \frac{1}{(1+\|y\|)(1+\|x+y\|)} \\), we obtain:

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|y\|}{1+\|y\|}. \\]

Since \\( \frac{\|x\|}{1+\|x\|} \\) is positive, we reach our goal inequality again.

We have shown that the inequality is true if either \\( \|x\| \\) or \\( \|y\| \\) is greater than or equal to \\( \|x+y\| \\), so now we need to consider what happens if both \\( \|x\| \\) and \\( \|y\| \\) are less than \\( \|x+y\| \\).

The triangle inequality states that \\( \|x+y\|\leq \|x\|+\|y\| \\), therefore,

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x+y\|}+\frac{\|y\|}{1+\|x+y\|}. \\]

Since \\( \|x\|<\|x+y\| \\), we have

\\[ \frac{\|x\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x\|}. \\]

In a similar fashion, \\( \|y\|<\|x+y\| \\) leads to

\\[ \frac{\|y\|}{1+\|x+y\|}\leq \frac{\|y\|}{1+\|y\|}. \\]

and therefore, 

\\[ \frac{\|x+y\|}{1+\|x+y\|}\leq \frac{\|x\|}{1+\|x\|}+\frac{\|y\|}{1+\|y\|} \\]

as needed.

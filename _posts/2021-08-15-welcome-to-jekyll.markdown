---
layout: post
title: 'Chapter 1.1, The Archemedean Property'
date: '2021-08-15 15:56:07 +0700'
categories: jekyll update
published: true
---
{% include katex.html %}

The Archemedean Property states that for any real number, \\(r\\), there exists a natural number \\(n\\) such that \\(x<n\\). Although this result is most certainly true and simple, it can be derived from the basic axioms which govern the set of real numbers, \\( \mathbb{R} \\).

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

---
layout: post
title:  "MathJax with Jekyll"
date:   2017-08-24 00:00:00 -0800
categories: Jekyll
---

In [the last article][last], I tried the very first time typing math formulas via [MathJax][mathjax]. It took me 3 hours to implement MathJax with Jekyll, so I just kept track of issues and solutions here for any further reference.

[last]: https://elvis-lee.github.io/java/2017/08/23/Modulo-Operation.html
[mathjax]: https://www.mathjax.org

I am using: 

* Kramdown

* Minima (Jekyll default theme)

<br><br>
List of links that I found useful:

* [Customizing CSS and HTML in your Jekyll theme](https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/)

* [Kramdown with MathJax](https://kramdown.gettalong.org/math_engine/mathjax.html)

* [MathJax with Jekyll](http://gastonsanchez.com/visually-enforced/opinion/2014/02/16/Mathjax-with-jekyll/)

* [MathJax basic tutorial and quick reference](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)

* [TeX commands available in MathJax](http://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm)

* [How to use MathJax in Jekyll generated Github pages](http://haixing-hu.github.io/programming/2013/09/20/how-to-use-mathjax-in-jekyll-generated-github-pages/)

* [Jekyll directory structure](https://jekyllrb.com/docs/structure/)

* [Jekyll Math Support](https://jekyllrb.com/docs/extras/#math-support)

<br><br>
**How to do it:** 

Add a link to MathJax in my `/_layouts/default.html`. Note that kramdown does not ship with the MathJax library and that therefore the “default” template does not include a link to it! [MathJax: Getting Started](http://docs.mathjax.org/en/latest/start.html) describes how to do it. Basically, I just added the following codes in my `/_layouts/default.html` file(create one in my own repo to overwrite the one in minima repo).

	```javascript
	<script type="text/javascript" async
  	src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
	</script>
	```

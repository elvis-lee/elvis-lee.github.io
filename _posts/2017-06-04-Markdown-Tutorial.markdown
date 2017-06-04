---
layout: post
title:  "Markdown Tutorial"
date:   2017-06-04 16:00:00 +0800
categories: markdown
---
To begin bloging, I studied `Markdown` from [a useful tutorial][markdown tutorial]. This blog is itself written using Markdown.



### 1. Font
* Italics

  To make a phrase italic in Markdown, we can surround words with an underscore (`_`).

  Syntax:
  {% highlight ruby %}
  _italic words_
  {% endhighlight %}

* Bold

  Similarly, to make phrases bold in Markdown, we can surround words with two asterisks (`**`).

  Syntax:
  {% highlight ruby %}
  **bold words**
  {% endhighlight %}



### 2. Header
To make headers in Markdown, you preface the phrase with a hash mark (`#`). You place the same number of hash marks as the size of the header you want. For example, for a header one, you'd use one hash mark (`# Header One`), while for a header three, you'd use three (`### Header Three`).



### 3. Link
* Inline Links

  Syntax:
  {% highlight ruby %}
  [link text](link URL)
  {% endhighlight %}

* Reference Links

  Syntax:
  {% highlight ruby %}
  [link text][link tag]
  [link tag]:link URL
  {% endhighlight %}



### 4. Images
Creating images is quite the same as creating links. The difference is that an image is prefaced with an exclamation mark（`!`）.

* Inline Images 

  Syntax:
  {% highlight ruby %}
  ![alt text](image URL)
  {% endhighlight %}

* Reference Images

  Syntax:
  {% highlight ruby %}
  ![alt text][image tag]
  [image tag]:image URL
  {% endhighlight %}

  Noted: Alt text in the brackets is optional, but it's considered useful and polite to the visually impaired.



### 5. Blockquote
Preface a line with the "greater than" caret (`>`) to create a block quote. If the quote spans multiple paragraphs, remember to place a caret character on each line of the quote. Here is an example: 
> Block quoting in Markdown is easy!



### 6. List

* Unordered List
  Preface each item in the list with an asterisk (`*`) to create an unordered list. Want more depth? Just indent each asterisk one space more than the preceding item.

* 6.2 Ordered List
  Ordered lists use numbers followed by periods. 

  Suppose we want to create a bullet list that requires some additional context (but not another list). To create this sort of text, your paragraph must start on a line all by itself underneath the bullet point, and it must be indented by at least one space. 



### 7. Paragraph
`Hard break` is breaking two paragraphs by inserting a new line between them. `Soft break` breaks paragraphs without inserting new lines. 

To make soft breaks, simply insert two spaces after each line.

### Reference Links
* [Markdown Tutorial][markdown tutorial]
* [Daring Fireball Markdown Basic][markdown basic]
* [Online Markdown Editor: Dingus][markdown editor]

[markdown tutorial]: http://www.markdowntutorial.com
[markdown basic]: https://daringfireball.net/projects/markdown/basics
[markdown editor]: https://daringfireball.net/projects/markdown/dingus


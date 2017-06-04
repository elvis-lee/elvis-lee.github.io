---
layout: post
title:  "Markdown Tutorial"
date:   2017-06-04 16:00:00 +0800
categories: markdown
---
To begin bloging, I studied `Markdown` from [a useful tutorial][markdown tutorial]. 

**Note:** This post is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

[src]: /text/t.text
<br><br>


### 1. Font
* Italics

  To make a phrase italic in Markdown, we can surround words with an underscore (`_`).

  Syntax:
  `_italic words_`

* Bold

  Similarly, to make phrases bold in Markdown, we can surround words with two asterisks (`**`).

  Syntax:
  `**bold words**`



### 2. Header
To make headers in Markdown, you preface the phrase with a hash mark (`#`). You place the same number of hash marks as the size of the header you want. For example, for a header one, you'd use one hash mark (`# Header One`), while for a header three, you'd use three (`### Header Three`).



### 3. Link
* Inline Links

  Syntax:`[link text](link URL)`

* Reference Links

  Syntax:
  ```
  [link text][link tag]
  [link tag]:link URL
  ```



### 4. Images
Creating images is quite the same as creating links. The difference is that an image is prefaced with an exclamation mark（`!`）.

* Inline Images 

  Syntax:
  `![alt text](image URL)`

* Reference Images

  Syntax:
  ```
  ![alt text][image tag]
  [image tag]:image URL
  ```
  

  Noted: Alt text in the brackets is optional, but it's considered useful and polite to the visually impaired.

  Images support test:![ZJU][zju]



### 5. Blockquote
Preface a line with the "greater than" caret (`>`) to create a block quote. If the quote spans multiple paragraphs, remember to place a caret character on each line of the quote. Here is an example: 
> Block quoting in Markdown is easy!



### 6. List

* Unordered List

  Preface each item in the list with an asterisk (`*`) to create an unordered list. Want more depth? Just indent each asterisk one space more than the preceding item.

* Ordered List

  Ordered lists use numbers followed by periods. 

  Suppose we want to create a bullet list that requires some additional context (but not another list). To create this sort of text, your paragraph must start on a line all by itself underneath the bullet point, and it must be indented by at least one space. 

### 7. Paragraph

`Hard break` is breaking two paragraphs by inserting a new line between them. `Soft break` breaks paragraphs without inserting new lines. 

To make soft breaks, simply insert two spaces after each line.

### 8. Code

* Inline Code

  For inline code blocks, wrap them in backticks: \`var example = true\`. Output: `var example = true`

* Longer Code Block

  Syntax:

      ```Language
      bla bla bla
      {
  	    bla bla bla
      }
      ```


  For example,
  
      ```javascript
      if (isAwesome){
        return true
      }
      ```
  
  Output:
  ```javascript
  if (isAwesome){
    return true
  }
  ```

<br><br>  
### Small Tricks
* How to create blank lines?

  Since most of the Markdown complier html, we can simply add `<br><br>` in the Markdown source.


<br><br>
### Reference Links
* [Markdown Tutorial][markdown tutorial]
* [Daring Fireball Markdown Basic][markdown basic]
* [Online Markdown Editor: Dingus][markdown editor]



[markdown tutorial]: http://www.markdowntutorial.com
[markdown basic]: https://daringfireball.net/projects/markdown/basics
[markdown editor]: https://daringfireball.net/projects/markdown/dingus
[zju]: /image/2017-06-04-Markdown-Tutorial.markdown/zju.jpg
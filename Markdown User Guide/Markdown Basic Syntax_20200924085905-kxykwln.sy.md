> This article mainly introduces the basic syntax of Markdown, please refer to ((20200924092619-pw51c0y "Markdown Extended Syntax")).
> The concise version of the grammar can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).

## Overview

Almost all Markdown engines support the [Basic Syntax](https://daringfireball.net/projects/markdown/syntax) designed by Markdown inventor John Gruber, but different Markdown processing engines have slightly different performance details, as follows Introduce them one by one.

## Heading

To create a title, just start with the hash sign `#`, the number of hash signs corresponds to the level of the title. For example, if you want to create a `<h3>`, you can start with three `#`: `### Three-level heading `. The title syntax using hash marks is called "ATX title" in the [CommonMark Specification](https://spec.commonmark.org).

| Markdown                   | HTML                           | Rendering results            |
| -------------------------- | ------------------------------ | ---------------------------- |
| `# Level 1 heading `       | `<h1>First-level heading</h1>` | <h1>First-level heading</h1> |
| `## Level 2 heading `      | `<h2>Level 2 heading</h2>`     | <h2>Level 2 heading</h2>     |
| `### Level 3 heading `     | `<h3>Level 3 heading</h3>`     | <h3>Level 3 heading</h3>     |
| `#### Level 4 heading `    | `<h4>Level 4 heading</h4>`     | <h4>Level 4 heading</h4>     |
| `###### Level 5 heading `  | `<h5>Level 5 heading</h5>`     | <h5>Level 5 heading</h5>     |
| `####### Level 6 heading ` | ` <h6>Level 6 heading</h6>`    | <h6>Level 6 heading</h6>     |

### Heading optional syntax

In addition to using ATX headings, we can also use Setext headings: in the next line of the text, use one or more equal signs `=` to indicate the first-level heading, and one or more dashes `-` to indicate the second-level heading.

| Markdown                        | HTML                           | Rendering results                |
| ------------------------------- | ------------------------------ | -------------------------------- |
| First-level heading<br>======   | `<h1>First-level heading</h1>` | hhh <h1>First-level heading</h1> |
| Secondary Title<br>------------ | `<h2>Secondary Title</h2>`     | hhh <h2>Secondary Title</h2>     |

### Heading Best Practices

1. ATX headings between paragraphs are best separated by blank lines. Because some Markdown engines do not recognize the title syntax that lacks leading and trailing blank lines.

   | ✅ Safe                                                                            | ❌ Unsafe                                                             |
   | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
   | This is a paragraph.<br /><br /># First level heading<br /><br />Another paragraph. | This is a paragraph.<br /># First level heading<br />Another paragraph |
2. **Be sure to add a space after the hash sign of the ATX heading**

   | ✅ Safe              | ❌ Unsafe            |
   | --------------------- | --------------------- |
   | # First-level heading | # First-level heading |
3. Try not to use Setext grammar to write headings, because Setext grammar can only write to secondary headings

## Paragraph

Use blank lines to separate text.

| Markdown                                                                           | HTML                                                                                        | Rendering results                                                                     |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| I love using Markdown.<br /><br />I will use Markdown to typeset all my documents. | `<p>I like to use Markdown. `<br>`<p>I will use Markdown to typeset all my documents. </p>` | <p>I like to use Markdown.</p><p>I will use Markdown to typeset all my documents.</p> |

### Paragraph best practices

1. Do not use spaces or tabs (`\t` is the Tab key) to indent the beginning of the paragraph, otherwise it may be rendered as a code block.

   | ✅ Safe                                                                    | ❌ Unsafe                                                 |
   | --------------------------------------------------------------------------- | ---------------------------------------------------------- |
   | Do not indent the beginning.<br><br>Just keep the left alignment like this. | The beginning indentation may be rendered as a code block. |

2. In traditional Chinese typesetting, there is a habit of "blank two spaces" at the beginning of a paragraph. You can use full-width spaces `　` or HTML entities `&emsp;`. It is recommended not to leave two spaces in the typeset of articles in the field of science and technology.

## Break

If you need to wrap the text `<br>`, you can add two or more spaces at the end of the text and press Enter.

| Markdown                                            | HTML                                                           | Rendering results                                   |
| --------------------------------------------------- | -------------------------------------------------------------- | --------------------------------------------------- |
| This is the first line.<br>This is the second line. | `<p>This is the first line. <br>This is the second line. </p>` | This is the first line.<br>This is the second line. |

### Best Practices for Breaking Lines

At present, most Markdown engines will automatically convert the newline character `\n` to `<br>`, that is, soft line feed to hard line feed. So although it is safe to write two or more spaces at the end, it may also cause some minor problems: the trailing space is not visible in some editors; accidentally or habitually pressing it will cause wrong typeset. Because of these minor problems, it may be the safest way to use `<br>` to wrap lines, but it is not very elegant. In addition, in the CommonMark specification, you can use a backslash `\` at the end of the text to break lines, but I don't recommend this way of writing.

In summary, my suggestion is to **do not use trailing spaces, `\` or `<br>`**, because almost all Markdown engines now basically support soft line breaks to hard line breaks.

## Bold and emphasize

Bold corresponds to bold, and emphasis corresponds to italics.

### Bold

To bold text, you can use two asterisks `**` or two underscores `__` to wrap the text to be bolded.

| Markdown                         | HTML                                       | Rendering results                         |
| -------------------------------- | ------------------------------------------ | ----------------------------------------- |
| Bold the text\*\*Bold\*\*A click | `Bold the text <strong>Bold</strong> once` | Make the text<strong>Bold</strong> once   |
| Make the text\_\_ bold\_\_ once  | `Make the text <strong>bold</strong> once` | Make the text<strong> bold </strong> once |

#### Bold best practice

The difference between using asterisks for bold and underscores is that spaces can be added before and after the asterisk, but underscores must be added.

| ✅ Safe                               | ❌ Unsafe                              |
| -------------------------------------- | --------------------------------------- |
| `Asterisk **Bold** No spaces required` | `No spaces underscore __Bold__ invalid` |

### Emphasize

To emphasize text, you can use an asterisk `*` or an underscore `_` to wrap the text to be emphasized.

| Markdown                        | HTML                               | Rendering results                |
| ------------------------------- | ---------------------------------- | -------------------------------- |
| Put the text\*emphasized\* once | `<em>emphasize the text</em> once` | <em>emphasize the text</em> once |
| Put the text\_emphasized\_ once | `<em>emphasize the text</em> once` | <em>emphasize</em> the text once |

#### Emphasize best practices

Similar to bold, spaces can be used before and after the asterisk, but the underscore must be added.

| ✅ Safe                               | ❌ Unsafe                             |
| -------------------------------------- | -------------------------------------- |
| `asterisk *emphasis*no space required` | `no space underscore_emphasis_invalid` |

### Bold and emphasize

If you need to emphasize the text while bolding it, you can use three asterisks `***` or three underscores `___` to wrap the text to be emphasized.

| Markdown                                                 | HTML                                                                                             | Rendering results                                                           |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| Example of***bolding and emphasizing*** at the same time | `Example of <strong><em>bolding and emphasizing at the same time</em></strong>`                  | At the same time<strong><em>bolding and emphasizing </em></strong> Examples |
| Example of bolding and emphasizing ___ at the same time  | `Example of <strong><em>bolding and emphasizing at the same time</em></strong> at the same time` | <strong><em>Bolding and emphasizing at the same time</em></strong> example  |
| At the same time__*Bold and emphasized*__ example        | `At the same time <strong><em>Bold and emphasized</em></strong> example`                         | At the same time<strong><em>Bold and emphasized</em></strong> example       |
| At the same time**_Bold and emphasized_** example        | `At the same time <strong><em>Bold and emphasized</em></strong> example`                         | At the same time<strong><em>Bold and emphasized</em></strong> Examples      |
| Asterisk***can be omitted*** plus space                  | `Asterisk<strong><em>can be omitted</em></strong>Add space`                                      | Asterisk<strong><em>can be omitted</em ></strong>Add space                  |

## Block Quote

To create a block quote `<blockquote>`, just add a greater than sign `>` before the paragraph.

```markdown
> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me
```

Rendering result

> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me

### Segment within block quote

If you need to segment, you can add a `>` before the blank line of the segment.

```markdown
> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me
```

Rendering result:

> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me

### Nested block quotes

Block quotes can be nested, adding two greater than signs `>>` before the paragraph to indicate two levels of nesting.

```markdown
> Block quoted paragraph
>
>> Nested block quotes
```

### Block quote contains other elements

Block quotes can contain most other syntax elements. The CommonMark specification defines a block reference as a container block. The container block can contain any block-level element and row-level element, which means that a block reference can contain any other elements.

```markdown
> ### The heading is a leaf block element
>
> * List item one is a container block element
> * List item two is also a container block element
>
> **Bold** and *Emphasis* are row-level elements.
```

Rendering result:

> ### The heading is a leaf block element
>
> * List item one is a container block element
> * List item two is also a container block element
>
> **Bold** and *Emphasis* are row-level elements.

## List

The list is divided into an ordered list and an unordered list. Lists in Markdown can only contain list item elements. List items, like block references, are container blocks. In other words, list items can contain any other elements.

### Ordered List

An ordered list can be created by using Arabic numerals followed by `.` or `)`, and the numbers do not have to be consecutively incremented.

| Markdown                                 | HTML                                                    |
| ---------------------------------------- | ------------------------------------------------------- |
| 1. List item one<br>2. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| 1. List item one<br>1. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| 1. List item one<br>3. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |

### Unordered List

Unordered lists can start with a dash `-`, an asterisk `*`, or a plus sign `+`, followed by a space to separate the text content.

| Markdown                               | HTML                                                    |
| -------------------------------------- | ------------------------------------------------------- |
| -List item one<br>- List item two<br>  | `<ul><li>List item one</li><li>List item two</li></ul>` |
| * List item one<br>* List item two<br> | `<ul><li>List item one</li><li>List item two</li></ul>` |
| + List item one<br>+ List item two<br> | `<ul><li>List item one</li><li>List item two</li></ul>` |

### List item contains other elements

List items can contain any other elements, such as paragraphs, block quotes, code blocks, pictures, etc. The point of use is that the starting character of the element to be included should be "aligned" with the starting content of the list item.

#### List item contains paragraph

```markdown
* List item one
* The first paragraph of list item two
  
  This is the second paragraph
* List item three
```

Rendering result:

* List item one
* The first paragraph of list item two

  This is the second paragraph
* List item three

#### List item contains block quote

```markdown
* List item one
* The first paragraph of list item two
  
  > The second paragraph is a block quote
* List item three
```

Rendering result:

* List item one
* The first paragraph of list item two
  > The second paragraph is a block quote
  >
* List item three

#### List item contains code block

````markdown
* List item one
* The first paragraph of list item two
  
   ```
  Here is the code block
  echo Hello, world!
   ```
* List item three
````

Rendering result:

* List item one
* The first paragraph of list item two
  ```
  Here is the code block
  echo Hello, world!
  ```
* List item three

#### List item contains pictures

````markdown
* List item one
* The first paragraph of list item two
  
  ![B3log](https://static.b3log.org/images/brand/b3log-128.png "B3log Open Source Community")
* List item three
````

Rendering result:

* List item one
* The first paragraph of list item two

  ![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)
* List item three

## Code

The code can be wrapped with backticks span</code>.

| Markdown                           | HTML                                     | Rendering results                        |
| ---------------------------------- | ---------------------------------------- | ---------------------------------------- |
| The command to list files is\`ls\` | The command to list files isspan</code>` | The command to list files is span</code> |

### Escaping backticks

If you need to display the backquote, you can use the escape character `\` to escape the backquote.

| Markdown          | HTML        | Rendering results |
| ----------------- | ----------- | ----------------- |
| Type a backtick\` | span</code> | Type a backtick ` |

### Code block

Code blocks can be indented with four spaces or tabs `\t`.

```markdown
    <html>
      <head>
      </head>
    </html>
```

Rendering result:

```
<html>
  <head>
  </head>
</html>
```

**It is recommended to use fence code block syntax to typeset code blocks**, that is, use span</code> to wrap the code block and specify the syntax highlighting language:

````markdown
```html
<html>
  <head>
  </head>
</html>
```
````

## Thematic breaks

Create a dividing line with three or more asterisks `***`, dashes `---`, or underscores `___`.

```markdown
***
---
___
```

Rendering result:

---

## Hyperlink

Create a hyperlink by `[link text](URL)`.

```markdown
We are from the niche open source community [B3log](https://b3log.org).
```

Rendering result:

We are from the niche open source community [B3log](https://b3log.org).

### Add hyperlink title

The link title is optional and is enclosed in double quotes after the URL in parentheses. When the mouse is moved over the hyperlink, the title content will appear.

```markdown
We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").
```

Rendering result:

We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").

### URL and email address

If you want to display the URL or email address directly, you can use `<` and `>` to wrap the URL or email address.

```markdown
<https://b3log.org>

<os@b3log.org>
```

Most Markdown engines also support automatic conversion, so you can omit `<>`:

```markdown
https://b3log.org

os@b3log.org
```

### Hyperlink format typeset

Hyperlinks can be used together with element structures such as bold emphasis, code, etc.

```markdown
We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).
```

Rendering result:

We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).

### Quote style hyperlink

Use citation style hyperlinks to make the original Markdown easier to read. The citation style hyperlink is divided into two parts: link reference and link definition.

#### Link reference

A link reference is used where a hyperlink needs to be inserted. It consists of two sets of square brackets. The first set of square brackets is used to specify the link text, the second set of square brackets is used to specify the link identifier, and the link identifier points to the link definition.

```markdown
[Link Text][Link Label]

[Link Label]: https://b3log.org
```

Rendering result:

[Link Text][Link Label]

The link reference can also consist of only a set of square brackets, in which case the link identifier will be used for the link text.

```markdown
[Link Label]

[Link Label]: https://b3log.org
```

Rendering result:

[Link Label]

#### Link definition

The link definition consists of three parts:

1. Square brackets wrap to define the link identifier, followed by a colon `:`
2. URL can be written directly or wrapped in angle brackets `<>`
3. Link title, this part is optional and can be wrapped in double quotes, single quotes or parentheses

```markdown
[Link ID]: https://b3log.org
[Link ID]: <https://b3log.org>
[Link logo]: https://b3log.org "B3log open source"
[Link logo]: https://b3log.org'B3log open source'
[Link logo]: https://b3log.org (B3log open source)
```

The link definition can be placed anywhere in the entire Markdown text. Some people are accustomed to putting it after the quoted paragraph, and some people are accustomed to putting it at the end of the text.

### Hyperlink Best Practice

The English content is naturally separated by spaces, so there is no separation problem when using automatic hyperlinks. But Chinese will have this problem, such as:

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```

This content will render incorrectly on many Markdown engines. In order to ensure compatibility as much as possible, consider using spaces to separate:

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```

Or use angle brackets `<>` to wrap:

```markdown
Our website is <https://b3log.org> Open source enthusiasts are welcome to join!
```

So you can get the expected rendering result:

Our website is [https://b3log.org](https://b3log.org) Open source enthusiasts are welcome to join!

## Picture

Use the exclamation mark `!` followed by a hyperlink to render the image.

```markdown
![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)
```

Rendering result:

![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)

### Hyperlink nested image

If you need to click on the picture to jump to the hyperlink, you only need to include the picture in the text part of the link.

```markdown
[![LianDi](https://static.b3log.org/images/brand/hacpai-128.png)](https://ld246.com)
```

Rendering result:

[![LianDi](https://static.b3log.org/images/brand/hacpai-128.png)](https://ld246.com)

## Escape character

You can use the backslash `\` to escape the following characters:

| Characters  | Chinese name               |
| ----------- | -------------------------- |
| `\`         | Backslash                  |
| span</code> | backtick                   |
| `*`         | Asterisk                   |
| `_`         | Underscore                 |
| `{}`        | curly braces               |
| `[]`        | Square brackets            |
| `()`        | Parentheses                |
| `#`         | hashtag                    |
| `+`         | plus sign                  |
| `-`         | dash (minus sign)          |
| `.`         | Point                      |
| `!`         | Exclamation mark           |
| span</code> | Vertical bar (pipe symbol) |

Almost all ASCII punctuation marks can be escaped with backslashes.

## Embed HTML

Markdown naturally supports embedding HTML code.

```markdown
**Markdown** and <em>HTML</em> mixed typesetting.
```

Rendering result:

**Markdown** and <em>HTML</em> mixed typesetting.

### Embedding HTML Best Practices

This is useful when you need to set the image size and font color, but we don’t recommend using HTML too much for typesetting, because this is actually not universal, because some Markdown engines filter some parts for security reasons Labels or attributes; secondly, because it is too Markdown!

Also, don’t embed Markdown in HTML, it won’t work:

```markdown
<p>**Bold** will not take effect. </p>
```

Rendering result:

<p>**Bold** will not take effect. </p>


## Summary

Good use of blank lines and spaces is the key to Markdown typesetting. In many cases, it is because of missing blank lines or spaces that unexpected rendering results are produced.

With the improvement of the CommonMark/GFM specification and gradually becoming the industry's unified Markdown standard, more and more Markdown engines have implemented the specification. It is recommended that Markdown users should follow the specifications as much as possible for typesetting, so as to avoid detail rendering problems to the greatest extent.

## Reference

* [Markdown Guide](https://www.markdownguide.org)
* [CommonMark Spec](https://spec.commonmark.org)

[Link Label]: https://b3log.org

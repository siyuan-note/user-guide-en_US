> This article mainly introduces the extended syntax of Markdown, please refer to ((20200924085905-kxykwln "Markdown Basic Syntax")).
> The concise version of the syntax can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).

## Overview

In [Basic Syntax](https://ld246.com/article/1583129520165), we introduced the most commonly used typesetting usage of Markdown, but sometimes the basic syntax is not enough to meet the more complex typesetting needs, then you need to use the extended syntax up.

Some individuals and organizations have extended the basic syntax, such as the introduction of tables, fenced code blocks, code highlighting, automatic links, footnotes and directories, etc. These extended syntax require specific Markdown engines to support.

## Availability

Not all Markdown engines support the extended syntax, so before using the extended syntax, you may need to confirm the specific Markdown engine support, and browse their usage documents to understand which elements can be supported.

### Mainstream Markdown syntax specifications

Markdown syntax specifications have not yet formed a standard. The following syntax specifications are more mainstream.

* [CommonMark](https://commonmark.org)
* [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm)
* [Markdown Extra](https://michelf.ca/projects/php-markdown/extra)
* [MultiMarkdown](https://fletcherpenney.net/multimarkdown)
* [R Markdown](https://rmarkdown.rstudio.com)

Among them, CommonMark and GFM are currently the most likely to be standardized. GFM is an extension of GitHub based on CommonMark. It is almost a de facto standard. For the interpretation of CommonMark specifications, please refer to [here](https://ld246.com/article/1566893557720).

### Markdown engine

[Here](https://github.com/markdown/markdown.github.com/wiki/Implementations) lists a lot of Markdown engine implementations, most of them support extended syntax by setting switches, the specific details Please refer to their documentation.

## Form

Use dash `---` to separate the header and body of the table, and use the vertical bar `|` to separate the columns. The vertical bars at the beginning and end of each row are optional.

```markdown
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```

Rendering result:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

Each column does not have to be aligned, the following example can also be rendered:

```markdown
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```

### Table alignment

If you need to align the table content to the left, center or right, you can add a colon `:` to `---`. The colon only appears on the left to indicate left alignment, on both sides indicates center alignment, and only on the right indicates right alignment.

```markdown
| Syntax | Description | Test Text |
| :--- | :----: | ---: |
| Header | Title | Here's this |
| Paragraph | Text | And more |
```

Rendering result:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text    |    And more |

### Table content typeset

The content in the table can also be typeset, such as bolding, emphasizing text, inserting hyperlinks, etc. However, it is limited to the use of "span-level elements" for typesetting, and "block-level elements" cannot be used, such as headings, block quotes, lists, dividers, etc.

### Table content escape vertical bar

If you need to use the vertical bar `|` in the table content, you need to escape it. You can use `\|` to escape, but it is safer to write a vertical line HTML entity to represent `&#124;`, because some Markdown engines can’t handle the `\|` in the table content correctly.

## Fence code block

In [Basic Syntax](https://ld246.com/article/1583129520165), we introduced that code blocks can be typeset by indentation with four spaces or tabs `\t`. But we recommend using the fenced code block syntax, that is, use three or more backquotes span</code> or three or more squiggles `~~~` to wrap the code block content:

````markdown
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

Rendering result:

```text
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

If you need to display the original Markdown of the code block (like the example shown above), you can start with a larger number of backticks at the outermost layer, and the number of closed backticks is equal to the number at the beginning.

``````markdown
````
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
``````

### Code block syntax highlighting

The syntax highlighting of code blocks requires the support of the Markdown engine, and is typeset by adding the name of the programming language after the opening backquote.

````markdown
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

Rendering result:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## Footnotes

Footnotes are used to add details or references at the end of the text, so that the body of the article will look more concise and clear. After creating a footnote, a superscript number link will appear in the text where the footnote is quoted, and the reader will jump to the corresponding position defined by the footnote at the end of the text after clicking.

Footnote quotes are created by `[^identifier]`. The identifier part can be numbers or text, but cannot contain spaces or tabs. Identifiers are only used for associative references and definitions. When rendering, they will automatically be rendered in increasing numbers according to the order of the footnote definition. But this is not absolute, some Markdown engines also use the identifier part for rendering.

The footnote definition is created using `[^identifier]:`, and the detailed description or reference that needs to be added is after the colon. The footnote definition does not have to be placed at the end of the entire Markdown text, it can also work if it is sandwiched between paragraphs, lists, or block quotes.

```markdown
Here is a footnote reference [^1], and here is another footnote reference [^bignote].

[^1]: The first footnote definition.
[^bignote]: The footnote definition can use multiple paragraphs.

    Indented paragraphs are included in this footnote definition.

    ```
    You can use code blocks.
    ```

    There are other line-level typesetting syntaxes, such as **bold** and [link](https://b3log.org).
```

## Heading designation ID {#heading-ids}

Some Markdown engines support specifying an ID for the title, while others automatically add an ID. The function of the title ID is to allow other places to jump directly to the title through the anchor point. The syntax of title designation ID is to wrap the ID in curly braces after the title.

```markdown
### This is a title {#custom-id}
```

Rendered HTML:

```html
<h3 id="custom-id">This is a headline</h3>
```

### Link to the specified heading

You can link to the title in the text through the hyperlink syntax.

| Markdown                                 | HTML                                                | Rendering results                                                                                         |
| ---------------------------------------- | --------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `[Heading Designation ID](#heading-ids)` | `<a href="#heading-ids">Heading Designation ID</a>` | [Heading Designation ID](%5Bhttps://ld246.com/%5D(https://ld246.com/)) article/1583305480675#heading-ids) |

If you need to link to the title of another page, you need to write the full link path, such as `[title designation ID](https://ld246.com/article/1583305480675#heading-ids)`.

## Strikethrough

The text can be crossed out with a strikethrough, and the result will be typeset~just like this~. To create a strikethrough, you can wrap the text to be deleted with one `~` or two wavy lines `~~`.

```
~~ The earth is flat. ~~ Now we know that the earth is round.
```

Rendering result:

~~ The earth is flat. ~~ Now we know that the earth is round.

## task list

Render task list items by adding `[ ]` or `[x]` to ordinary list items.

```markdown
-[x] To-do one
-[] To-do list two
-[] To-do list three
```

Rendering result:

-[X] To-do one
-[] To-do list two
-[] To-do list three

## Emoji

There are two ways to use Emoji: directly input Emoji characters or use the alias `:smile:`. For direct input, you need to make sure that the current editor uses UTF-8 encoding.

```markdown
The weather is really nice today :sunny:
Flower 🌻 smile at me
```

Rendering result:

The weather is really nice today ☀️
Flower 🌻 smile at me

## Prohibit automatic linking

Most Markdown engines enable automatic linking by default, so when we want to render a link as plain text, we need to turn it into code:

```markdown
`https://b3log.org`
```

Rendering result:

`https://b3log.org`

## to sum up

Try to use only the extended syntax defined by GFM, so that you can maximize the support of many Markdown engines and get consistent rendering results.

## Reference

* [Markdown Guide](https://www.markdownguide.org)
* [CommonMark Spec](https://spec.commonmark.org)

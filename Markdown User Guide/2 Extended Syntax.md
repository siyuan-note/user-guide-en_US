> This article mainly introduces the extended syntax of Markdown, please refer to ((20200924085905-kxykwln "Markdown Basic Syntax")).
> The concise version of the syntax can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).
> {: id="20210104091506-xm7temh"}
{: id="20210104091506-x1wsday"}

## Overview
{: id="20210104091506-pyrebmy"}

In [Basic Syntax](https://ld246.com/article/1583129520165), we introduced the most commonly used typesetting usage of Markdown, but sometimes the basic syntax is not enough to meet the more complex typesetting needs, then you need to use the extended syntax up.
{: id="20210104091506-pmey9fk"}

Some individuals and organizations have extended the basic syntax, such as the introduction of tables, fenced code blocks, code highlighting, automatic links, footnotes and directories, etc. These extended syntax require specific Markdown engines to support.
{: id="20210104091506-6j34tm6"}

## Availability
{: id="20210104091506-r3oyhsq"}

Not all Markdown engines support the extended syntax, so before using the extended syntax, you may need to confirm the specific Markdown engine support, and browse their usage documents to understand which elements can be supported.
{: id="20210104091506-bo8an6u"}

### Mainstream Markdown syntax specifications
{: id="20210104091506-vkngv7e"}

Markdown syntax specifications have not yet formed a standard. The following syntax specifications are more mainstream.
{: id="20210104091506-hslzlxn"}

* {: id="20210104091506-hperija"}[CommonMark](https://commonmark.org)
* {: id="20210104091506-3k4od60"}[GitHub Flavored Markdown (GFM)](https://github.github.com/gfm)
* {: id="20210104091506-7q0kqfq"}[Markdown Extra](https://michelf.ca/projects/php-markdown/extra)
* {: id="20210104091506-b7o111b"}[MultiMarkdown](https://fletcherpenney.net/multimarkdown)
* {: id="20210104091506-po4zxky"}[R Markdown](https://rmarkdown.rstudio.com)
{: id="20210104091506-zbse03w"}

Among them, CommonMark and GFM are currently the most likely to be standardized. GFM is an extension of GitHub based on CommonMark. It is almost a de facto standard. For the interpretation of CommonMark specifications, please refer to [here](https://ld246.com/article/1566893557720).
{: id="20210104091506-9qhz78h"}

### Markdown engine
{: id="20210104091506-hxeynpa"}

[Here](https://github.com/markdown/markdown.github.com/wiki/Implementations) lists a lot of Markdown engine implementations, most of them support extended syntax by setting switches, the specific details Please refer to their documentation.
{: id="20210104091506-id5228x"}

## Form
{: id="20210104091506-d9hbgbf"}

Use dash `---` to separate the header and body of the table, and use the vertical bar `|` to separate the columns. The vertical bars at the beginning and end of each row are optional.
{: id="20210104091506-b6zd7p4"}

```markdown
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```
{: id="20210104091506-4diovxb"}

Rendering result:
{: id="20210104091506-fwgkzum"}

| Syntax    | Description |
| ----------- | ------------- |
| Header    | Title       |
| Paragraph | Text        |
{: id="20210104091506-dqijstn"}

Each column does not have to be aligned, the following example can also be rendered:
{: id="20210104091506-9akqmax"}

```markdown
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```
{: id="20210104091506-yd9orlr"}

### Table alignment
{: id="20210104091506-f982iwf"}

If you need to align the table content to the left, center or right, you can add a colon `:` to `---`. The colon only appears on the left to indicate left alignment, on both sides indicates center alignment, and only on the right indicates right alignment.
{: id="20210104091506-bigacfq"}

```markdown
| Syntax | Description | Test Text |
| :--- | :----: | ---: |
| Header | Title | Here's this |
| Paragraph | Text | And more |
```
{: id="20210104091506-g4ckryl"}

Rendering result:
{: id="20210104091506-z6bxo73"}

| Syntax    | Description |   Test Text |
| :---------- | :-----------: | ------------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text    |    And more |
{: id="20210104091506-tasafr9"}

### Table content typeset
{: id="20210104091506-fm8h3l6"}

The content in the table can also be typeset, such as bolding, emphasizing text, inserting hyperlinks, etc. However, it is limited to the use of "span-level elements" for typesetting, and "block-level elements" cannot be used, such as headings, block quotes, lists, dividers, etc.
{: id="20210104091506-ucze39k"}

### Table content escape vertical bar
{: id="20210104091506-9675br0"}

If you need to use the vertical bar `|` in the table content, you need to escape it. You can use `\|` to escape, but it is safer to write a vertical line HTML entity to represent `&#124;`, because some Markdown engines can’t handle the `\|` in the table content correctly.
{: id="20210104091506-yfgxbwf"}

## Fence code block
{: id="20210104091506-rkbggi9"}

In [Basic Syntax](https://ld246.com/article/1583129520165), we introduced that code blocks can be typeset by indentation with four spaces or tabs `\t`. But we recommend using the fenced code block syntax, that is, use three or more backquotes span</code> or three or more squiggles `~~~` to wrap the code block content:
{: id="20210104091506-eg9i737"}

````markdown
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
{: id="20210104091506-kf2431x"}

Rendering result:
{: id="20210104091506-dwzhwlh"}

```text
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
{: id="20210104091506-pwlvhbg"}

If you need to display the original Markdown of the code block (like the example shown above), you can start with a larger number of backticks at the outermost layer, and the number of closed backticks is equal to the number at the beginning.
{: id="20210104091506-g6dmqwr"}

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
{: id="20210104091506-sxviri0"}

### Code block syntax highlighting
{: id="20210104091506-zcjfbpi"}

The syntax highlighting of code blocks requires the support of the Markdown engine, and is typeset by adding the name of the programming language after the opening backquote.
{: id="20210104091506-uxryonj"}

````markdown
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
{: id="20210104091506-x9lm3vd"}

Rendering result:
{: id="20210104091506-pquyv02"}

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
{: id="20210104091506-f3hku4p"}

## Footnotes
{: id="20210104091506-48yjtz3"}

Footnotes are used to add details or references at the end of the text, so that the body of the article will look more concise and clear. After creating a footnote, a superscript number link will appear in the text where the footnote is quoted, and the reader will jump to the corresponding position defined by the footnote at the end of the text after clicking.
{: id="20210104091506-le2n6zy"}

Footnote quotes are created by `[^identifier]`. The identifier part can be numbers or text, but cannot contain spaces or tabs. Identifiers are only used for associative references and definitions. When rendering, they will automatically be rendered in increasing numbers according to the order of the footnote definition. But this is not absolute, some Markdown engines also use the identifier part for rendering.
{: id="20210104091506-zeborrn"}

The footnote definition is created using `[^identifier]:`, and the detailed description or reference that needs to be added is after the colon. The footnote definition does not have to be placed at the end of the entire Markdown text, it can also work if it is sandwiched between paragraphs, lists, or block quotes.
{: id="20210104091506-zrep5fd"}

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
{: id="20210104091506-2x7281s"}

## Heading designation ID {#heading-ids}
{: id="20210104091506-w7xx70p"}

Some Markdown engines support specifying an ID for the title, while others automatically add an ID. The function of the title ID is to allow other places to jump directly to the title through the anchor point. The syntax of title designation ID is to wrap the ID in curly braces after the title.
{: id="20210104091506-ctftegy"}

```markdown
### This is a title {#custom-id}
```
{: id="20210104091506-koumsx1"}

Rendered HTML:
{: id="20210104091506-lp8q4om"}

```html
<h3 id="custom-id">This is a headline</h3>
```
{: id="20210104091506-qug42ky"}

### Link to the specified heading
{: id="20210104091506-xyy3us3"}

You can link to the title in the text through the hyperlink syntax.
{: id="20210104091506-gabdho9"}

| Markdown                                 | HTML                                                | Rendering results                                                                                         |
| ------------------------------------------ | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `[Heading Designation ID](#heading-ids)` | `<a href="#heading-ids">Heading Designation ID</a>` | [Heading Designation ID](%5Bhttps://ld246.com/%5D(https://ld246.com/)) article/1583305480675#heading-ids) |
{: id="20210104091506-8r2z6b2"}

If you need to link to the title of another page, you need to write the full link path, such as `[title designation ID](https://ld246.com/article/1583305480675#heading-ids)`.
{: id="20210104091506-2lewm8b"}

## Strikethrough
{: id="20210104091506-hbmllpb"}

The text can be crossed out with a strikethrough, and the result will be typeset~just like this~. To create a strikethrough, you can wrap the text to be deleted with one `~` or two wavy lines `~~`.
{: id="20210104091506-2hk04iz"}

```
~~ The earth is flat. ~~ Now we know that the earth is round.
```
{: id="20210104091506-u52ryzn"}

Rendering result:
{: id="20210104091506-016tb75"}

~~ The earth is flat. ~~ Now we know that the earth is round.
{: id="20210104091506-am88l0m"}

## task list
{: id="20210104091506-qotbyh1"}

Render task list items by adding `[ ]` or `[x]` to ordinary list items.
{: id="20210104091506-rkodhft"}

```markdown
-[x] To-do one
-[] To-do list two
-[] To-do list three
```
{: id="20210104091506-mxrft1x"}

Rendering result:
{: id="20210104091506-u2y9zfc"}

-[X] To-do one
-[] To-do list two
-[] To-do list three
{: id="20210104091506-3ykwokj"}

## Emoji
{: id="20210104091506-wlmix4m"}

There are two ways to use Emoji: directly input Emoji characters or use the alias `:smile:`. For direct input, you need to make sure that the current editor uses UTF-8 encoding.
{: id="20210104091506-e28ues1"}

```markdown
The weather is really nice today :sunny:
Flower 🌻 smile at me
```
{: id="20210104091506-gb4vl3l"}

Rendering result:
{: id="20210104091506-6ta1f4p"}

The weather is really nice today ☀️
Flower 🌻 smile at me
{: id="20210104091506-zk5mfob"}

## Prohibit automatic linking
{: id="20210104091506-3hshib5"}

Most Markdown engines enable automatic linking by default, so when we want to render a link as plain text, we need to turn it into code:
{: id="20210104091506-ehkrupo"}

```markdown
`https://b3log.org`
```
{: id="20210104091506-1b65bvv"}

Rendering result:
{: id="20210104091506-rr8d44a"}

`https://b3log.org`
{: id="20210104091506-aw779fe"}

## to sum up
{: id="20210104091506-on1gs9a"}

Try to use only the extended syntax defined by GFM, so that you can maximize the support of many Markdown engines and get consistent rendering results.
{: id="20210104091506-kklnr4q"}

## Reference
{: id="20210104091506-ae8ngus"}

* {: id="20210104091506-fjyy13g"}[Markdown Guide](https://www.markdownguide.org)
* {: id="20210104091506-yxj1mvp"}[CommonMark Spec](https://spec.commonmark.org)
{: id="20210104091506-ktn57af"}


{: id="20200924092619-pw51c0y" type="doc"}

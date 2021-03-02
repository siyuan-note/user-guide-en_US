> This article mainly introduces the basic syntax of Markdown, please refer to ((20200924092619-pw51c0y "Markdown Extended Syntax")).
> The concise version of the syntax can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).
> {: id="20210104091501-jmccakm" updated="20210302223818"}
{: id="20210104091501-9fffph9"}

## Overview
{: id="20210104091501-75f38dd"}

Almost all Markdown engines support the [Basic Syntax](https://daringfireball.net/projects/markdown/syntax) designed by Markdown inventor John Gruber, but different Markdown processing engines have slightly different performance details, as follows Introduce them one by one.
{: id="20210104091501-8e6d3fc"}

## Heading
{: id="20210104091501-h6z8ory"}

To create a title, just start with the hash sign `#`, the number of hash signs corresponds to the level of the title. For example, if you want to create a `<h3>`, you can start with three `#`: `### Three-level heading `. The title syntax using hash marks is called "ATX title" in the [CommonMark Specification](https://spec.commonmark.org).
{: id="20210104091501-d0usvhm"}

| Markdown                   | HTML                           | Rendering results            |
| ---------------------------- | -------------------------------- | ------------------------------ |
| `# Level 1 heading `       | `<h1>First-level heading</h1>` | <h1>First-level heading</h1> |
| `## Level 2 heading `      | `<h2>Level 2 heading</h2>`     | <h2>Level 2 heading</h2>     |
| `### Level 3 heading `     | `<h3>Level 3 heading</h3>`     | <h3>Level 3 heading</h3>     |
| `#### Level 4 heading `    | `<h4>Level 4 heading</h4>`     | <h4>Level 4 heading</h4>     |
| `###### Level 5 heading `  | `<h5>Level 5 heading</h5>`     | <h5>Level 5 heading</h5>     |
| `####### Level 6 heading ` | ` <h6>Level 6 heading</h6>`    | <h6>Level 6 heading</h6>     |
{: id="20210104091501-efc5m2y"}

### Heading optional syntax
{: id="20210104091501-7ufe1az"}

In addition to using ATX headings, we can also use Setext headings: in the next line of the text, use one or more equal signs `=` to indicate the first-level heading, and one or more dashes `-` to indicate the second-level heading.
{: id="20210104091501-1t6294v"}

| Markdown                        | HTML                           | Rendering results            |
| --------------------------------- | -------------------------------- | ------------------------------ |
| First-level heading<br>======   | `<h1>First-level heading</h1>` | <h1>First-level heading</h1> |
| Secondary Title<br>------------ | `<h2>Secondary Title</h2>`     | <h2>Secondary Title</h2>     |
{: id="20210104091501-i84lhwo"}

### Heading Best Practices
{: id="20210104091501-ncw0460"}

1. {: id="20210104091501-oxnjqh0"}ATX headings between paragraphs are best separated by blank lines. Because some Markdown engines do not recognize the title syntax that lacks leading and trailing blank lines.
   {: id="20210104091501-l935kik"}

   | ✅ Safe                                                                             | ❌ Unsafe                                                              |
   | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
   | This is a paragraph.<br /><br /># First level heading<br /><br />Another paragraph. | This is a paragraph.<br /># First level heading<br />Another paragraph |
   {: id="20210104091501-2ugpgmy"}
2. {: id="20210104091501-wy37912"}**Be sure to add a space after the hash sign of the ATX heading**
   {: id="20210104091501-9ksvi19"}

   | ✅ Safe               | ❌ Unsafe             |
   | ----------------------- | ----------------------- |
   | # First-level heading | # First-level heading |
   {: id="20210104091501-r36you0"}
3. {: id="20210104091501-h9pktfa"}Try not to use Setext syntax to write headings, because Setext syntax can only write to secondary headings
   {: id="20210104091501-mlvvlml"}
{: id="20210104091501-rhzv7zh"}

## Paragraph
{: id="20210104091501-hxma6h8"}

Use blank lines to separate text.
{: id="20210104091501-x4fxor6"}

| Markdown                                                                           | HTML                                                                                        | Rendering results                                                                     |
| ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| I love using Markdown.<br /><br />I will use Markdown to typeset all my documents. | `<p>I like to use Markdown. `<br>`<p>I will use Markdown to typeset all my documents. </p>` | <p>I like to use Markdown.</p><p>I will use Markdown to typeset all my documents.</p> |
{: id="20210104091501-b9v22t8"}

### Paragraph best practices
{: id="20210104091501-ey9w925"}

1. {: id="20210104091501-5w362yt"}Do not use spaces or tabs (`\t` is the Tab key) to indent the beginning of the paragraph, otherwise it may be rendered as a code block.
   {: id="20210104091501-ybuygap"}

   | ✅ Safe                                                                     | ❌ Unsafe                                                  |
   | ----------------------------------------------------------------------------- | ------------------------------------------------------------ |
   | Do not indent the beginning.<br><br>Just keep the left alignment like this. | The beginning indentation may be rendered as a code block. |
   {: id="20210104091501-vsp9ev4"}
2. {: id="20210104091501-9ul57kr"}In traditional Chinese typesetting, there is a habit of "blank two spaces" at the beginning of a paragraph. You can use full-width spaces `　` or HTML entities `&emsp;`. It is recommended not to leave two spaces in the typeset of articles in the field of science and technology.
   {: id="20210104091501-lryj8zl"}
{: id="20210104091501-99h5pgz"}

## Break
{: id="20210104091501-kidm0si"}

If you need to wrap the text `<br>`, you can add two or more spaces at the end of the text and press Enter.
{: id="20210104091501-6szn67b"}

| Markdown                                            | HTML                                                           | Rendering results                                   |
| ----------------------------------------------------- | ---------------------------------------------------------------- | ----------------------------------------------------- |
| This is the first line.<br>This is the second line. | `<p>This is the first line. <br>This is the second line. </p>` | This is the first line.<br>This is the second line. |
{: id="20210104091501-rrbd67z"}

### Best Practices for Breaking Lines
{: id="20210104091501-lcqygxs"}

At present, most Markdown engines will automatically convert the newline character `\n` to `<br>`, that is, soft line feed to hard line feed. So although it is safe to write two or more spaces at the end, it may also cause some minor problems: the trailing space is not visible in some editors; accidentally or habitually pressing it will cause wrong typeset. Because of these minor problems, it may be the safest way to use `<br>` to wrap lines, but it is not very elegant. In addition, in the CommonMark specification, you can use a backslash `\` at the end of the text to break lines, but I don't recommend this way of writing.
{: id="20210104091501-3aw8x5p"}

In summary, my suggestion is to **do not use trailing spaces, `\` or `<br>`**, because almost all Markdown engines now basically support soft line breaks to hard line breaks.
{: id="20210104091501-6xlbyzn"}

## Bold and emphasize
{: id="20210104091501-3jormnu"}

Bold corresponds to bold, and emphasis corresponds to italics.
{: id="20210104091501-b6rcwll"}

### Bold
{: id="20210104091501-6pa4jp1"}

To bold text, you can use two asterisks `**` or two underscores `__` to wrap the text to be bolded.
{: id="20210104091501-sug654k"}

| Markdown                     | HTML                                       | Rendering results                               |
| ------------------------------ | -------------------------------------------- | ------------------------------------------------- |
| Bold the text\*\*Bold\*\*A click | `Bold the text <strong>Bold</strong> once` | Make the text<strong>Bold</strong> once   |
| Make the text\_\_ bold\_\_ once  | `Make the text <strong>bold</strong> once` | Make the text<strong> bold </strong> once |
{: id="20210104091501-080wumx"}

#### Bold best practice
{: id="20210104091501-bgckoe7"}

The difference between using asterisks for bold and underscores is that spaces can be added before and after the asterisk, but underscores must be added.
{: id="20210104091501-pi250vy"}

| ✅ Safe                                | ❌ Unsafe                               |
| ---------------------------------------- | ----------------------------------------- |
| `Asterisk **Bold** No spaces required` | `No spaces underscore __Bold__ invalid` |
{: id="20210104091501-qrcce4s"}

### Emphasize
{: id="20210104091501-uwdyx64"}

To emphasize text, you can use an asterisk `*` or an underscore `_` to wrap the text to be emphasized.
{: id="20210104091501-1p97x3o"}

| Markdown                      | HTML                               | Rendering results                  |
| ------------------------------- | ------------------------------------ | ------------------------------------ |
| Put the text\*emphasized\* once | `<em>emphasize the text</em> once` | <em>emphasize the text</em> once |
| Put the text\_emphasized\_ once | `<em>emphasize the text</em> once` | <em>emphasize</em> the text once |
{: id="20210104091501-cggneqg"}

#### Emphasize best practices
{: id="20210104091501-zx0pcw7"}

Similar to bold, spaces can be used before and after the asterisk, but the underscore must be added.
{: id="20210104091501-mjr9ymr"}

| ✅ Safe                                | ❌ Unsafe                              |
| ---------------------------------------- | ---------------------------------------- |
| `asterisk *emphasis*no space required` | `no space underscore_emphasis_invalid` |
{: id="20210104091501-otnuufk"}

### Bold and emphasize
{: id="20210104091501-oi5e9nw"}

If you need to emphasize the text while bolding it, you can use three asterisks `***` or three underscores `___` to wrap the text to be emphasized.
{: id="20210104091501-v7z4vvy"}

| Markdown                                             | HTML                                                                                        | Rendering results                                                                |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Example of \*\*\*bold and emphasize\*\*\* at the same time | `Example of <strong><em>bold and emphasize</em></strong> at the same time`                  | Example of <strong><em>bold and emphasize</em></strong> at the same time |
| Example of \_\_\_bold and emphasize\_\_\_ at the same time | `Example of <strong><em>bold and emphasize at the same time</em></strong> at the same time` | Example of <strong><em>bold and emphasize</em></strong> at the same time |
| At the same time \_\_\*bold and emphasize\*\_\_ example    | `Example of <strong><em>bold and emphasize</em></strong> at the same time`                  | Example of <strong><em>bold and emphasize</em></strong> at the same time |
| At the same time \*\*\_bold and emphasize\_\*\* example    | `Example of <strong><em>bold and emphasize</em></strong> at the same time`                  | Example of <strong><em>bold and emphasize</em></strong> at the same time |
| Asterisk***can be omitted***plus space               | `Asterisk<strong><em>can be omitted</em></strong>plus space`                                | Asterisk<strong><em>can be omitted</em ></strong>plus space              |
{: id="20210104091501-esy36zo"}

## Blockquote
{: id="20210104091501-y113sx6"}

To create a block quote `<blockquote>`, just add a greater than sign `>` before the paragraph.
{: id="20210104091501-loevr1x"}

```markdown
> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me
```
{: id="20210104091501-6tirklo"}

Rendering result
{: id="20210104091501-lu9y4jr"}

> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me
> {: id="20210104091501-u55enn2"}
{: id="20210104091501-f9avu3c"}

### Segment within blockquote
{: id="20210104091501-bwzt7j1"}

If you need to segment, you can add a `>` before the blank line of the segment.
{: id="20210104091501-akmhmn3"}

```markdown
> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me
```
{: id="20210104091501-ctsd448"}

Rendering result:
{: id="20210104091501-b3jxc33"}

> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
> {: id="20210104091501-o41cqg6"}
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me
> {: id="20210104091501-6oy8obg"}
{: id="20210104091501-zs75owc"}

### Nested block quotes
{: id="20210104091501-wroela6"}

Block quotes can be nested, adding two greater than signs `>>` before the paragraph to indicate two levels of nesting.
{: id="20210104091501-hrv6j8m"}

```markdown
> Block quoted paragraph
>
>> Nested block quotes
```
{: id="20210104091501-hq4vvvx"}

### Block quote contains other elements
{: id="20210104091501-822g5u6"}

Block quotes can contain most other syntax elements. The CommonMark specification defines a block reference as a container block. The container block can contain any block-level element and row-level element, which means that a block reference can contain any other elements.
{: id="20210104091501-sfex5e0"}

```markdown
> ### The heading is a leaf block element
>
> * List item one is a container block element
> * List item two is also a container block element
>
> **Bold** and *Emphasis* are row-level elements.
```
{: id="20210104091501-u5lr7qr"}

Rendering result:
{: id="20210104091501-14f7qo5"}

> ### The heading is a leaf block element
> {: id="20210104091501-t95h7c4"}
>
> * {: id="20210104091501-gve1v34"}List item one is a container block element
>   {: id="20210216134045-jecq2dp"}
> * {: id="20210104091501-bna0tdv"}List item two is also a container block element
>   {: id="20210216134045-59ay87p"}
> {: id="20210104091501-zj8vhx2"}
>
> **Bold** and *Emphasis* are row-level elements.
> {: id="20210104091501-0x3sil5"}
{: id="20210104091501-0hamtw1"}

## List
{: id="20210104091501-nnrgu57"}

The list is divided into an ordered list and an unordered list. Lists in Markdown can only contain list item elements. List items, like block references, are container blocks. In other words, list items can contain any other elements.
{: id="20210104091501-rqs410w"}

### Ordered List
{: id="20210104091501-ryfwju0"}

An ordered list can be created by using Arabic numerals followed by `.` or `)`, and the numbers do not have to be consecutively incremented.
{: id="20210104091501-zpa0tyw"}

| Markdown | HTML                                                    |
| ---------- | --------------------------------------------------------- |
| <br><br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| <br><br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| <br><br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
{: id="20210104091501-gm9c7t9"}

### Unordered List
{: id="20210104091501-lopyz5l"}

Unordered lists can start with a dash `-`, an asterisk `*`, or a plus sign `+`, followed by a space to separate the text content.
{: id="20210104091501-qwgzyud"}

| Markdown               | HTML                                                    |
| ------------------------ | --------------------------------------------------------- |
| -List item one<br><br> | `<ul><li>List item one</li><li>List item two</li></ul>` |
| <br><br>               | `<ul><li>List item one</li><li>List item two</li></ul>` |
| <br><br>               | `<ul><li>List item one</li><li>List item two</li></ul>` |
{: id="20210104091501-dklh9ct"}

### List item contains other elements
{: id="20210104091501-74nhyc4"}

List items can contain any other elements, such as paragraphs, block quotes, code blocks, pictures, etc. The point of use is that the starting character of the element to be included should be "aligned" with the starting content of the list item.
{: id="20210104091501-rw457dw"}

#### List item contains paragraph
{: id="20210104091501-tc3yt11"}

```markdown
* List item one
* The first paragraph of list item two
  
  This is the second paragraph
* List item three
```
{: id="20210104091501-sqtay2b"}

Rendering result:
{: id="20210104091501-krclbjv"}

* {: id="20210104091501-4z6ofzx"}List item one
  {: id="20210104091501-cep89do"}
* {: id="20210104091501-inp8585"}The first paragraph of list item two
  {: id="20210104091501-alyy8gu"}

  This is the second paragraph
  {: id="20210104091501-xbzbdka"}
* {: id="20210104091501-1ywieep"}List item three
  {: id="20210104091501-ou35dfi"}
{: id="20210104091501-yk3r52b"}

#### List item contains block quote
{: id="20210104091501-5p32fd8"}

```markdown
* List item one
* The first paragraph of list item two
  
  > The second paragraph is a block quote
* List item three
```
{: id="20210104091501-hz5a05r"}

Rendering result:
{: id="20210104091501-sqmwgwm"}

* {: id="20210104091501-2ctsuyv"}List item one
  {: id="20210216134045-q60t6ge"}
* {: id="20210104091501-b1oz2mx"}The first paragraph of list item two
  {: id="20210216134045-wzj7hts"}

  > The second paragraph is a block quote
  > {: id="20210104091501-a702uy7"}
  >
  {: id="20210104091501-3d6jagp"}
* {: id="20210104091501-u5hx1vm"}List item three
  {: id="20210216134045-fl3pi8u"}
{: id="20210104091501-m69k5xz"}

#### List item contains code block
{: id="20210104091501-t87w4jo"}

````markdown
* List item one
* The first paragraph of list item two
  
   ```
  Here is the code block
  echo Hello, world!
   ```
* List item three
````
{: id="20210104091501-us1ki57"}

Rendering result:
{: id="20210104091501-90bevjs"}

* {: id="20210104091501-dyrinem"}List item one
  {: id="20210216134045-3ztd5ok"}
* {: id="20210104091501-uytwsxn"}The first paragraph of list item two
  {: id="20210216134045-7oci9mh"}

  ```
  Here is the code block
  echo Hello, world!
  ```
  {: id="20210104091501-76rstv1"}
* {: id="20210104091501-gc9q5nk"}List item three
  {: id="20210216134045-m8dnlzf"}
{: id="20210104091501-uu2at02"}

#### List item contains pictures
{: id="20210104091501-3q9rrx4"}

````markdown
* List item one
* The first paragraph of list item two
  
  ![B3log](https://b3log.org/images/brand/b3log-128.png "B3log Open Source Community")
* List item three
````
{: id="20210104091501-dgotc25"}

Rendering result:
{: id="20210104091501-t9piqry"}

* {: id="20210104091501-m3xw8uz"}List item one
  {: id="20210104091501-sndh12j"}
* {: id="20210104091501-0lhb0mh"}The first paragraph of list item two
  {: id="20210104091501-8ejrp68"}

  ![B3log Logo](https://b3log.org/images/brand/b3log-128.png)
  {: id="20210104091501-uuadhve"}
* {: id="20210104091501-ehys932"}List item three
  {: id="20210104091501-xyoybu3"}
{: id="20210104091501-7m1kh30"}

## Code
{: id="20210104091501-vmx3qxq"}

The code can be wrapped with backticks span</code>.
{: id="20210104091501-0lzv3z8"}

| Markdown                          | HTML                                           | Rendering results                 |
| ----------------------------------- | ------------------------------------------------ | ----------------------------------- |
| The command to list files is \`ls\` | The command to list files is `<code>ls</code>` | The command to list files is `ls` |
{: id="20210104091501-29xf94h"}

### Escaping backticks
{: id="20210104091501-2pqngar"}

If you need to display the backquote, you can use the escape character `\` to escape the backquote.
{: id="20210104091501-jxti9h3"}

| Markdown          | HTML              | Rendering results |
| ------------------- | ------------------- | ------------------- |
| Type a backtick \` | Type a backtick ` | Type a backtick ` |
{: id="20210104091501-zstovis"}

### Code block
{: id="20210104091501-pjsvj0f"}

Code blocks can be indented with four spaces or tabs `\t`.
{: id="20210104091501-713aqbe"}

```markdown
    <html>
      <head>
      </head>
    </html>
```
{: id="20210104091501-qw0x4yi"}

Rendering result:
{: id="20210104091501-w3cchz2"}

```
<html>
  <head>
  </head>
</html>
```
{: id="20210104091501-dp5q2zh"}

**It is recommended to use fence code block syntax to typeset code blocks**, that is, use span</code> to wrap the code block and specify the syntax highlighting language:
{: id="20210104091501-uzf7ah0"}

````markdown
```html
<html>
  <head>
  </head>
</html>
```
````
{: id="20210104091501-p8oyxxl"}

## Thematic breaks
{: id="20210104091501-ds34jtm"}

Create a dividing line with three or more asterisks `***`, dashes `---`, or underscores `___`.
{: id="20210104091501-u40w0pz"}

```markdown
***
---
___
```
{: id="20210104091501-ih3ickv"}

Rendering result:
{: id="20210104091501-s38t5nt"}

---

## Hyperlink
{: id="20210104091501-ey0c3xs"}

Create a hyperlink by `[link text](URL)`.
{: id="20210104091501-zqeslzy"}

```markdown
We are from the niche open source community [B3log](https://b3log.org).
```
{: id="20210104091501-7curax5"}

Rendering result:
{: id="20210104091501-csiqi0y"}

We are from the niche open source community [B3log](https://b3log.org).
{: id="20210104091501-jvktcu5"}

### Add hyperlink title
{: id="20210104091501-mbp1xx2"}

The link title is optional and is enclosed in double quotes after the URL in parentheses. When the mouse is moved over the hyperlink, the title content will appear.
{: id="20210104091501-mdyxpwg"}

```markdown
We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").
```
{: id="20210104091501-ix6z903"}

Rendering result:
{: id="20210104091501-9i4d44l"}

We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").
{: id="20210104091501-t31q5iy"}

### URL and email address
{: id="20210104091501-ayur82d"}

If you want to display the URL or email address directly, you can use `<` and `>` to wrap the URL or email address.
{: id="20210104091501-cwkb3wp"}

```markdown
<https://b3log.org>

<os@b3log.org>
```
{: id="20210104091501-y3je2n0"}

Most Markdown engines also support automatic conversion, so you can omit `<>`:
{: id="20210104091501-lr2enzt"}

```markdown
https://b3log.org

os@b3log.org
```
{: id="20210104091501-skiedao"}

### Hyperlink format typeset
{: id="20210104091501-2ghyzez"}

Hyperlinks can be used together with element structures such as bold emphasis, code, etc.
{: id="20210104091501-3bb0bs8"}

```markdown
We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).
```
{: id="20210104091501-empfstj"}

Rendering result:
{: id="20210104091501-s650k8l"}

We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).
{: id="20210104091501-v0uxjlh"}

### Quote style hyperlink
{: id="20210104091501-nz63kxv"}

Use citation style hyperlinks to make the original Markdown easier to read. The citation style hyperlink is divided into two parts: link reference and link definition.
{: id="20210104091501-fkot8sz"}

#### Link reference
{: id="20210104091501-uwp9cee"}

A link reference is used where a hyperlink needs to be inserted. It consists of two sets of square brackets. The first set of square brackets is used to specify the link text, the second set of square brackets is used to specify the link identifier, and the link identifier points to the link definition.
{: id="20210104091501-5oovtoo"}

```markdown
[Link Text][Link Label]

[Link Label]: https://b3log.org
```
{: id="20210104091501-20g4wqu"}

Rendering result:
{: id="20210104091501-h84nv1l"}

[Link Text][Link Label]
{: id="20210104091501-z1jtkx6"}

The link reference can also consist of only a set of square brackets, in which case the link identifier will be used for the link text.
{: id="20210104091501-5yyofm2"}

```markdown
[Link Label]

[Link Label]: https://b3log.org
```
{: id="20210104091501-g77y2yq"}

Rendering result:
{: id="20210104091501-lprd09g"}

[Link Label]
{: id="20210104091501-lsdg6y0"}

#### Link definition
{: id="20210104091501-5sw4pyj"}

The link definition consists of three parts:
{: id="20210104091501-d59zjqe"}

1. {: id="20210104091501-y6j7zrb"}Square brackets wrap to define the link identifier, followed by a colon `:`
   {: id="20210216134045-r8vybfe"}
2. {: id="20210104091501-97o9nbq"}URL can be written directly or wrapped in angle brackets `<>`
   {: id="20210216134045-j4gdngy"}
3. {: id="20210104091501-a2ffeds"}Link title, this part is optional and can be wrapped in double quotes, single quotes or parentheses
   {: id="20210216134045-tfdtpep"}
{: id="20210104091501-daxhv5r"}

```markdown
[Link ID]: https://b3log.org
[Link ID]: <https://b3log.org>
[Link logo]: https://b3log.org "B3log open source"
[Link logo]: https://b3log.org'B3log open source'
[Link logo]: https://b3log.org (B3log open source)
```
{: id="20210104091501-xgzg80n"}

The link definition can be placed anywhere in the entire Markdown text. Some people are accustomed to putting it after the quoted paragraph, and some people are accustomed to putting it at the end of the text.
{: id="20210104091501-xrnfqqa"}

### Hyperlink Best Practice
{: id="20210104091501-kzkn3og"}

The English content is naturally separated by spaces, so there is no separation problem when using automatic hyperlinks. But Chinese will have this problem, such as:
{: id="20210104091501-2fzcguy"}

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```
{: id="20210104091501-hodxz90"}

This content will render incorrectly on many Markdown engines. In order to ensure compatibility as much as possible, consider using spaces to separate:
{: id="20210104091501-mkn9h83"}

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```
{: id="20210104091501-ewb49tm"}

Or use angle brackets `<>` to wrap:
{: id="20210104091501-eyc3qqz"}

```markdown
Our website is <https://b3log.org> Open source enthusiasts are welcome to join!
```
{: id="20210104091501-2oa0v5z"}

So you can get the expected rendering result:
{: id="20210104091501-ivr3via"}

Our website is [https://b3log.org](https://b3log.org) Open source enthusiasts are welcome to join!
{: id="20210104091501-n8xqse4"}

## Picture
{: id="20210104091501-qdid0iv"}

Use the exclamation mark `!` followed by a hyperlink to render the image.
{: id="20210104091501-16uw63o"}

```markdown
![B3log Logo](https://b3log.org/images/brand/b3log-128.png)
```
{: id="20210104091501-j0cwfgo"}

Rendering result:
{: id="20210104091501-b6t3hny"}

![B3log Logo](https://b3log.org/images/brand/b3log-128.png)
{: id="20210104091501-shaalez"}

### Hyperlink nested image
{: id="20210104091501-t5j4vvp"}

If you need to click on the picture to jump to the hyperlink, you only need to include the picture in the text part of the link.
{: id="20210104091501-vxh48yo"}

```markdown
[![LianDi](https://b3log.org/images/brand/hacpai-128.png)](https://ld246.com)
```
{: id="20210104091501-lz44osc"}

Rendering result:
{: id="20210104091501-x9nimrg"}

[![LianDi](https://b3log.org/images/brand/hacpai-128.png)](https://ld246.com)
{: id="20210104091501-qoo2seo"}

## Escape character
{: id="20210104091501-agqruvx"}

You can use the backslash `\` to escape the following characters:
{: id="20210104091501-3g47u02"}

| Characters  | Chinese name               |
| ------------- | ---------------------------- |
| `\`         | Backslash                  |
| `` ` ``     | backtick                   |
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
| `\|` </code> | Vertical bar (pipe symbol) |
{: id="20210104091501-9kq13rz"}

Almost all ASCII punctuation marks can be escaped with backslashes.
{: id="20210104091501-94mq1s6"}

## Embed HTML
{: id="20210104091501-xew5zhh"}

Markdown naturally supports embedding HTML code.
{: id="20210104091501-62u5mpo"}

```markdown
**Markdown** and <em>HTML</em> mixed typesetting.
```
{: id="20210104091501-lvbg47x"}

Rendering result:
{: id="20210104091501-m2a68br"}

**Markdown** and <em>HTML</em> mixed typesetting.
{: id="20210104091501-ffdld6m"}

### Embedding HTML Best Practices
{: id="20210104091501-hafz7jx"}

This is useful when you need to set the image size and font color, but we don’t recommend using HTML too much for typesetting, because this is actually not universal, because some Markdown engines filter some parts for security reasons Labels or attributes; secondly, because it is too Markdown!
{: id="20210104091501-a767twl"}

Also, don’t embed Markdown in HTML, it won’t work:
{: id="20210104091501-zwe1gzc"}

```markdown
<p>**Bold** will not take effect. </p>
```
{: id="20210104091501-91c7lob"}

Rendering result:
{: id="20210104091501-2r3oiie"}

<p>**Bold** will not take effect. </p>

{: id="20210104091501-5h7ipyd"}

## Summary
{: id="20210104091501-ggwr2dm"}

Good use of blank lines and spaces is the key to Markdown typesetting. In many cases, it is because of missing blank lines or spaces that unexpected rendering results are produced.
{: id="20210104091501-u0qnwhe"}

With the improvement of the CommonMark/GFM specification and gradually becoming the industry's unified Markdown standard, more and more Markdown engines have implemented the specification. It is recommended that Markdown users should follow the specifications as much as possible for typesetting, so as to avoid detail rendering problems to the greatest extent.
{: id="20210104091501-9v4hx0p"}

## Reference
{: id="20210104091501-awhnw82"}

* {: id="20210104091501-q8kha7c"}[Markdown Guide](https://www.markdownguide.org)
  {: id="20210216134045-rysmmw0"}
* {: id="20210104091501-amvsrqq"}[CommonMark Spec](https://spec.commonmark.org)
  {: id="20210216134045-9jzb6ea"}
{: id="20210104091501-vi9mtye"}

[Link Label]: https://b3log.org
{: id="20210302223819-uqae5w9"}


{: id="20200924085905-kxykwln" type="doc"}

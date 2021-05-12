## Content Block type cheatsheet
{: id="20210104091538-4b3n4al"}

Hover the mouse over the content block and the corresponding icon will appear on the left side of the content block. For format usage, please refer to ((20200924093441-ft2rhps "Markdown Complete Demo")).
{: id="20210104091538-ngfa912" updated="20210302223854"}

| Icon                                                                    | Type                 | ((20200925102736-x94e40g "Meta Type")) |
| ------------------------------------------------------------------------- | ---------------------- | --------------------------------- |
| ![paragraph.svg](assets/paragraph-20210512171139-2x8lgt5.svg)           | Paragraph block      | Leaf block                      |
| ![heading.svg](assets/heading-20210512171149-56npt09.svg)               | Heading block        | Leaf block                      |
| ![math-block.svg](assets/math-block-20210512171155-9w2eti5.svg)         | Math Formula block   | Leaf block                      |
| ![code-block.svg](assets/code-block-20210512171201-pw7hrv2.svg)         | Code block           | Leaf block                      |
| ![table.svg](assets/table-20210512171208-hgfm17w.svg)                   | Table block          | Leaf block                      |
| ![unordered-list.svg](assets/unordered-list-20210512171214-90nb6w0.svg) | Unordered List block | Container block                 |
| ![ordered-list.svg](assets/ordered-list-20210512171220-ghfzj2f.svg)     | Ordered List block   | Container block                 |
| ![task-list.svg](assets/task-list-20210512171226-br51zxn.svg)           | Task list block      | Container block                 |
| ![list-item.svg](assets/list-item-20210512171231-2yc3wfd.svg)           | List Item block      | Container block                 |
| ![blockquote.svg](assets/blockquote-20210512171236-9dl6ui9.svg)         | Blockquote block     | Container block                 |
| ![super-block.svg](assets/super-block-20210512171243-ydsukhs.svg)       | Super block          | Container block                 |
| ![doc.svg](assets/doc-20210512171251-8qzw4l4.svg)                       | Document block       | Container block                 |
{: id="20210104091538-le8t1ci"}

## Details of content block types
{: id="20210104091538-a55chyw"}

Below we introduce the details of these content block types. #Content block/Type#
{: id="20210104091538-a61xzjz"}

### Paragraph block
{: id="20210104091538-67s659i"}

![paragraph](assets/paragraph-20210512171139-2x8lgt5.svg)
{: id="20210104091538-e0zt5qh" updated="20210512171308"}

Here is a sample paragraph.
{: id="20210104091538-v7dhyea"}

Press Enter directly after a paragraph to form a new paragraph.
{: id="20210104091538-u96pio8"}

### Heading block
{: id="20210104091538-d5t39y5"}

![heading](assets/heading-20210512171149-56npt09.svg)
{: id="20210104091538-d84k7sa" updated="20210512171318"}

The above is the heading block, which supports level one to six.
{: id="20210104091538-o0ti5xd"}

### Mathematical formula block
{: id="20210104091538-u3ku9wo"}

![math-block](assets/math-block-20210512171155-9w2eti5.svg)
{: id="20210104091538-kuun1bc" updated="20210512171325"}

$$
a^2 + b^2 = c^2
$$
{: id="20210104091538-ko666d2"}

You can switch the math formula block rendering engine in the settings, the default is `MathJax`.
{: id="20210104091538-9a3yc1w"}

### Code block
{: id="20210104091538-fa7y245"}

![code-block](assets/code-block-20210512171201-pw7hrv2.svg)
{: id="20210104091538-8dyz7jj" updated="20210512171334"}

```js
function hello() {}
```
{: id="20210104091538-xsj6knt"}

### Table block
{: id="20210104091538-38bsz5r"}

![table](assets/table-20210512171208-hgfm17w.svg)
{: id="20210104091538-zc8ai9n" updated="20210512171342"}

| Column 1           | Column 2           |
| -------------------- | -------------------- |
| Row One Column One | Row One Column Two |
| Row Two Column One | Row Two Column Two |
{: id="20210104091538-pbqg66x"}

If you need to use `|` in the form, please use `\` to escape, that is, you need to enter `\|`.
{: id="20210104091538-ok40ct8"}

### Unordered List Block
{: id="20210104091538-cddpqkl"}

![unordered-list](assets/unordered-list-20210512171214-90nb6w0.svg)
{: id="20210104091538-ym0xna0" updated="20210512171353"}

* {: id="20210104091538-60hsat5"}List item one
  {: id="20210302223851-9vz2n9a"}
* {: id="20210104091538-ocml6u6"}List item two
  {: id="20210302223851-q996hlf"}
{: id="20210104091538-g2v9tfm"}

The unordered list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-9zkv22k"}

If you need to wrap a line in a list item, use <kbd>Shift Enter</kbd>.
{: id="20210104091538-lb00enw"}

### Ordered List Block
{: id="20210104091538-jhbekfn"}

![ordered-list](assets/ordered-list-20210512171220-ghfzj2f.svg)
{: id="20210104091538-fle9kwp" updated="20210512171407"}

1. {: id="20210104091538-s49jwy3"}List item one
   {: id="20210302223851-w2smsmh"}
2. {: id="20210104091538-cqk5t72"}List item two
   {: id="20210302223851-1p5ob4q"}
{: id="20210104091538-qy3j9yk"}

An ordered list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-1ix6ueu"}

### Task list block
{: id="20210104091538-uz0na96" updated="20210503220211"}

![task-list](assets/task-list-20210512171226-br51zxn.svg)
{: id="20210104091538-hy0rb8f" updated="20210512171414"}

- {: id="20210104091538-urtl418"}[X] To do one
  {: id="20210302223851-99onwrg"}
- {: id="20210104091538-cwwt4j5"}[ ] To do two
  {: id="20210302223851-gzah6cx"}
{: id="20210104091538-d5chiez"}

The task list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-tw00i00" updated="20210503220216"}

### List item block
{: id="20210104091538-wqiaxdu"}

![list-item](assets/list-item-20210512171231-2yc3wfd.svg)
{: id="20210104091538-qqhyuw2" updated="20210512171428"}

The basic usage of outline notes can be realized through the list item block. The list item block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-lbf2al4"}

### Blockquote Block
{: id="20210104091538-w91ot9s"}

![blockquote](assets/blockquote-20210512171236-9dl6ui9.svg)
{: id="20210104091538-i8x92b5" updated="20210512171433"}

> Note that it is not a content block quote, but a block quote (Blockquote).
> {: id="20210104091538-osgy8b0"}
{: id="20210104091538-jl60vah"}

The block reference block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-lz7s79p"}

### Super block
{: id="20210104091538-lubwy1k"}

![super-block](assets/super-block-20210512171243-ydsukhs.svg)
{: id="20210104091538-6cpmf1u" updated="20210512171440"}

The super block is a type ((20200925102736-x94e40g "container block")). It can be used to combine continuous content blocks in a document, and also to support horizontal typesetting.
{: id="20210104091538-hpihzah" updated="20210503220329"}

### Documentation block
{: id="20210104091538-clx67q4"}

![doc](assets/doc-20210512171251-8qzw4l4.svg)
{: id="20210104091538-ot2afhs" updated="20210512171446"}

The entire document is a block, and the document block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-mg5xa52"}

## Content Block meta type
{: id="20200925102736-x94e40g"}

The content block is logically divided into a leaf block and a container block. The leaf block cannot contain other blocks, and the container block can contain other blocks:
{: id="20210104091538-36hcqp1"}

* {: id="20210104091538-7ux94d1"}List block: can only contain list item blocks
  {: id="20210302223851-6sw8cbv"}
* {: id="20210104091538-qj0m5z6"}List item block: can contain any other non-document blocks
  {: id="20210302223851-ra0j9je"}
* {: id="20210104091538-as7s34n"}Blockquote block: can contain any non-document blocks
  {: id="20210302223851-orfn1qc"}
* {: id="20210104091538-66zs0qu"}Super block: can contain any non-document blocks
  {: id="20210302223851-xuok2cn"}
* {: id="20210104091538-frbdtaw"}Document block: can contain any non-document blocks
  {: id="20210302223851-9b5hb4i"}
{: id="20210104091538-3pi7fbf"}


{: id="20200924101225-k254i8g" type="doc"}

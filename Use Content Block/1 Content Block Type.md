## Content Block type cheatsheet
{: id="20210104091538-4b3n4al"}

Hover the mouse over the content block and the corresponding icon will appear on the left side of the content block. For format usage, please refer to ((20200924093441-ft2rhps "Markdown Complete Demo")).
{: id="20210104091538-ngfa912"}

| Icon                                         | Type                 | ((20200925102736-x94e40g "Meta Type")) |
| ---------------------------------------------- | ---------------------- | --------------------------------- |
| ![paragraph](assets/paragraph.svg)           | Paragraph block      | Leaf block                      |
| ![heading](assets/heading.svg)               | Heading block        | Leaf block                      |
| ![math-block](assets/math-block.svg)         | Math Formula block   | Leaf block                      |
| ![code-block](assets/code-block.svg)         | Code block           | Leaf block                      |
| ![table](assets/table.svg)                   | Table block          | Leaf block                      |
| ![unordered-list](assets/unordered-list.svg) | Unordered List block | Container block                 |
| ![ordered-list](assets/ordered-list.svg)     | Ordered List block   | Container block                 |
| ![task-list](assets/task-list.svg)           | To-do list block     | Container block                 |
| ![list-item](assets/list-item.svg)           | List Item block      | Container block                 |
| ![blockquote](assets/blockquote.svg)         | Blockquote block     | Container block                 |
| ![super-block](assets/super-block.svg)       | Super block          | Container block                 |
| ![doc](assets/doc.svg)                       | Document block       | Container block                 |
{: id="20210104091538-le8t1ci"}

## Details of content block types
{: id="20210104091538-a55chyw"}

Below we introduce the details of these content block types. #Content block/Type#
{: id="20210104091538-a61xzjz"}

### Paragraph block
{: id="20210104091538-67s659i"}

![paragraph](assets/paragraph.svg)
{: id="20210104091538-e0zt5qh"}

Here is a sample paragraph.
{: id="20210104091538-v7dhyea"}

Press Enter directly after a paragraph to form a new paragraph.
{: id="20210104091538-u96pio8"}

### Heading block
{: id="20210104091538-d5t39y5"}

![heading](assets/heading.svg)
{: id="20210104091538-d84k7sa"}

The above is the heading block, which supports level one to six.
{: id="20210104091538-o0ti5xd"}

When using ((20200924101312-jj4e0v3 "Content block reference")) or ((20200924101312-385dey5 "Content block embedding")), related content blocks under the heading block will be automatically aggregated according to the heading level.
{: id="20210104091538-7qvmp8d"}

### Mathematical formula block
{: id="20210104091538-u3ku9wo"}

![math-block](assets/math-block.svg)
{: id="20210104091538-kuun1bc"}

$$
a^2 + b^2 = c^2
$$
{: id="20210104091538-ko666d2"}

You can switch the math formula block rendering engine in the settings, the default is `MathJax`.
{: id="20210104091538-9a3yc1w"}

### Code block
{: id="20210104091538-fa7y245"}

![code-block](assets/code-block.svg)
{: id="20210104091538-8dyz7jj"}

```js
function hello() {}
```
{: id="20210104091538-xsj6knt"}

### Table block
{: id="20210104091538-38bsz5r"}

![table](assets/table.svg)
{: id="20210104091538-zc8ai9n"}

| Column 1           | Column 2           |
| -------------------- | -------------------- |
| Row One Column One | Row One Column Two |
| Row Two Column One | Row Two Column Two |
{: id="20210104091538-pbqg66x"}

If you need to use `|` in the form, please use `\` to escape, that is, you need to enter `\|`.
{: id="20210104091538-ok40ct8"}

### Unordered List Block
{: id="20210104091538-cddpqkl"}

![unordered-list](assets/unordered-list.svg)
{: id="20210104091538-ym0xna0"}

* {: id="20210104091538-60hsat5"}List item one
* {: id="20210104091538-ocml6u6"}List item two
{: id="20210104091538-g2v9tfm"}

The unordered list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-9zkv22k"}

If you need to wrap a line in a list item, use <kbd>Shift Enter</kbd>.
{: id="20210104091538-lb00enw"}

### Ordered List Block
{: id="20210104091538-jhbekfn"}

![ordered-list](assets/ordered-list.svg)
{: id="20210104091538-fle9kwp"}

1. {: id="20210104091538-s49jwy3"}List item one
2. {: id="20210104091538-cqk5t72"}List item two
{: id="20210104091538-qy3j9yk"}

An ordered list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-1ix6ueu"}

### To do list block
{: id="20210104091538-uz0na96"}

![task-list](assets/task-list.svg)
{: id="20210104091538-hy0rb8f"}

- {: id="20210104091538-urtl418"}[X] To do one
- {: id="20210104091538-cwwt4j5"}[ ] To do two
{: id="20210104091538-d5chiez"}

The to-do list block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-tw00i00"}

### List item block
{: id="20210104091538-wqiaxdu"}

![list-item](assets/list-item.svg)
{: id="20210104091538-qqhyuw2"}

The basic usage of outline notes can be realized through the list item block. The list item block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-lbf2al4"}

### Blockquote Block
{: id="20210104091538-w91ot9s"}

![blockquote](assets/blockquote.svg)
{: id="20210104091538-i8x92b5"}

> Note that it is not a content block quote, but a block quote (Blockquote).
> {: id="20210104091538-osgy8b0"}
{: id="20210104091538-jl60vah"}

The block reference block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-lz7s79p"}

### Super block
{: id="20210104091538-lubwy1k"}

![super-block](assets/super-block.svg)
{: id="20210104091538-6cpmf1u"}

The super block is a type ((20200925102736-x94e40g "container block")). It can be used to combine continuous content blocks in a document, using a single line of `{{{` as the start marker and `}}}` as the end marker.
{: id="20210104091538-hpihzah"}

```markdown
{{{

Paragraph block

* List block

> Blockquote block

# Heading block

{{{

Nested super block
...

}}}

...

}}}
```
{: id="20210104091538-qz97dbp"}

### Documentation block
{: id="20210104091538-clx67q4"}

![doc](assets/doc.svg)
{: id="20210104091538-ot2afhs"}

The entire document is a block, and the document block is a type ((20200925102736-x94e40g "container block")).
{: id="20210104091538-mg5xa52"}

## Content Block meta type
{: id="20200925102736-x94e40g"}

The content block is logically divided into a leaf block and a container block. The leaf block cannot contain other blocks, and the container block can contain other blocks:
{: id="20210104091538-36hcqp1"}

* {: id="20210104091538-7ux94d1"}List block: can only contain list item blocks
* {: id="20210104091538-qj0m5z6"}List item block: can contain any other non-document blocks
* {: id="20210104091538-as7s34n"}Blockquote block: can contain any non-document blocks
* {: id="20210104091538-66zs0qu"}Super block: can contain any non-document blocks
* {: id="20210104091538-frbdtaw"}Document block: can contain any non-document blocks
{: id="20210104091538-3pi7fbf"}


{: id="20200924101225-k254i8g" type="doc"}

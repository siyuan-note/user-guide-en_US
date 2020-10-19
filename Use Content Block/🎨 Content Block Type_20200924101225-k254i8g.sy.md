## Content Block type cheatsheet

Hover the mouse over the content block and the corresponding icon will appear on the left side of the content block. For format usage, please refer to ((20200924093441-ft2rhps "Markdown Complete Demo")).

| Icon                                     | Type                 | ((20200925102736-x94e40g "Meta Type")) |
| ---------------------------------------- | -------------------- | -------------------------------------- |
| ![paragraph](assets/paragraph.svg)       | Paragraph block      | Leaf block                             |
| ![heading](assets/heading.svg)           | Heading block        | Leaf block                             |
| ![math-block](assets/math-block.svg)     | Math Formula Block   | Leaf Block                             |
| ![math-block](assets/code-block.svg)     | Code block           | Leaf block                             |
| ![math-block](assets/unordered-list.svg) | Unordered List Block | Container block                        |
| ![math-block](assets/ordered-list.svg)   | Ordered List Block   | Container block                        |
| ![math-block](assets/task-list.svg)      | To-do list block     | Container block                        |
| ![math-block](assets/table.svg)          | Table block          | Leaf block                             |
| ![math-block](assets/blockquote.svg)     | Blockquote block     | Container block                        |
| ![doc](assets/doc.svg)                   | Document block       | Container block                        |

## Details of content block types

Below we introduce the details of these content block types.

### Paragraph block

![paragraph](assets/paragraph.svg)

Here is a sample paragraph.

Press Enter directly after a paragraph to form a new paragraph.

### Heading block

![heading](assets/heading.svg)

The above is the heading block, which supports level one to six.

When using ((20200924101312-jj4e0v3 "Content block reference")) or ((20200924101312-385dey5 "Content block embedding")), related content blocks under the title block will be automatically aggregated according to the heading level.

### Mathematical formula block

![math-block](assets/math-block.svg)

$$
a^2 + b^2 = c^2
$$

You can switch the math formula block rendering engine in the settings, the default is `MathJax`.

### Code block

![math-block](assets/code-block.svg)

```js
function hello() {}
```

### Unordered List Block

![math-block](assets/unordered-list.svg)

* List item one
* List item two

The unordered list block is a type ((20200925102736-x94e40g "block container")).

If you need to wrap a line in a list item, use <kbd>Shift Enter</kbd>.

### Ordered List Block

![math-block](assets/ordered-list.svg)

1. List item one
2. List item two

An ordered list block is a type ((20200925102736-x94e40g "block container")).

### To do list block

![math-block](assets/task-list.svg)

-[X] To do one
-[] To do two

The to-do list block is a type ((20200925102736-x94e40g "block container")).

### Table block

![math-block](assets/table.svg)

| Column 1           | Column 2           |
| ------------------ | ------------------ |
| Row One Column One | Row One Column Two |
| Row Two Column One | Row Two Column Two |

If you need to use `|` in the form, please use `\` to escape, that is, you need to enter `\|`.

### Block Quote Block

![math-block](assets/blockquote.svg)

> Note that it is not a content block quote, but a block quote (Blockquote).

The block reference block is a type ((20200925102736-x94e40g "block container")).

### Documentation block

![doc](assets/doc.svg)

The entire document is a block, and the document block is a type ((20200925102736-x94e40g "block container")).

## Content Block meta type
{: id="20200925102736-x94e40g"}

The content block is logically divided into a leaf block and a container block. The leaf block cannot contain other blocks, and the container block can contain other blocks, following the CommonMark/GFM specification.

There are several types of container blocks:

* List block: can only contain list item blocks (does not support list item blocks for the time being, that is, it cannot link a single list item), list item blocks can contain any other non-document blocks
* Block reference block: can contain any non-document block
* Super block #TODO#: can contain any non-document block
* Document block: can contain any non-document content block

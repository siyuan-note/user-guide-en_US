If the search keyword starts with the following characters, type filtering is enabled.

* `d` Document block
* `h` Heading block
* `l` List block (including ordered list block, unordered list block and task list block)
* `i` List item block
* `c` Code block
* `m` Mathematical formula block
* `t` Table block
* `b` Blockquote block
* `s` Super block
* `p` Paragraph block

For example, if you want to search for all heading blocks that contain `Markdown`, you can use `hMarkdown` as the search criteria. If the beginning character of the keyword to be searched is in the above list, you need to use `\` to escape. For example, if you want to search for the keyword `doc`, `d` will hit the document block filter, so that the keyword actually searched is `oc`, which needs to be escaped by `\doc`.


{: id="20201222100222-q47d64s" type="doc"}

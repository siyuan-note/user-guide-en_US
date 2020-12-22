## `blocks` table
{: id="20201117103851-gx21lz6"}

This table is used to store content block data.

|    Field | Type | Description                                             |
| ---------: | :----: | --------------------------------------------------------- |
|       id | text | Self-incrementing primary key                           |
| block_id | text | Content block ID                                        |
|      box | text | Notebook name                                           |
|     path | text | Path of the document where the content block is located |
|  tree_id | text | Abstract Syntax Tree ID, as the same as root node ID    |
|  content | text | Content block Markdown                                  |
|     type | text | Content block type                                      |

Example:

```sql
SELECT * FROM blocks WHERE content LIKE '%content block%'
```

List of `type` content block type values:

* `NodeDocument` Document block
* `NodeHeading` Heading block
* `NodeParagraph` Paragraph block
* `NodeList` List block
* `NodeListItem` List item block
* `NodeMathBlock` Mathematical formula block
* `NodeCodeBlock` Code block
* `NodeBlockquote` Blockquote block
* `NodeTable` Table block
* `NodeSuperBlock` Super block

## Default query conditions

* If you do not specify the `type` column, the default will add `type = NodeParagraph`, that is, only query paragraph blocks
* If `LIMIT` is not specified, only the first 32 results will be returned at most


{: id="20201222100339-i5hzcph" type="doc"}

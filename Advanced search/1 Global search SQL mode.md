## `blocks` table
{: id="20201117103851-gx21lz6"}

This table is used to store content block data.
{: id="20201224120448-t51cvuj"}

|     Field | Description                                                                    |
| ----------: | -------------------------------------------------------------------------------- |
|        id | Content block ID                                                               |
| parent_id | Parent block ID, If the content block is a document block, this field is empty |
|   root_id | Root block ID, which is the document block ID                                  |
|       box | Notebook name                                                                  |
|      path | Document path where content block is located                                   |
|      name | Content block name                                                             |
|      memo | Content block memo                                                             |
|   content | Text with Markdown markers removed                                             |
|  markdown | Text with complete Markdown markers                                            |
|      type | Content block type, please refer to ((20201224092621-haejkkh "here"))                 |
|      time | Create time                                                                    |
|       ial | Inline attributes list, like  `{: name="value"}`                               |
|      sort | For sorting, the smaller the value, the higher the sort                        |
{: id="20210111225813-9kys36i"}

## Default query conditions
{: id="20201224120448-dd94dgz"}

* {: id="20201224120448-f5yv48x"}If `LIMIT` is not specified, only the first 32 results will be returned at most
{: id="20201224120448-ox8c45i"}


{: id="20201222100339-i5hzcph" type="doc"}

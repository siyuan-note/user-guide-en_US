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

## Default values
{: id="20201224120448-dd94dgz"}

* {: id="20210112165011-hndbj25"}If `LIMIT` is not specified, only the first 32 results will be returned at most
* {: id="20210112165011-n8zrkxm"}`sort` field
  * {: id="20210112165011-hb9w8kd"}Document block: `0`
  * {: id="20210112165011-epgryib"}Heading block: `5`
  * {: id="20210112165011-m8d9n8y"}List block: `10`
  * {: id="20210112165011-l855w5d"}List item block: `15`
  * {: id="20210112165011-s2y8b3b"}Code block: `20`
  * {: id="20210112165011-zcnzdjs"}Mathematical formula block: `25`
  * {: id="20210112165011-jfb3akr"}Table block: `30`
  * {: id="20210112165011-w9j14de"}Blockquote block: `35`
  * {: id="20210112165011-8t05120"}Super block: `40`
  * {: id="20210112165011-t89y8yx"}Paragraph block: `45`
  {: id="20210112165011-fodiphq"}
{: id="20210112165011-irm4wch"}


{: id="20201222100339-i5hzcph" type="doc"}

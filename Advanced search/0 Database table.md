## Table `blocks`
{: id="20201117103851-gx21lz6" updated="20210302223506"}

This table is used to store content block data.
{: id="20201224120448-t51cvuj"}

|       Field | Description                                                                    |
| ------------: | -------------------------------------------------------------------------------- |
|          id | Content block ID                                                               |
|   parent_id | Parent block ID, If the content block is a document block, this field is empty |
| previous_id | Previous block ID                                                              |
|     next_id | Next block ID                                                                  |
|     root_id | Root block ID, which is the document block ID                                  |
|        hash | Summary checksum of the content                                                |
|         box | Notebook name                                                                  |
|        path | Document path where content block is located                                   |
|        name | Content block name                                                             |
|       alias | Content block alias                                                            |
|        memo | Content block memo                                                             |
|     content | Text with Markdown markers removed                                             |
|    markdown | Text with complete Markdown markers                                            |
|      length | Markdown text length                                                           |
|        type | Content block type, please refer to ((20210210104024-efd1ar6 "here"))                 |
|     subtype | Content block subtype, please refer to ((20210210104037-xex9wds "here"))              |
|         ial | Inline attributes list, like  `{: name="value"}`                               |
|        sort | For sorting, the smaller the value, the higher the sort                        |
|     created | Create time                                                                    |
|     updated | Update time                                                                    |
{: id="20210111225813-9kys36i" updated="20210321230154"}

## Default values
{: id="20201224120448-dd94dgz"}

* {: id="20210112165011-hndbj25"}If `LIMIT` is not specified, only the first 32 results will be returned at most
  {: id="20210210104251-j5gbxzv"}
* {: id="20210112165011-n8zrkxm"}`sort` field
  {: id="20210210104251-nno6rgh"}

  * {: id="20210112165011-hb9w8kd"}Document block: `0`
    {: id="20210210104251-iy9ugib"}
  * {: id="20210112165011-epgryib"}Heading block: `5`
    {: id="20210210104251-blu4b7p"}
  * {: id="20210112165011-m8d9n8y"}List block: `10`
    {: id="20210210104251-wi73iql"}
  * {: id="20210112165011-l855w5d"}List item block: `15`
    {: id="20210210104251-gi77vbg"}
  * {: id="20210112165011-s2y8b3b"}Code block: `20`
    {: id="20210210104251-x1h16tv"}
  * {: id="20210112165011-zcnzdjs"}Mathematical formula block: `25`
    {: id="20210210104251-bxza6ez"}
  * {: id="20210112165011-jfb3akr"}Table block: `30`
    {: id="20210210104251-29bs67e"}
  * {: id="20210112165011-w9j14de"}Blockquote block: `35`
    {: id="20210210104251-8iggp8k"}
  * {: id="20210112165011-8t05120"}Super block: `40`
    {: id="20210210104251-m12jzc5"}
  * {: id="20210112165011-t89y8yx"}Paragraph block: `45`
    {: id="20210210104251-4q3mvqt"}
  {: id="20210112165011-fodiphq"}
{: id="20210112165011-irm4wch"}


{: id="20201222100339-i5hzcph" type="doc"}

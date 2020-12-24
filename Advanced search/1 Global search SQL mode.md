## `blocks` table
{: id="20201117103851-gx21lz6"}

This table is used to store content block data.
{: id="20201222212031-ypi15p9"}

|   Field | Type | Description                                             |
| --------: | :----: | --------------------------------------------------------- |
|      id | text | Content block ID                                        |
|     box | text | Notebook name                                           |
|    path | text | Path of the document where the content block is located |
| tree_id | text | Abstract Syntax Tree ID, as the same as root node ID    |
| content | text | Content block Markdown                                  |
|    type | text | Content block type                                      |
|    time | text | date time                                               |
{: id="20201222212031-wzd8v2b"}

Example:
{: id="20201222212031-v5d0rau"}

```sql
SELECT * FROM blocks WHERE content LIKE '%content block%'
```
{: id="20201222212031-ce7gkuz"}

List of `type` content block type please refer to ((20201224092621-haejkkh "here")).
{: id="20201222212031-nbnw5z5"}

## Default query conditions
{: id="20201222212031-oprjmx6"}

* {: id="20201222212031-vn4686r"}If you do not specify the `type` column, the default will add `type = p`, that is, only query paragraph blocks
* {: id="20201222212031-xblb7nt"}If `LIMIT` is not specified, only the first 32 results will be returned at most
{: id="20201222212031-ub749l7"}


{: id="20201222100339-i5hzcph" type="doc"}

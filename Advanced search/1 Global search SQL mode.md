## `blocks` table
{: id="20201117103851-gx21lz6"}

This table is used to store content block data.
{: id="20201224120448-t51cvuj"}

|   Field | Type | Description                                             |
| --------: | :----: | --------------------------------------------------------- |
|      id | text | Content block ID                                        |
|     box | text | Notebook name                                           |
|    path | text | Path of the document where the content block is located |
| tree_id | text | Abstract Syntax Tree ID, as the same as root node ID    |
| content | text | Content block Markdown                                  |
|    type | text | Content block type                                      |
|    time | text | date time                                               |
{: id="20201224120448-9rlsmk8"}

Example:
{: id="20201224120448-dmq3ovb"}

```sql
SELECT * FROM blocks WHERE content LIKE '%content block%'
```
{: id="20201224120448-mruqdo4"}

List of `type` content block type please refer to ((20201224092621-haejkkh "here")).
{: id="20201224120448-d0ttg6o"}

## Default query conditions
{: id="20201224120448-dd94dgz"}

* {: id="20201224120448-f5yv48x"}If `LIMIT` is not specified, only the first 32 results will be returned at most
{: id="20201224120448-ox8c45i"}


{: id="20201222100339-i5hzcph" type="doc"}

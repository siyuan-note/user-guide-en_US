## Dynamic query embed syntax

The syntax of the content block dynamic query embed is:

```sql
!{{ SELECT * FROM blocks WHERE content LIKE '%content block%' }}
```

It needs to be used on its own line. The script syntax used is SQL. For details, please refer to ((20201117103851-gx21lz6 "here")).

### Example

* Query list items that contain `content block`:

  ```sql
  !{{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND type = 'NodeListItem' }}
  ```
* The query content contains both `content block` and `reference` paragraph blocks:

  ```sql
    !{{ SELECT * FROM blocks WHERE content LIKE'%content block%' AND content LIKE'%reference%' }}
  ```
* The query content contains title blocks of both `content block` and `embed`, and the first 2 items are selected in descending order of time:

  ```sql
  !{{ SELECT * FROM blocks WHERE (content LIKE '%content block%' AND content LIKE '%embed%') AND type ='NodeHeading' ORDER BY block_id DESC LIMIT 4 }}
  ```

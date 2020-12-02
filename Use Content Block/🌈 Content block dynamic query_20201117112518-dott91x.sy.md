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

Let's actually run it to see the effect.

#### Case 1

The query contains paragraph blocks of both `In SiYuan` and `core concept` text, and excludes the current document (otherwise the paragraph block will also be included in the result set, because the current paragraph also contains these two texts. The following case is similar):

!{{SELECT * FROM blocks WHERE (content LIKE '%In SiYuan%' AND content LIKE '%core concept%') AND path NOT LIKE '%Content block dynamic query%'}}

#### Case 2

Query paragraph blocks that contain both `#Content block/Embed#` tags and `#Content block/Reference#`:

!{{SELECT * FROM blocks WHERE (content LIKE '%#Content block/Embed#%' OR content LIKE '%#Content block/Reference#%') AND path NOT LIKE '%Content block dynamic query%'}}

#### Case 3

Sometimes we may need to randomly display content blocks to facilitate review.

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}

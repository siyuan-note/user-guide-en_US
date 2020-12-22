## Dynamic query embed syntax
{: id="20201222214649-60ioj6t"}

The syntax of the content block dynamic query embed is:
{: id="20201222214649-jd16k6e"}

```sql
!{{ SELECT * FROM blocks WHERE content LIKE '%content block%' }}
```
{: id="20201222214649-hze4djt"}

It needs to be used on its own line. The script syntax used is SQL. For details, please refer to ((20201117103851-gx21lz6 "here")).
{: id="20201222214649-mzwdhup"}

### Example
{: id="20201222214649-0j0f9zl"}

* {: id="20201222214649-p36vijb"}Query list items that contain `content block`:
  {: id="20201222214649-b6q60wg"}

  ```sql
  !{{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND type = 'i' }}
  ```
  {: id="20201222214649-cy7syho"}
* {: id="20201222214649-t0sdr1u"}The query content contains both `content block` and `reference` paragraph blocks:
  {: id="20201222214649-tqhar9y"}

  ```sql
    !{{ SELECT * FROM blocks WHERE content LIKE'%content block%' AND content LIKE'%reference%' }}
  ```
  {: id="20201222214649-c6z8fax"}
* {: id="20201222214649-sr55lzm"}The query content contains heading blocks of both `content block` and `embed`, and the first 2 items are selected in descending order of time:
  {: id="20201222214649-ccg6w01"}

  ```sql
  !{{ SELECT * FROM blocks WHERE (content LIKE '%content block%' AND content LIKE '%embed%') AND type ='h' ORDER BY block_id DESC LIMIT 4 }}
  ```
  {: id="20201222214649-a69wqe2"}
{: id="20201222214649-et5lpnq"}

Let's actually run it to see the effect.
{: id="20201222214649-kuues5d"}

#### Case 1
{: id="20201222214649-sxlseit"}

The query contains paragraph blocks of both `In SiYuan` and `core concept` text, and excludes the current document (otherwise the paragraph block will also be included in the result set, because the current paragraph also contains these two texts. The following case is similar):
{: id="20201222214649-54c92lr"}

!{{SELECT * FROM blocks WHERE (content LIKE '%In SiYuan%' AND content LIKE '%core concept%') AND path NOT LIKE '%Content block dynamic query%'}}

{: id="20201222214834-y6blmt7" type="doc"}

{: id="20201222214649-hdc4j02"}

#### Case 2
{: id="20201222214649-6wtteml"}

Query paragraph blocks that contain both `#Content block/Embed#` tags and `#Content block/Reference#`:
{: id="20201222214649-6zh7ceh"}

!{{SELECT * FROM blocks WHERE (content LIKE '%#Content block/Embed#%' OR content LIKE '%#Content block/Reference#%') AND path NOT LIKE '%Content block dynamic query%'}}

{: id="20201222214834-xhxrz5r" type="doc"}

{: id="20201222214649-wsf8ice"}

#### Case 3
{: id="20201222214649-jq48t5m"}

Sometimes we may need to randomly display content blocks to facilitate review.
{: id="20201222214649-ha3qsc9"}

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}

{: id="20201222214834-kbq9y3o" type="doc"}

{: id="20201222214649-lp5ghxd"}


{: id="20201117112518-dott91x" type="doc"}

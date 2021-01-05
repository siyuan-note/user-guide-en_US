## Dynamic query embed syntax
{: id="20201224120448-6jnrawi"}

The syntax of the content block dynamic query embed is:
{: id="20201224120448-0nang3o"}

```sql
!{{ SELECT * FROM blocks WHERE content LIKE '%content block%' }}
```
{: id="20201224120448-ufqf1yh"}

It needs to be used on its own line. The script syntax used is SQL. For details, please refer to ((20201117103851-gx21lz6 "here")).
{: id="20201224120448-m5x1moo"}

### Example
{: id="20201224120448-8ew9ane"}

* {: id="20201224120448-wkokoaj"}Query list items that contain `content block`:
  {: id="20201224120448-6h7nng9"}

  ```sql
  !{{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND type = 'i' }}
  ```
  {: id="20201224120448-vogvrc7"}
* {: id="20201224120448-4ke7k9b"}The query content contains both `content block` and `reference` paragraph blocks:
  {: id="20201224120448-apivasm"}

  ```sql
    !{{ SELECT * FROM blocks WHERE content LIKE'%content block%' AND content LIKE'%reference%' }}
  ```
  {: id="20201224120448-bzzavtn"}
* {: id="20201224120448-n2nsjie"}The query content contains heading blocks of both `content block` and `embed`, and the first 2 items are selected in descending order of time:
  {: id="20201224120448-whs65cs"}

  ```sql
  !{{ SELECT * FROM blocks WHERE (content LIKE '%content block%' AND content LIKE '%embed%') AND type ='h' ORDER BY block_id DESC LIMIT 4 }}
  ```
  {: id="20201224120448-x2jp7sk"}
{: id="20201224120448-2uaiqr9"}

Let's actually run it to see the effect.
{: id="20201224120448-cl3wz81"}

#### Case 1
{: id="20201224120448-vagdm2b"}

The query contains paragraph blocks of both `In SiYuan` and `core concept` text, and excludes the current document (otherwise the paragraph block will also be included in the result set, because the current paragraph also contains these two texts. The following case is similar):
{: id="20201224120448-9gbg6ot"}

!{{SELECT * FROM blocks WHERE (content LIKE '%In SiYuan%' AND content LIKE '%core concept%') AND path NOT LIKE '%Content block dynamic query%'}}
{: id="20201224120448-xz2n8gx"}

#### Case 2
{: id="20201224120448-gx2xvjh"}

Query paragraph blocks that contain both tags `Content block/Embed` and `Content block/Reference`:
{: id="20201224120448-e0ohbtq"}

!{{SELECT * FROM blocks WHERE (content LIKE '%Content block/Embed%' OR content LIKE '%Content block/Reference%') AND path NOT LIKE '%Content block dynamic query%'}}
{: id="20201224120448-ww21jau"}

#### Case 3
{: id="20201224120448-508mr48"}

Sometimes we may need to randomly display content blocks to facilitate review.
{: id="20201224120448-vralmz9"}

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}
{: id="20201224120448-bmpyxnj"}


{: id="20201117112518-dott91x" type="doc"}

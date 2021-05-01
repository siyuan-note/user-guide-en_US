## Syntax
{: id="20201224120448-6jnrawi"}

The content block dynamic query is mainly used to summarize the required content blocks, and the method used is almost the same as that of search, supporting text mode and SQL mode. Use `{{` and `}}` to wrap text expressions or SQL scripts on a single line:
{: id="20210111230452-5lclhuo" updated="20210501171223"}

* {: id="20210111230452-7zr00k0"}Use text mode: `{{ Keyword }}`
  {: id="20210302223908-eckoja8" updated="20210501171232"}
* {: id="20210111230452-ppe5dev"}Use SQL mode: `{{ SELECT * FROM blocks WHERE content LIKE'%Keyword%' }}`, for details please refer to ((20201117103851-gx21lz6 "here"))
  {: id="20210302223908-9jg45et" updated="20210501171238"}
{: id="20210111230452-806gfrj"}

## Example
{: id="20201224120448-8ew9ane"}

* {: id="20201224120448-wkokoaj"}Query list items that contain `content block`:
  {: id="20201224120448-6h7nng9"}

  ```
  {{ i:content block }}
  ```
  {: id="20201224120448-vogvrc7"}
* {: id="20201224120448-4ke7k9b"}The query content contains both `content block` and `reference` paragraph blocks:
  {: id="20201224120448-apivasm"}

  ```
  {{ p:((content block) AND reference) }}
  ```
  {: id="20201224120448-bzzavtn"}
* {: id="20201224120448-n2nsjie"}The query content contains heading blocks of both `content block` and `embed`, and the first 2 items are selected in descending order of time:
  {: id="20201224120448-whs65cs"}

  ```sql
  {{ SELECT * FROM blocks WHERE (content LIKE '%content block%' AND content LIKE '%embed%') AND type ='h' ORDER BY block_id DESC LIMIT 2 }}
  ```
  {: id="20201224120448-x2jp7sk"}
{: id="20201224120448-2uaiqr9" updated="20210501171250"}

Let's actually run it to see the effect.
{: id="20201224120448-cl3wz81"}

### Case 1
{: id="20201224120448-vagdm2b"}

The query contains paragraph blocks of both `In SiYuan` and `core concept` text, and excludes the current document (otherwise the paragraph block will also be included in the result set, because the current paragraph also contains these two texts. The following case is similar):
{: id="20201224120448-9gbg6ot"}

!{{(p:"In SiYuan" AND "core concept") AND path:!"Content block dynamic query"}}
{: id="20210111231445-gwfrxnl"}

### Case 2
{: id="20201224120448-gx2xvjh"}

Query paragraph blocks that contain both tags `#Content block/Embed#` and `#Content block/Reference#`:
{: id="20201224120448-e0ohbtq"}

!{{SELECT * FROM blocks WHERE (content LIKE '%#Content block/Embed#%' OR content LIKE '%#Content block/Reference#%') AND path NOT LIKE '%Content block dynamic query%'}}
{: id="20201224120448-ww21jau"}

### Case 3
{: id="20201224120448-508mr48"}

Sometimes we may need to randomly roam and display content blocks to facilitate review.
{: id="20201224120448-vralmz9"}

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}
{: id="20201224120448-bmpyxnj"}


{: id="20201117112518-dott91x" type="doc"}

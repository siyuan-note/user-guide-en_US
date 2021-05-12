## Overview
{: id="20201224120448-6jnrawi" updated="20210512154707"}

The embed content block is mainly used to summarize the required content blocks, use `{{` and `}}` to wrap SQL scripts on a single line: `{{ SELECT * FROM blocks WHERE content LIKE'%Keyword%' }}`, database table please refer to ((20201117103851-gx21lz6 "here")). #Content block/Embed#
{: id="20210111230452-5lclhuo" updated="20210512154710"}

## Example
{: id="20201224120448-8ew9ane"}

* {: id="20201224120448-wkokoaj"}Query list items that contain `content block`:
  {: id="20201224120448-6h7nng9"}

  ```sql
  {{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND type = 'i' }}
  ```
  {: id="20201224120448-vogvrc7"}
* {: id="20201224120448-4ke7k9b"}The query content contains both `content block` and `reference` paragraph blocks:
  {: id="20201224120448-apivasm"}

  ```sql
  {{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND content LIKE '%reference%' AND type = 'p') }}
  ```
  {: id="20201224120448-bzzavtn"}
* {: id="20201224120448-n2nsjie"}The query content contains heading blocks of both `content block` and `embed`, and the first 2 items are selected in descending order of update time:
  {: id="20201224120448-whs65cs" updated="20210503152045"}

  ```sql
  {{ SELECT * FROM blocks WHERE content LIKE '%content block%' AND content LIKE '%embed%' AND type ='h' ORDER BY updated DESC LIMIT 2 }}
  ```
  {: id="20201224120448-x2jp7sk"}
{: id="20201224120448-2uaiqr9" updated="20210503152127"}

### Case 1
{: id="20201224120448-vagdm2b"}

The query contains paragraph blocks of both `In SiYuan` and `core concept` text, and excludes the current document (otherwise the paragraph block will also be included in the result set, because the current paragraph also contains these two texts. The following case is similar):
{: id="20201224120448-9gbg6ot"}

!{{SELECT * FROM blocks WHERE content LIKE '%In SiYuan%' AND content LIKE '%core concept%' AND path NOT LIKE '%Embed Content Block%'}}
{: id="20210111231445-gwfrxnl"}

### Case 2
{: id="20201224120448-gx2xvjh"}

Query paragraph blocks that contain both tags `#Content block/Embed#` and `#Content block/Reference#`:
{: id="20201224120448-e0ohbtq"}

!{{SELECT * FROM blocks WHERE (content LIKE '%#Content block/Embed#%' OR content LIKE '%#Content block/Reference#%') AND path NOT LIKE '%Embed Content Block%'}}
{: id="20201224120448-ww21jau"}

### Case 3
{: id="20201224120448-508mr48"}

Sometimes we may need to randomly roam and display content blocks to facilitate review.
{: id="20201224120448-vralmz9"}

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}
{: id="20201224120448-bmpyxnj"}


{: id="20201117112518-dott91x" type="doc"}

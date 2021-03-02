## Global search
{: id="20201230105105-78pxcj3"}

Trigger the search box via <kbd>Ctrl P</kbd> / <kbd>⌘ P</kbd>, support two modes:
{: id="20201230105105-53h62re" updated="20210302223746"}

* {: id="20201230105105-4ehgu59"}((20201222100328-kzqg0mz "Text mode")): Can cover most query scenarios with concise syntax
  {: id="20210302223744-6r387x3"}
* {: id="20201230105105-jgzn24z"}((20201222100339-i5hzcph "SQL mode")): Able to achieve complex query requirements, friendly to programmers
  {: id="20210302223744-8f8ners"}
{: id="20201230105105-8fuimro"}

## Content block reference search
{: id="20201230105105-xwodyzr"}

Content block reference/embedded search, in the editor document by typing `((keyword` to trigger, support ((20201222100222-q47d64s "Type filtering")).
{: id="20201230105105-ccbssgd"}

#Note#: Global search and block ref search only return the direct sub-blocks at the root level of the document when no type filter is specified. For example, the document structure is as follows:
{: id="20201230111223-blg0opd"}

```markdown
## Heading

Paragraph 1.

* List
  * Child List
   
    Child Paragraph.

Paragraph 2.
```
{: id="20201230111252-1vpgd4n"}

When using `gra` as the search condition, only `Paragraph 1` (type `p`), `List` (type `l`) and `Paragraph 2` (type `p`) are returned. If you need to return a sub-block of a non-root container block, you need to use the type filter `i:gra`, then return two list item blocks `List` (type `i`) and `Child List` (type `i`).
{: id="20201230111314-e0rdu8y"}

## Relation graph search
{: id="20201230105105-fqu6x6v"}

Relation graph search, filter nodes and connections based on keywords in the relation graph.
{: id="20201230105105-7ke5gy9"}


{: id="20200924100839-5oe1j4n" type="doc"}

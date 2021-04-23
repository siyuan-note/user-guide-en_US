For ((20200924101106-19z4kaa "content block")), the most valuable way to use it is to link them through ((20200924101312-jj4e0v3 "Content block reference")) and ((20200924101312-385dey5 "Content block embedding")). A good link is directional:
{: id="20210104091542-v1yca4p" updated="20210302223858"}

* {: id="20210104091542-ctguz9s"}Forwardlink, that is, which other content blocks are used in the current content block
  {: id="20210302223856-grgney1"}
* {: id="20210104091542-7fy85lw"}Backlink, that is, the current content block is used by those other content blocks
  {: id="20210302223856-qk6hr9b"}
{: id="20210104091542-9h3i9dh"}

The forward link is included in the content of the current block, which we can see intuitively. Backlinks need to be searched in other documents to know, and it is precisely this information that is more valuable to us. We can use the following two ways to help us better grasp the knowledge points or diverge ideas:
{: id="20210104091542-hbzfsn5"}

* {: id="20210104091542-1ryw6y3"}((20200924101210-zwf8ags "Graph")): browse forward and backward link relationships between content blocks
  {: id="20210302223856-ngw7ijw"}
* {: id="20210104091542-40sj7jl"}((20200924101210-3qfiiat "Backlinks")): Display the backlinks of the current content block as a text list
  {: id="20210302223856-y92ousb"}
{: id="20210104091542-rlv1299"}

### Content block reference
{: id="20200924101312-jj4e0v3"}

Entering `((` will trigger the content block quotation search, continue to enter as the search keyword, use the up and down keys to select in the search results and press Enter to complete the content block quotation. #Note#: that cross-notebook references are not supported.
{: id="20210104091542-6dj8jvc"}

The complete syntax of the content block quote is: `((id "text"))`, where the `id` is like: `202008250000-a1b2c3d`, consisting of time and 7 random characters, the content block id is when the content block is created It will be automatically generated; the following `text` is the custom anchor text for the content block in the quote. After the content block quote is established, hover the mouse over the anchor text and a preview floating layer will pop up to show the quoted content block. #Content block/Reference#
{: id="20210104091542-ev4hpxo"}

### Content block embedding
{: id="20200924101312-385dey5"}

Enter `!((` at the beginning of a new line and it will trigger the content block embedded search. Just like the content block reference, you can complete the embedding by selecting the content block you need in the search results. It also supports custom `text` anchor text After the embedding operation is completed, the embedded content block will be displayed directly below. #Content block/Embed#
{: id="20210104091542-a81lx0q"}

#Note#: the content block embedding itself is also a kind of content block, which means that we cannot use the content block embedding in the middle of a sentence, and can only embed at the beginning of a new line.
{: id="20210104091542-23pgmmz" updated="20210423103419"}


{: id="20200924101256-f8b1sbi" type="doc"}

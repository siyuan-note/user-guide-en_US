For ((20200924101106-19z4kaa "content block")), the most valuable way to use it is to link them through ((20200924101312-jj4e0v3 "Content block reference")) and ((20200924094024-s0oyhvp "Content block embedding")). A good link is directional:

* Forwardlink, that is, which other content blocks are used in the current content block
* Backlink, that is, the current content block is used by those other content blocks

The forward link is included in the content of the current block, which we can see intuitively. Backlinks need to be searched in other documents to know, and it is precisely this information that is more valuable to us. We can use the following two ways to help us better grasp the knowledge points or diverge ideas:

* ((20200924101210-zwf8ags "Graph")): browse forward and backward link relationships between content blocks
* ((20200924101210-3qfiiat "Backlinks")): Display the backlinks of the current content block as a text list

### Content block reference
{: id="20200924101312-jj4e0v3"}

Entering `((` will trigger the content block quotation search, continue to enter as the search keyword, use the up and down keys to select in the search results and press Enter to complete the content block quotation. #Note#: that cross-notebook references are not supported.

The complete syntax of the content block quote is: `((id "text"))`, where the `id` is like: `202008250000-a1b2c3d`, consisting of time and 7 random characters, the content block id is when the content block is created It will be automatically generated; the following `text` is the custom ((20201123093328-4q4cws1 "anchor text")) for the content block in the quote. After the content block quote is established, hover the mouse over the anchor text and a preview floating layer will pop up to show the quoted content block. #Content block/Reference#

### Content block embedding
{: id="20200924101312-385dey5"}

Enter `!((` at the beginning of a new line and it will trigger the content block embedded search. Just like the content block reference, you can complete the embedding by selecting the content block you need in the search results. It also supports custom `text` ((20201123093328-4q4cws1 "anchor text")) After the embedding operation is completed, the embedded content block will be displayed directly below. #Content block/Embed#

#Note#: the content block embedding itself is also a kind of content block, which means that we cannot use the content block embedding in the middle of a sentence, and can only embed at the beginning of a new line. The following is an example of content block embedding:

!((20200923234102-fota8wn "Content block embed example"))

### Anchor text
{: id="20201123093328-4q4cws1"}

The content block reference and embedding syntax described above support setting anchor text. In addition to setting the anchor text as a fixed content, it also supports the use of template variables so that it can dynamically follow the changes of the definition block. The anchor text template variables currently supported are as follows:

* `{{.title}}`: Use definition block title to fill. If the definition block itself is a document block or heading block, use the document name or title text to fill the variable; if it is another content block, use the upper heading of the block to fill, if there is no upper heading, use the document name to fill
* `{{.text}}`: Use definition block content text to fill


{: id="20200924101256-f8b1sbi" type="doc"}

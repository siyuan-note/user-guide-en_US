## Correspondence between Document and Heading

The heading block and the document block have a natural correspondence, because:

* Each document block has a name
* Each heading block also has a name

So we can convert between the document block and the heading block. In addition, because the content block is referenced based on id, the conversion process will not break the existing reference relationship.

## Convert Document block to Heading block

In the file tree, select the document that needs to be converted into a heading block, and then drag it to the position to be inserted in the editor tab. There are two situations here:

1. Place the document block on the existing heading block, and the document block will be inserted below as the level node of the heading block
2. Place the document block on a non-heading block, and the document block will be inserted as a child node of the heading block to which the block belongs

After the document block is converted to a heading block:

* The original document name will become the heading name
* Logically, the document block is a first-level title, and the relative level will be changed according to the insertion position
* Each heading level in the original document will be adjusted according to the insertion position
  * For the above situation 1: For example, if the original document contains the first, second, and third level headings, and the insertion position is a second-level heading, the heading block after the document block conversion will be a second-level heading. Level 3 headings will become Level 2, 3, and 4 headings
  * For the second case above: For example, the original document contains headings of level 1, 2, and 3, and the insertion position is a paragraph block under a level 2 heading. The heading block after the conversion of the document block will be a level 3 heading. Level 1, 2, and 3 headings will become Level 3, 4, and 5 headings

## Convert Heading block to Document block

In the editor tab, select the heading block to be converted, press and hold the heading block icon, and then drag it to the folder to be placed in the file tree. If you need to place it on the notebook root folder, drag the heading block icon to the top notebook icon row.

After the heading block is converted to a document block:

* The heading name will become the document name
* If there are subtitles under the original heading block, the largest level of these subtitles will be used as the first level of the new document, and the remaining subtitles will be adjusted according to the relative level
  * For example, the original heading block contains three, four, and five levels of subtitles, and these subtitles will be converted into one, two, and three levels after being converted into a document block


{: id="20201210233038-3xr19g5" type="doc"}

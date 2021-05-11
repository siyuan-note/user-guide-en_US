## Correspondence between Document and Heading
{: id="20210104091550-oyzs64s"}

The heading block and the document block have a natural correspondence, because:
{: id="20210104091550-stqtr5k"}

* {: id="20210104091550-kfphjkv"}Each document block has a name
  {: id="20210302223904-ak8zul2" updated="20210302223906"}
* {: id="20210104091550-cod7uyo"}Each heading block also has a name
  {: id="20210302223904-3rbkt5r"}
{: id="20210104091550-c9m7yo3"}

So we can convert between the document block and the heading block. In addition, because the content block is referenced based on id, the conversion process will not break the existing reference relationship.
{: id="20210104091550-0izuikh"}

## Convert Document block to Heading block
{: id="20210104091550-5sh49go"}

In the doc tree, select the document that needs to be converted into a heading block, and then drag it to the position to be inserted in the editor tab. There are two situations here:
{: id="20210104091550-rbetlgr"}

1. {: id="20210104091550-12grx1a"}Place the document block on the existing heading block, and the document block will be inserted below as the level node of the heading block
   {: id="20210302223904-ytpydxa"}
2. {: id="20210104091550-a5hh8bg"}Place the document block on a non-heading block, and the document block will be inserted as a child node of the heading block to which the block belongs
   {: id="20210302223904-4rlhclw"}
{: id="20210104091550-qfc4zlm"}

After the document block is converted to a heading block:
{: id="20210104091550-9sy6z40"}

* {: id="20210104091550-7unpq37"}The original document name will become the heading name
  {: id="20210302223904-bzkmex1"}
* {: id="20210104091550-hi3ky7o"}Logically, the document block is a first-level title, and the relative level will be changed according to the insertion position
  {: id="20210302223904-l78gsey"}
* {: id="20210104091550-cumad9i"}Each heading level in the original document will be adjusted according to the insertion position
  {: id="20210302223904-dsfeeh6"}

  * {: id="20210104091550-q8xxl8s"}For the above situation 1: For example, if the original document contains the first, second, and third level headings, and the insertion position is a second-level heading, the heading block after the document block conversion will be a second-level heading. Level 3 headings will become Level 2, 3, and 4 headings
    {: id="20210302223904-z5rbkfi"}
  * {: id="20210104091550-ks1lqvh"}For the second case above: For example, the original document contains headings of level 1, 2, and 3, and the insertion position is a paragraph block under a level 2 heading. The heading block after the conversion of the document block will be a level 3 heading. Level 1, 2, and 3 headings will become Level 3, 4, and 5 headings
    {: id="20210302223904-hwh19uj"}
  {: id="20210104091550-rbvitpg"}
{: id="20210104091550-zq0ph0f"}

## Convert Heading block to Document block
{: id="20210104091550-fualfrs"}

In the editor tab, select the heading block to be converted, press and hold the heading block icon, and then drag it to the folder to be placed in the doc tree. If you need to place it on the notebook root folder, drag the heading block icon to the top notebook icon row.
{: id="20210104091550-1pe70bg"}

After the heading block is converted to a document block:
{: id="20210104091550-atbf12t"}

* {: id="20210104091550-85231ks"}The heading name will become the document name
  {: id="20210302223904-brosops"}
* {: id="20210104091550-s2nrev0"}If there are subtitles under the original heading block, the largest level of these subtitles will be used as the first level of the new document, and the remaining subtitles will be adjusted according to the relative level
  {: id="20210302223904-mleww72"}

  * {: id="20210104091550-o45r6uw"}For example, the original heading block contains three, four, and five levels of subtitles, and these subtitles will be converted into one, two, and three levels after being converted into a document block
    {: id="20210302223904-62szx4g"}
  {: id="20210104091550-c8bmph5"}
{: id="20210104091550-nsd8w2j"}


{: id="20201210233038-3xr19g5" type="doc"}

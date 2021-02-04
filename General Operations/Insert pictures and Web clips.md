## Insert picture
{: id="20201210194734-v2rmiaq"}

In the editor, you can directly paste the copied picture from the system clipboard, and the picture file will be copied to the assets folder at the same level as the current document. You can also insert pictures by dragging and dropping picture files into the editor.
{: id="20210104091430-uqs502r"}

If you use the standard Markdown syntax `![alt](assets/image "title")` to specify a title, then `title` will be rendered below the image as a legend, and the title part of the text supports span-level typesetting, such as bold, Italics, formulas, etc.
{: id="20210104091430-tj5w1co"}

![SiYuan.png](assets/SiYuan.png "*When one drinks water, one must not forget where it comes from*"){: parent-style="display: block; text-align: center;"}
{: id="20210104091430-yd3zyeu"}

If you need to adjust the size and position of the picture, please right-click the picture and select zoom and position from the drop-down menu.
{: id="20210204172633-q2q1r7i"}

## Clips
{: id="20210104091430-bxc6t2h"}

Through the "Clip" function, we can paste other rich text content (such as Web pages, Word, Excel, etc.) into the editor, and SiYuan will automatically convert it into standard Markdown text.
{: id="20210104091430-ktqjqwj"}

The specific usage is to manually select the content of the webpage, for example, select the text part of the webpage article to copy, and then paste it in SiYuan. Do not select all pages to copy, otherwise you may not be able to paste any content.
{: id="20210104091430-zr3uc63"}

If you check Settings - Assets - Auto fetch remote image to local, the clip will download the picture files on the Web page to assets folder and replace the picture address in the content with the local assets path.
{: id="20210104091430-aihyfq1"}

## Cleanup unreferenced assets
{: id="20210115224203-q8bj2gd"}

"Reference" refers to the link `[foo](bar)` through Markdown, the image syntax `![foo](bar)` or the attribute `src` of HTML tags (such as `<img>`, `<iframe>`) link the asset files (files under the assets folder). There are two situations:
{: id="20210115224203-he7ycn9"}

1. {: id="20210115224203-1g8zvdg"}Reference to a specific asset file, such as a picture or a file
   {: id="20210204172630-7rtyepg"}
2. {: id="20210115224203-xb0ycqg"}Reference to a asset folder (a subfolder under the assets folder) must end with `/`, such as `[foo](assets/bar/)`
   {: id="20210204172630-kq680iv"}
{: id="20210115224203-r3mwskz"}

The second case is special: if a asset folder is referenced, all the following asset files will be counted as already referenced regardless of whether they are individually referenced.
{: id="20210115224203-hb1ykk2"}

In Settings - Assets, you can clean up unreferenced assets by one-click. If you need to retrieve files that have been deleted by mistake, please via ((20210104091559-kgrtuyh "local repository rollback")).
{: id="20210115224203-e03wglt"}

#Note#: Using absolute paths (local or network paths) will not be included Clean up calculations.
{: id="20210130103832-93r5ddp"}


{: id="20200924100744-br924ar" type="doc"}

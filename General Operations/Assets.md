## Overview
{: id="20210503095708-2g6bgl4" updated="20210503095731"}

All attachment files inserted through the editor are asset files, and they will be placed in the data/assets folder of the workspace.
{: id="20210503095710-1vp1uxw" updated="20210503095750"}

## Insert picture
{: id="20201210194734-v2rmiaq"}

In the editor, you can directly paste the copied picture from the system clipboard, or you can also insert pictures by dragging and dropping picture files into the editor.
{: id="20210104091430-uqs502r" updated="20210503095810"}

If you specify a title for a picture, then the title will be rendered below the image as a legend, and the title part of the text supports span-level typesetting, such as bold, Italics, formulas, etc.
{: id="20210104091430-tj5w1co" updated="20210417113148"}

![SiYuan.png](assets/SiYuan-20210512171727-0xnnlw8.png "When one drinks water, one must not forget where it comes from"){: parent-style="display: block; text-align: center; white-space: initial;"}
{: id="20210104091430-yd3zyeu" updated="20210512171730"}

## Cleanup unreferenced assets
{: id="20210115224203-q8bj2gd"}

"Reference" refers to the link `[foo](bar)` through Markdown, the image syntax `![foo](bar)` or the attribute `src` of HTML tags (such as `<img>`, `<iframe>`) link the asset files. There are two situations:
{: id="20210115224203-he7ycn9" updated="20210503095907"}

1. {: id="20210115224203-1g8zvdg"}Reference to a specific asset file, such as a picture or a file
   {: id="20210204172630-7rtyepg"}
2. {: id="20210115224203-xb0ycqg"}Reference to a asset folder (a subfolder under the assets folder) must end with `/`, such as `[foo](assets/bar/)`
   {: id="20210204172630-kq680iv"}
{: id="20210115224203-r3mwskz"}

The second case is special: if a asset folder is referenced, all the following asset files will be counted as already referenced regardless of whether they are individually referenced.
{: id="20210115224203-hb1ykk2"}

In <kbd>Settings</kbd> - <kbd>Assets</kbd>, you can clean up unreferenced assets by one-click. If you need to retrieve files that have been deleted by mistake, please via ((20210104091559-kgrtuyh "Rollback")).
{: id="20210115224203-e03wglt" updated="20210512160530"}

#Note#: Using absolute paths (local or network paths) will not be included Clean up calculations.
{: id="20210130103832-93r5ddp"}


{: id="20200924100744-br924ar" type="doc"}

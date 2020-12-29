## Import
{: id="20201229152405-ivntzua"}

When you use SiYuan to open a local folder or connect to WebDAV, SiYuan will convert the Markdown files (`.md` and `.markdown`) in the path:
{: id="20201229152405-a3csud5"}

* {: id="20201229152405-mqaa41i"}Documents that do not contain `{: id="" type="doc"}` in in the existing Markdown content will be regarded as files to be imported
* {: id="20201229152405-vwg2kjn"}Automatically convert `[[link|text]]` in the file to be imported into content block reference (only handle `link` as full path or relative path)
* {: id="20201229152405-c7zqv5e"}Automatically convert `#tag` to `#tag#`
{: id="20201229152405-d5sbj00"}

The converted Markdown file uses kramdown syntax. For details, please see ((20200924095851-u5jmzr3 "Storage format")).
{: id="20201229152405-izrrksv"}

## Export
{: id="20201229152405-vlhitro"}

Copy (Ctrl C) in the editor is ((20200924100600-knx7ub0 "formatted Markdown text")).
{: id="20201229152405-ghscnap"}

Right-click and select "Export" after selecting the document in the file tree:
{: id="20201229152405-wqguawh"}

* {: id="20201229152405-ggpurvj"}Markdown: Markdown files complying with GFM/CommonMark standards
* {: id="20201229152405-77568gf"}[TextBundle](http://textbundle.org): Package Markdown and its associated resource files to provide better Markdown migration
* {: id="20201229152405-lfebmzi"}PDF
{: id="20201229152405-kpk3qdy"}

If you need to export more formats, please complete via [Pandoc](https://pandoc.org).
{: id="20201229152405-0kx9qg6"}


{: id="20200924100808-j9sddk9" type="doc"}

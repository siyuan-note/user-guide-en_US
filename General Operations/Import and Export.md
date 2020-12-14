## Import

When you use SiYuan to open a local folder or connect to WebDAV, SiYuan will convert the Markdown files (`.md` and `.markdown`) in the path:

* Documents that do not contain `{: id="" type="doc"}` in in the existing Markdown content will be regarded as files to be imported
* Automatically convert `[[link|text]]` in the file to be imported into content block reference (only handle `link` as full path or relative path)
* Automatically convert `#tag` to `#tag#`

The converted Markdown file uses kramdown syntax. For details, please see ((20200924095851-u5jmzr3 "Storage format")).

## Export

Copy (Ctrl C) in the editor is ((20200924100600-knx7ub0 "formatted Markdown text")). If you need to export standard Markdown files, you can right-click on the file tree document and select "Export". If you need to export automatically during editing, please check "Auto Export" in `Settings - Export`.

The right-click export on the file tree also supports packaging Markdown and its associated resource files through [TextBundle](http://textbundle.org), which can provide better Markdown migration.


{: id="20200924100808-j9sddk9" type="doc"}

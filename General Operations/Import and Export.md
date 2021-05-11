## Import
{: id="20201229152405-ivntzua"}

Right-click and select "Import" after selecting a folder on the doc tree, and you can choose to import a folder or a single file in the secondary menu.
{: id="20210120161035-zxkyg0w" updated="20210302223730"}

The import process mainly completes the following conversion processing:
{: id="20210120155800-zxa7194"}

* {: id="20210120155800-skvb3nx"}Parse and generate content blocks
  {: id="20210302223727-7qa4h3g"}
* {: id="20210120155800-lscebcp"}Convert `[[link|text]]` to content block reference
  {: id="20210302223727-gdmpvir"}
* {: id="20210120155800-f31147b"}Convert `#tag `to `#tag#`
  {: id="20210302223727-jt3b8sz" updated="20210417113309"}
{: id="20210120155800-i46fkz7"}

#Note#: Copying standard Markdown files directly to the notebook folder on the system will not be automatically converted, and the import function must be used.
{: id="20210127230807-5medqfv"}

## Export
{: id="20201229152405-vlhitro"}

### Edit content copy
{: id="20210120155909-y3e52s3"}

After selecting the content in the editor, you can see the copy option in the right-click menu:
{: id="20210120155909-ct288u8"}

* {: id="20210120155909-nn8tpwk"}Copy: mainly used inside SiYuan (kramdown)
  {: id="20210302223727-ty6z9qp"}
* {: id="20210120155909-zj9dg0j"}Copy as standard Markdown: copy to a place other than SiYuan
  {: id="20210302223727-knjree5"}
{: id="20210120155909-ouc1le7"}

### Full text export
{: id="20210120155909-lx3y6by"}

Right-click and select "Export" after selecting the document in the doc tree:
{: id="20210120155909-08i894p"}

* {: id="20210120155909-48jy3x5"}Markdown: Markdown files complying with GFM/CommonMark standards
  {: id="20210302223727-xscow91"}
* {: id="20210120155909-27u47et"}[TextBundle](http://textbundle.org): Package Markdown and its associated asset files to provide better Markdown migration
  {: id="20210302223727-g2hc973" updated="20210503100034"}
* {: id="20210120155909-f9oo9lr"}PDF
  {: id="20210302223727-wscm47q"}
* {: id="20210120155909-bglztv7"}HTML
  {: id="20210302223727-wbonhn9"}
{: id="20210120155909-3j6fzii"}

If you need to export more formats, please complete via [Pandoc](https://pandoc.org).
{: id="20210120155909-pc5gzx7"}

Select a folder on the doc tree and right-click and select "Export" to export in batches. The export is a standard Markdown file compression package.
{: id="20210120155909-5d1u5zc"}


{: id="20200924100808-j9sddk9" type="doc"}

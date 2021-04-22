## Markdown specifications and extensions
{: id="20210104091524-aa7klsh" updated="20210302223840"}

Markdown is popular because of its simplicity and versatility. After standardization through the GFM/CommonMark specification, almost all platforms and software that support Markdown have been implemented.
{: id="20210104091524-doh26q0"}

At present, this is recognized as "pure" Markdown, and there are not so many "bells and whistles". Users can rest assured to use, versatility and migration can be guaranteed to the greatest extent.
{: id="20210104091524-7qo2rd1"}

However, the GFM specification cannot meet some "modern" usage requirements, so many software introduces some extended syntax (such as superscript and subscript, footnotes, formulas, diagrams, etc.), although these extended syntax may not be universal on other platforms and software , But it can meet the specific needs of users on the platform and software, and then provide a wider range of format support through the export function.
{: id="20210104091524-k4bjeql"}

## Forward or backward
{: id="20210104091524-qmcugqc"}

After going further and further on the road of expanded grammar, we found that this seems to be a historical reversal. With the introduction of more specific grammars, the versatility of Markdown is gradually lost, as if it has become a proprietary format of specific software. More ironically, the introduction of grammar cannot solve the biggest problem of Markdown-its own resource files (although TextBundle/TextPack has made some efforts, it is basically not universal at present).
{: id="20210104091524-ww8manc"}

The more powerful the function, the more complicated the grammar. If you go along this road, the complexity of the grammar may exceed the human readable ability, which will completely lose the meaning of Markdown.
{: id="20210104091524-txt6lef"}

For developers, another way is not to choose Markdown text as the storage format at the beginning, but to use a more structured storage method, such as a database or JSON, and then support Markdown syntax typesetting at the application level. Developers who choose this path may have foreseen possible complex scenarios in the future.
{: id="20210104091524-sivdyxv"}

## User perspective
{: id="20210104091524-cmlb0fp"}

* {: id="20210104091524-df2d0d8"}"I want Markdown standard text so that other software can edit and view"
  {: id="20210302223838-z2cg8zu"}
* {: id="20210104091524-333tzzd"}"I want WYSIWYG editing mode, the split screen is too uncomfortable for me"
  {: id="20210302223838-fkmfhbv"}
* {: id="20210104091524-jxwr136"}"I want source code editing mode, this is the essence of Markdown, and I can render with the naked eye..."
  {: id="20210302223838-i977b97"}
* {: id="20210104091524-cwd47ou"}"I want to add color to the text, I want the horizontal layout, and I want the image zoom"
  {: id="20210302223838-k3n0o42"}
* {: id="20210104091524-o419gwt"}"I want to nest tables and merge cells"
  {: id="20210302223838-jsm9gzl"}
* {: id="20210104091524-w8gauww"}……
  {: id="20210302223838-129sgkh"}
* {: id="20210104091524-6e9q7en"}"What? This won't work, goodbye!"
  {: id="20210302223838-mpz2jwf"}
{: id="20210104091524-ciwnvtq"}

> There are only two kinds of languages: the ones people complain about and the ones nobody uses.
> {: id="20210104091524-79razfb"}
{: id="20210104091524-hpucoc2"}

Markdown is obviously the former.
{: id="20210104091524-1o6obbf"}


{: id="20201214230103-vwt7v43" type="doc"}

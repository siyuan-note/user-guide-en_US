## Markdown specifications and extensions

Markdown is popular because of its simplicity and versatility. After standardization through the GFM/CommonMark specification, almost all platforms and software that support Markdown have been implemented.

At present, this is recognized as "pure" Markdown, and there are not so many "bells and whistles". Users can rest assured to use, versatility and migration can be guaranteed to the greatest extent.

However, the GFM specification cannot meet some "modern" usage requirements, so many software introduces some extended syntax (such as superscript and subscript, footnotes, formulas, diagrams, etc.), although these extended syntax may not be universal on other platforms and software , But it can meet the specific needs of users on the platform and software, and then provide a wider range of format support through the export function.

## Forward or backward

After going further and further on the road of expanded grammar, we found that this seems to be a historical reversal. With the introduction of more specific grammars, the versatility of Markdown is gradually lost, as if it has become a proprietary format of specific software. More ironically, the introduction of grammar cannot solve the biggest problem of Markdown-its own resource files (although TextBundle/TextPack has made some efforts, it is basically not universal at present).

The more powerful the function, the more complicated the grammar. If you go along this road, the complexity of the grammar may exceed the human readable ability, which will completely lose the meaning of Markdown.

For developers, another way is not to choose Markdown text as the storage format at the beginning, but to use a more structured storage method, such as a database or JSON, and then support Markdown syntax typesetting at the application level. Developers who choose this path may have foreseen possible complex scenarios in the future.

## User perspective

* "I want Markdown standard text so that other software can edit and view"
* "I want to render and edit in real time, the split screen is too uncomfortable for me"
* "I want source code editing mode, this is the essence of Markdown, and I can render with the naked eye..."
* "I want to add color to the text, I want the horizontal layout, and I want the image zoom"
* "I want to nest tables and merge cells"
* ……
* "What? This won't work, goodbye!"

> There are only two kinds of languages: the ones people complain about and the ones nobody uses.

Markdown is obviously the former.


{: id="20201214230103-vwt7v43" type="doc"}

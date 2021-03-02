## Logic conjunction
{: id="20201224120448-sur61q1" updated="20210302223454"}

Support operators `AND`, `OR` and `NOT` (note that capitalization is required). For example, `foo AND bar OR baz` means both foo and bar or baz; `foo NOT bar` means foo but not bar.
{: id="20201224120448-yei9n1e"}

* {: id="20201224120448-pu2kash"}`AND` can be omitted, for example, `foo AND bar` can be abbreviated as `foo bar`
  {: id="20210227102727-osv3hov"}
* {: id="20201224120448-ufj7cne"}`OR` can be replaced by `||`, `AND` can be replaced by `&&`, such as `foo && bar || baz`
  {: id="20210227102727-xukywn3"}
* {: id="20201224120448-tdpdev9"}`NOT` can be abbreviated as prefix `!` or `-`, for example, `foo NOT bar` can be abbreviated as `foo !bar` or `foo -bar`
  {: id="20210227102727-kuhz54o"}
{: id="20201224120448-7hjhl5g"}

## Exact match
{: id="20201224120448-59thpwc"}

Support for specifying exact matching through `""`, for example, `"foo"` means that exact match contains foo; `foo !"bar baz"` contains foo and does not contain bar baz.
{: id="20201224120448-s1dedv5"}

## Fuzzy match
{: id="20201224120448-2n0dios"}

* {: id="20201224120448-sged3z7"}Supports specifying a single character through `?`, for example, `f?o` can be fuzzy matching fo, fao, fbo
  {: id="20210227102727-4gwvq7q"}
* {: id="20201224120448-yytqban"}Support specifying multiple characters through `*`, for example, `f*o` can be fuzzy matching fo, fao, fabco
  {: id="20210227102727-ecnfk3w"}
{: id="20201224120448-vml16gr"}

## Regular match
{: id="20201224120448-ik0lpla"}

Supports specifying regular expressions through `/foo/`. For example, `/f[a-z]{2}/` can match up to the beginning of f followed by two a-z letters.
{: id="20201224120448-efh0obj"}

## Group
{: id="20201224120448-fbbntgh"}

Supports specifying priority through `()`, for example, `foo AND (bar OR baz)` means to include foo bar or foo baz at the same time.
{: id="20201224120448-87llfaw"}

## Specify field
{: id="20201224120448-jojjs8o"}

* {: id="20201224120448-5n2lr4o"}`path`: supports specifying the document path through `path:foo`, for example, `path:!foo` means searching in documents that do not contain the path foo; `path:(foo OR bar)` means the path is foo Or search in the documentation of bar
  {: id="20210227102727-pw144od"}
* {: id="20201224120448-5a519a3"}`type`: Supports specifying the content block type through `type:foo`, available types please refer to ((20201222100222-q47d64s "Type filtering")). For example, `type:h` means searching in the heading; `type:(m OR c)` means searching in a mathematical formula block or code block
  {: id="20210227102727-97vwz6l"}

  * {: id="20201225171153-5uu0mrq"}The `AND` logical conjunction of keywords and types supports abbreviation. For example, `foo type:h` can be abbreviated as `h:foo`; `(foo OR bar) type:l` can be abbreviated as `l:(foo OR bar) `. But `foo type:(l OR h)` cannot be abbreviated as `(l OR h):foo`, which means that the specified field must be a specific one
    {: id="20210227102727-a4baqet"}
  {: id="20201225171154-ujt8hoc"}
* {: id="20210112163745-3n24sso"}`markdown`: the default is to search on plain text. If you need to search the original Markdown text, use `markdown:foo`. For example, you can search the to-do list by `markdown:"[] "AND type:l`
  {: id="20210227102727-6aec2x4"}
{: id="20201224120448-48l2e0q"}

## Specify time range
{: id="20201224120448-sdjlz5y"}

Support to specify the content block creation time through `created: [20200219 TO 20200825]`, for example, `created: [20200219163030 TO 20200825]` means that from February 19th, 2020 at 16:30:30 PM to August 25th, 2020 at 00: 00: 00: 00 search in the content block created.
{: id="20201224120448-wi1kjaz" updated="20210227102855"}

* {: id="20201224120448-s2w7388"}`[` means greater than or equal to, `{` means greater than; `]` means less than or equal to, `}` means less than
  {: id="20210227102727-44lqlod"}
* {: id="20201224120448-np8fi3u"}You can mix `[` and `{`, such as `created: [20200219 TO 20200825}`
  {: id="20210227102727-zckosot"}
* {: id="20210227102742-eq10nk5"}If you need to query by update time, replace `created` with `updated`
  {: id="20210227102742-e19f0tb" updated="20210227102742"}
{: id="20201224120448-brfxvtb" updated="20210227102800"}

## Escape character
{: id="20201225090933-mcc6ctz"}

If you need to search for special characters that appear in the expression syntax, you need to use `\` to escape them. These special characters include: `+-&|!()"?*[]{}:/`. For example, `\(foo \[bar \-baz` will search for (foo [bar -baz.
{: id="20201225090933-h1qx9jb"}


{: id="20201222100328-kzqg0mz" type="doc"}

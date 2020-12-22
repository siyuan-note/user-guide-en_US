## Logic conjunction
{: id="20201222215050-d5m9lhd"}

Support operators `AND`, `OR` and `NOT` (note that capitalization is required). For example, `foo AND bar OR baz` means both foo and bar or baz; `foo NOT bar` means foo but not bar .
{: id="20201222215050-7p44ua6"}

* {: id="20201222215050-m9ao1zd"}`AND` can be omitted, for example, `foo AND bar` can be abbreviated as `foo bar`
* {: id="20201222215050-ywlzdqn"}`OR` can be replaced by `||`, `AND` can be replaced by `&&`, such as `foo && bar || baz`
* {: id="20201222215050-6ysl1ld"}`NOT` can be abbreviated as prefix `!` or `-`, for example, `foo NOT bar` can be abbreviated as `foo !bar` or `foo -bar`
{: id="20201222215050-duaevku"}

## Exact match
{: id="20201222215050-wm2qhvh"}

Support for specifying exact matching through `""`, for example, `"foo"` means that exact match contains foo; `foo !"bar baz"` contains foo and does not contain bar baz.
{: id="20201222215050-fp1cc3v"}

## Fuzzy match
{: id="20201222215050-hkjgu0g"}

* {: id="20201222215050-wd5tl4b"}Supports specifying a single character through `?`, for example, `f?o` can be fuzzy matching fo, fao, fbo.
* {: id="20201222215050-8ehu17j"}Support specifying multiple characters through `*`, for example, `f*o` can be fuzzy matching fo, fao, fabco.
{: id="20201222215050-dwhhe00"}

## Group
{: id="20201222215050-1xcw8q8"}

Supports specifying priority through `()`, for example, `foo AND (bar OR baz)` means to include foo bar or foo baz at the same time.
{: id="20201222215050-n6f3ps8"}

## Specify field
{: id="20201222215050-hktn5gr"}

* {: id="20201222215050-jr9gbsc"}`path`: supports specifying the document path through `path:foo`, for example, `path:!foo` means searching in documents that do not contain the path foo; `path:(foo OR bar)` means the path is foo Or search in the documentation of bar
* {: id="20201222215050-k83yd33"}`type`: Supports specifying the content block type through `type:foo`, available types please refer to ((20201222100222-q47d64s "Type filtering")). For example, `path:(h)` means searching in the title; type:(m OR c)` means searching in a mathematical formula block or code block
{: id="20201222215050-7jymwyb"}

## Specify time range
{: id="20201222215050-4ra1pgb"}

Support to specify the content block creation time through `time: [20200219 TO 20200825]`, for example, `time: [20200219163030 TO 20200825]` means that from February 19th, 2020 at 16:30:30 PM to August 25th, 2020 Search in the content block created at 00: 00: 00: 00.
{: id="20201222215050-6hwydlm"}

* {: id="20201222215050-5krj0s6"}`[` means greater than or equal to, `{` means greater than; `]` means less than or equal to, `}` means less than
* {: id="20201222215050-cqdq68o"}You can mix `[` and `{`, such as `time: [20200219 TO 20200825}`
{: id="20201222215050-qy5yanb"}


{: id="20201222100328-kzqg0mz" type="doc"}

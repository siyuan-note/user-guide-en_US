The template snippet is used to quickly insert the previously set text content at the cursor caret position and supports variables.
{: id="20210104091444-bu1zdhb" updated="20210302223800"}

## Template folder
{: id="20210104091444-ts3dff2"}

The documents in the folder named `templates` will be regarded as template documents. The template folder can be placed under the root of the notebook or under any level of folder.
{: id="20210104091444-qqyoi9t"}

The content block in the template document will not be searched by ((20200924101312-jj4e0v3 "Content block reference")), it is only used as template text.
{: id="20210104091444-e6fpmpg"}

## Writing a template
{: id="20210104091444-jy56z0p"}

The biggest difference between template snippets and ordinary documents is that variables can be written in the template, and these variables will be filled and rendered when the template is used. The template is implemented using [The Go Programming Language text template](https://golang.org/pkg/text/template/). If you know this, you can implement some program logic in it, such as comparison logic, Iterative logic, etc.
{: id="20210104091444-ycq0a40"}

It doesn't matter if you don't know too much, because using variables directly is the most common usage of templates. We have built in some variables and functions through the open source project [Sprig](https://github.com/Masterminds/sprig) to simplify the use of templates. The most commonly used one is to render the current time through `{{now | date "2006-01-02 15:04:05"}}`. For more usage, please refer to [Sprig Function Documentation](http://masterminds.github.io/sprig/).
{: id="20210104091444-c7gg3ak"}

There is a detail about the date and time formatting. #Note#: The formatting of the Go programming language is more "alternative". Instead of using `yyyy-MM-dd HH:mm:ss`, use `2006-01-02 15:04: 05` This fixed time format ([related discussions on Stack Overflow](https://stackoverflow.com/questions/20530327/origin-of-mon-jan-2-150405-mst-2006-in-golang)).
{: id="20210104091444-i618qd8"}

In addition to the built-in variables and functions of Sprig, the following variables and functions are also supported:
{: id="20210104091444-2wbdokx"}

* {: id="20210104091444-d5hpwdd"}`title`: Use this variable to insert the current document name. For example, if the template content is `# {{.title}}`, it will be inserted into the current document content with the first-level heading syntax after invoking
  {: id="20210131162138-93wovlc"}
* {: id="20210221131637-9xmclwp"}`id`：Use this variable to insert the current document id.
  {: id="20210221131637-hnlhxny"}
* {: id="20210121193829-wfzsf6m"}`sql`: Use this function to query the database, and the parameter is a SQL statement: `{{ sql "SELECT * FROM blocks LIMIT 7" }}`
  {: id="20210131162138-7ufhbho"}
{: id="20210104091444-mwbvc9m"}

## Invoke template
{: id="20210104091444-4re70bp"}

At the cursor caret position, inputting `{{` will trigger a template search, continue to input to filter by the template document name, find the template to be inserted and press Enter. #Note#: It does not support the call template of the broken notebook.
{: id="20210104091444-gfccosk"}

## An example
{: id="20210104091444-xz57sof"}

```plaintext
{{$before := (div (now.Sub (toDate "2006-01-02" "2020-02-19")).Hours 24)}}

{{$after := (div ((toDate "2006-01-02" "2048-02-19").Sub now).Hours 24)}}
Today is `{{now | date "2006-01-02"}}`.

* `{{$before}}` days have passed since `2020-02-19`
* There are `{{$after}}` days left from `2048-02-19`
```
{: id="20210104091444-cclnk66"}

`$before` and `$after` define two variables to record the number of days from the current date to 2020 and 2048, respectively.
{: id="20210104091444-rku6ohp"}

## Push to template bazaar
{: id="20210131162806-sk9tg4q"}

Please make sure that the root path of your template repository contains at least these two files before listing ([repo example](https://github.com/88250/November-Rain)):
{: id="20210131162806-wuttf37"}

* {: id="20210131162806-v0untr5"}template.json (please make sure the JSON format is correct)
  {: id="20210131162806-lyudtae"}
* {: id="20210131162806-vruviwi"}preview.png (please compress the image size within 128 KB)
  {: id="20210131162806-v86lig4"}
{: id="20210131162806-vsk0d2y"}

After confirmation, please [create a pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) to the [Community Bazaar](https://github.com/siyuan-note/bazaar) repository and modify the themes.json file in it. This file is the index file of all community template repositories, the format is:
{: id="20210131162806-j35q2kr"}

```json
{
   "repos": [
     "username/reponame@commithash"
   ]
}
```
{: id="20210131162806-bmhjqma"}

Among them, `commithash`, please fill in the Git commit hash of the latest released version on your template repository, please use the full hash value instead of the 7-digit short value.
{: id="20210131162806-0jwldvf"}

#### Update
{: id="20210131162806-pccuk3l"}

If the template you developed has an updated version, please remember:
{: id="20210131162806-0gkw7xr"}

* {: id="20210131162806-h1928oc"}Update the version field in your template.json
  {: id="20210131162806-eqoftxj"}
* {: id="20210131162806-4ldtdqg"}Create a Pull Request to the community bazaar
  {: id="20210131162806-kix2koc"}
{: id="20210131162806-aijnkan"}

{: id="20210131162142-6g1r08m"}


{: id="20201204184532-3qm9l8n" type="doc"}

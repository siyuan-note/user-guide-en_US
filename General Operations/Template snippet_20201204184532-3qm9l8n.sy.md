The template snippet is used to quickly insert the previously set text content at the cursor caret position and supports variables.

## Template folder

The documents in the folder named `templates` will be regarded as template documents. The template folder can be placed under the root of the notebook or under any level of folder.

The content block in the template document will not be searched by ((20200924101312-jj4e0v3 "Content block reference")), it is only used as template text.

## Writing a template

The biggest difference between template snippets and ordinary documents is that variables can be written in the template, and these variables will be filled and rendered when the template is used. The template is implemented using [The Go Programming Language text template](https://golang.org/pkg/text/template/). If you know this, you can implement some program logic in it, such as comparison logic, Iterative logic, etc.

It doesn't matter if you don't know too much, because using variables directly is the most common usage of templates. We have built in some variables and functions through the open source project [Sprig](https://github.com/Masterminds/sprig) to simplify the use of templates. The most commonly used one is to render the current time through `{{now | date "2006-01-02 15:04:05"}}`. For more usage, please refer to [Sprig Function Documentation](http://masterminds.github.io/sprig/).

There is a detail about the date and time formatting. #Note#: The formatting of the Go programming language is more "alternative". Instead of using `yyyy-MM-dd HH:mm:ss`, use `2006-01-02 15:04: 05` This fixed time format ([related discussions on Stack Overflow](https://stackoverflow.com/questions/20530327/origin-of-mon-jan-2-150405-mst-2006-in-golang)).

## Invoke template

At the cursor caret position, inputting `{{` will trigger a template search, continue to input to filter by the template document name, find the template to be inserted and press Enter. #Note#: It does not support the call template of the broken notebook.

## An example

```plaintext
{{$before := (div (now.Sub (toDate "2006-01-02" "2020-02-19")).Hours 24)}}

{{$after := (div ((toDate "2006-01-02" "2048-02-19").Sub now).Hours 24)}}
Today is `{{now | date "2006-01-02"}}`.

* `{{$before}}` days have passed since `2020-02-19`
* There are `{{$after}}` days left from `2048-02-19`
```

`$before` and `$after` define two variables to record the number of days from the current date to 2020 and 2048, respectively.

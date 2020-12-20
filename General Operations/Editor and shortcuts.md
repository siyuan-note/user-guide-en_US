## Vditor
{: id="20200924101004-lcuaajy"}

The editor component of SiYuan is called "Vditor", which is a browser-side Markdown editor and an open source project designed and developed by us. It can be found at [here](https://github.com/Vanessa219/vditor). Based on Vditor, we developed the editor mode currently used in SiYuan, and we will continue to improve it in the future to bring you a more modern Markdown editing experience.

## Application shortcuts

### General

| Name                                  | Shortcut key                                   |
| ------------------------------------- | ---------------------------------------------- |
| New document                          | <kbd>Ctrl N</kbd> / <kbd>⌘ N</kbd>           |
| Search                                | <kbd>Ctrl P</kbd> / <kbd>⌘ P</kbd>           |
| Close the current tab                 | <kbd>Ctrl W</kbd> / <kbd>⌘ W</kbd>           |
| File Tree Tab                         | <kbd>Alt 1</kbd> / <kbd>⌘ 1</kbd>            |
| Linkage outline tab                   | <kbd>Alt 2</kbd> / <kbd>⌘ 2</kbd>            |
| Bookmark tab                          | <kbd>Alt 3</kbd> / <kbd>⌘ 3</kbd>            |
| Tag tab                               | <kbd>Alt 4</kbd> / <kbd>⌘ 4</kbd>            |
| Linkage Backlink Tab                  | <kbd>Alt 7</kbd> / <kbd>⌘ 7</kbd>            |
| Linkage Diagram Tab                   | <kbd>Alt 8</kbd> / <kbd>⌘ 8</kbd>            |
| Global Relationship Diagram Tab       | <kbd>Alt 9</kbd> / <kbd>⌘ 9</kbd>            |
| Actual Size                           | <kbd>Ctrl 0</kbd> / <kbd>⌘ 0</kbd>           |
| Zoom In                               | <kbd>Ctrl =</kbd> / <kbd>⌘ =</kbd>           |
| Zoom Out                              | <kbd>Ctrl -</kbd> / <kbd>⌘ -</kbd>           |
| Paste block embed/Paste as plain text | <kbd>Ctrl Shift V</kbd> / <kbd>⌘ ⇧ V</kbd> |

## Editor shortcuts

### General

| Name                                     | Shortcut key                                                  | Remarks      |
| ---------------------------------------- | ------------------------------------------------------------- | ------------ |
| Content block quote                      | <kbd>((</kbd> / <kbd>[[</kbd> / <kbd>((</kbd> / <kbd>[[</kbd> | see below    |
| Emoticons                                | <kbd>:</kbd> / <kbd>Alt E</kbd> / <kbd>⌥ E</kbd>            |              |
| Title                                    | <kbd>Ctrl H</kbd> / <kbd>⌘ H</kbd>                          | see below    |
| Bold                                     | <kbd>Ctrl B</kbd> / <kbd>⌘ B</kbd>                          |              |
| Italic                                   | <kbd>Ctrl I</kbd> / <kbd>⌘ I</kbd>                          |              |
| Mark                                     | <kbd>Ctrl Shift M</kbd> / <kbd>⌘ ⇧ M</kbd>                |              |
| Tag                                      | <kbd>Ctrl Shift T</kbd> / <kbd>⌘ ⇧ T</kbd>                |              |
| Strikethrough                            | <kbd>Ctrl D</kbd> / <kbd>⌘ D</kbd>                          |              |
| Link                                     | <kbd>Ctrl K</kbd> / <kbd>⌘ K</kbd>                          | see below    |
| Unordered List                           | <kbd>Ctrl L</kbd> / <kbd>⌘ L</kbd>                          | see below    |
| Ordered list                             | <kbd>Ctrl O</kbd> / <kbd>⌘ O</kbd>                          | see below    |
| Task list                                | <kbd>Ctrl J</kbd> / <kbd>⌘ J</kbd>                          | see below    |
| Quote                                    | <kbd>Ctrl ;</kbd> / <kbd>⌘ ;</kbd>                          | see below    |
| Dividing line                            | <kbd>Ctrl Shift H </kbd> / <kbd>⌘ ⇧ H</kbd>               |              |
| Code block                               | <kbd>Ctrl U</kbd> / <kbd>⌘ U</kbd>                          | see below    |
| Code                                     | <kbd>Ctrl G</kbd> / <kbd>⌘ G</kbd>                          |              |
| Insert an empty block before the element | <kbd>Ctrl Shift B</kbd> / <kbd>⌘ ⇧ B</kbd>                |              |
| Insert an empty block after the element  | <kbd>Ctrl Shift E</kbd> / <kbd>⌘ ⇧ E</kbd>                |              |
| Table                                    | <kbd>Ctrl M</kbd> / <kbd>⌘ M</kbd>                          | see below    |
| Undo                                     | <kbd>Ctrl Z</kbd> / <kbd>⌘ Z</kbd>                          |              |
| Redo                                     | <kbd>Ctrl Y</kbd> / <kbd>⌘ Y</kbd>                          |              |
| Preview                                  | <kbd>Ctrl E</kbd> / <kbd>⌘ E</kbd>                          |              |
| Full screen                              | <kbd>Ctrl'</kbd> / <kbd>⌘'</kbd>                            |              |
| Move block element up                    | <kbd>Ctrl Shift U</kbd> / <kbd>⌘ ⇧ U</kbd>                | wysiwyg mode |
| Move block element down                  | <kbd>Ctrl Shift D</kbd> / <kbd>⌘ ⇧ D</kbd>                | wysiwyg mode |
| Remove current element                   | <kbd>Ctrl Shift X</kbd> / <kbd>⌘ ⇧ X</kbd>                | wysiwyg mode |
| Save                                     | <kbd>Ctrl S</kbd> / <kbd>⌘ S</kbd>                          |              |
| Wrong input                              | <kbd>Backspace</kbd>                                          |              |

### Content block reference <kbd>((</kbd> / <kbd>[[</kbd>

| Name                            | Shortcut key                                   | Remarks                                                             |
| ------------------------------- | ---------------------------------------------- | ------------------------------------------------------------------- |
| Select                          | <kbd>↑</kbd> / <kbd>↓</kbd>                |                                                                     |
| Completion                      | <kbd>Enter</kbd>                               |                                                                     |
| Jump out of content block quote | <kbd>Tab</kbd>                                 | Only useful in text content                                         |
| Copy content block ID           | <kbd>Ctrl Shift C</kbd> / <kbd>⌘ ⇧ X</kbd> |                                                                     |
| Paste content block reference   | <kbd>Ctrl V</kbd> / <kbd>⌘ v</kbd>           | Only available when the content block ID is copied in the clipboard |
| Past content block embed        | <kbd>Ctrl Shift V</kbd> / <kbd>⌘ ⇧ v</kbd> | Only available when the content block ID is copied in the clipboard |

### Heading <kbd>Ctrl H</kbd> / <kbd>⌘ H</kbd>

| Name        | Shortcut key                                                     |
| ----------- | ---------------------------------------------------------------- |
| Get bigger  | <kbd>Ctrl +</kbd> / <kbd>⌘ +</kbd>                             |
| Get smaller | <kbd>Ctrl -</kbd> / <kbd>⌘ -</kbd>                             |
| H1-H6       | <kbd>Ctrl Alt 1/2/3/4/5/6</kbd> / <kbd>⌘ ⌥ 1/2/3/4/5/6</kbd> |
| Pop-up menu | <kbd>Ctrl H</kbd> / <kbd>⌘ H</kbd>                             |

### Link <kbd>Ctrl K</kbd> / <kbd>⌘ K</kbd>

| Name                                 | Shortcut key                                |
| ------------------------------------ | ------------------------------------------- |
| Switch between input box and element | <kbd>Alt Enter</kbd> / <kbd>⌥ Enter</kbd> |
| Switch between input boxes           | <kbd>Tab</kbd>                              |

### List <kbd>Ctrl L/O/J</kbd> / <kbd>⌘ L/O/J</kbd>

| Name                          | Shortcut key                                   | Remarks                             |
| ----------------------------- | ---------------------------------------------- | ----------------------------------- |
| Indent 1                      | <kbd>Tab</kbd>                                 | The cursor must be at the beginning |
| Indent 2                      | <kbd>Ctrl Shift I</kbd> / <kbd>⌘ ⇧ I</kbd> |                                     |
| Reverse Indent 1              | <kbd>Shift Tab</kbd> / <kbd>⇧ Tab</kbd>      | The cursor must be at the beginning |
| Reverse indent 2              | <kbd>Enter</kbd>                               | Empty list item                     |
| Reverse indent 3              | <kbd>Ctrl Shift O</kbd> / <kbd>⌘ ⇧ O</kbd> |                                     |
| Switch between Done and To Do | <kbd>Ctrl Shift J</kbd> / <kbd>⌘ ⇧ J</kbd> | Task List                           |

### Quote <kbd>Ctrl ;</kbd> / <kbd>⌘ ;</kbd>

| Name                                             | Shortcut key                                         | Remarks                                      |
| ------------------------------------------------ | ---------------------------------------------------- | -------------------------------------------- |
| Insert an empty block before the top-level quote | <kbd>Ctrl Alt Enter</kbd> / <kbd>⌘ ⌥ Enter</kbd> | wysiwyg mode                                 |
| Insert an empty block after the top-level quote  | <kbd>Alt Enter</kbd> / <kbd>⌥ Enter</kbd>          | wysiwyg mode                                 |
| Insert block element 1                           | <kbd>></kbd>                                         | Insert reference in inline element           |
| Insert block element 2                           | <kbd>Ctrl Shift :</kbd> / <kbd>⌘ ⇧ :</kbd>       | Block element becomes reference wysiwyg mode |
| Switch between quotes and block elements         | <kbd>Ctrl ;</kbd> / <kbd>⌘ ;</kbd>                 |                                              |

### Code block <kbd>Ctrl U</kbd> / <kbd>⌘ U</kbd>

| Name                                    | Shortcut key                                |
| --------------------------------------- | ------------------------------------------- |
| Switch between input box and code block | <kbd>Alt Enter</kbd> / <kbd>⌥ Enter</kbd> |
| Hide editing interface                  | <kbd>Escape</kbd>                           |
| Select all codes                        | <kbd>Ctrl A</kbd> / <kbd>⌘ A</kbd>        |

### Table <kbd>Ctrl M</kbd> / <kbd>⌘ M</kbd>

| Name                                         | Shortcut key                                                        |
| -------------------------------------------- | ------------------------------------------------------------------- |
| Insert a new line under the current line     | <kbd>Ctrl =</kbd> / <kbd>⌘ =</kbd>                                |
| Delete line                                  | <kbd>Ctrl -</kbd> / <kbd>⌘ -</kbd>                                |
| Insert a new column after the current column | <kbd>Ctrl Shift +</kbd> / <kbd>⌘ ⇧ +</kbd>                      |
| Delete column                                | <kbd>Ctrl Shift -</kbd> / <kbd>⌘ ⇧ -</kbd>                      |
| Left aligned                                 | <kbd>Ctrl Shift L</kbd> / <kbd>⌘ ⇧ L</kbd>                      |
| Center alignment                             | <kbd>Ctrl Shift C</kbd> / <kbd>⌘ ⇧ C</kbd>                      |
| Right aligned                                | <kbd>Ctrl Shift R</kbd> / <kbd>⌘ ⇧ R</kbd>                      |
| Move the cursor to the input box             | <kbd>Alt Enter</kbd> / <kbd>⌥ Enter</kbd>                         |
| Switch between input boxes                   | <kbd>Tab</kbd>                                                      |
| Move the cursor to the previous element      | <kbd>Shift Tab</kbd> / <kbd>⇧ Tab</kbd><br /><kbd>Backspace</kbd> |
| Move the cursor to the next element          | <kbd>Tab</kbd>                                                      |


{: id="20200924100950-9op5xi1" type="doc"}

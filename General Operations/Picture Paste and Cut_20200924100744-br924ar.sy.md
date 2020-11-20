## Insert picture

In the editor, you can directly paste the copied picture from the system clipboard, and the picture file will be copied to the assets folder at the same level as the current document. You can also insert pictures by dragging and dropping picture files into the editor.

If you need to specify the image title, you can use the standard Markdown syntax: `![alt](assets/image "title")`, when the image exists independently in a content block (that is, there is no content before and after the image, the image has an exclusive section), The picture will be automatically centered, and `title` will be rendered below the picture as the picture title.

## Clips

Through the "Clip" function, we can paste other rich text content (such as Web pages, Word, Excel, etc.) into the editor, and Siyuan Note will automatically convert it into standard Markdown text.

The specific usage is to manually select the content of the webpage, for example, select the text part of the webpage article to copy, and then paste it in Siyuan. Do not select all pages to copy, otherwise you may not be able to paste any content.

If you check Settings - Assets - Auto fetch remote image to local, the clip will download the picture files on the Web page to assets folder and replace the picture address in the content with the local assets path.

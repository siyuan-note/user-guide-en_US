## Why are there many things like `{: id="20201024020406"}` inserted into my Markdown?
{: id="20201224120448-p7kmg64"}

These contents are used to store the content block identification and follow the kramdown syntax. For details, please see ((20200924095851-u5jmzr3 "{{.text}}")). If you need the standard Markdown (GFM/CommonMark) format, please use the ((20201229152405-vlhitro "Export")) function.
{: id="20201224120448-y0qff0p"}

## Is there any #Note# for deleting files/folders?
{: id="20201224120448-ygu8bzx"}

For local notebooks (not WebDAV), all operations will be managed through ((20201002092058-85k2cws "Local Repository"))  for version management. If you need to restore accidentally deleted data, you can perform operations through the Git client.
{: id="20201224120448-1wyj9f7"}

## How can I just wrap and not start a new paragraph?
{: id="20210106192438-on2fb5k"}

Use <kbd>Shift+Enter</kbd>.
{: id="20210106192504-pgryxb1"}

## How to insert a picture?
{: id="20201224120448-z2gba1k"}

You can insert a picture through the Markdown picture syntax `![optional picture description text](picture file path)`. You can also directly drag the image file into the editor to insert it, and the image file will be automatically copied to the assets folder at the same level of the document. For more details, please refer to ((20201210194734-v2rmiaq "{{.text}}")).
{: id="20201224120448-c445h02"}

## How to insert video and audio?
{: id="20201224120448-amyh0z2"}

You can use Markdown link syntax `[anchor text](media resource path)` to insert video, audio and other files. SiYuan will automatically load the player for rendering according to the file suffix.
{: id="20201224120448-3cfetom"}

## How to adjust table rows and columns?
{: id="20201224120448-eoju3re"}

First position the cursor on the cell that needs to be adjusted, and then right-click to see the table adjustment menu.
{: id="20201224120448-yti3dvr"}

## Where are the configuration files stored?
{: id="20201224120448-0f3b9ys"}

The default configuration folder is located in the user's home directory `~/.siyuan/`. If there is a configuration folder in the installation directory, the installation directory will be used first. You can also specify the configuration folder path by ((20200924100717-yzwzn64 "startup parameter")).
{: id="20201224120448-hexn2qn"}

## Do you plan to support plugins?
{: id="20201224120448-yq5ziln"}

Siyuan Note supports ((20201004194026-s8h2cog "Use on browser")),  which can be extended by browser plug-ins. We are looking forward to other developers writing browser plug-ins for SiYuan. With the gradual provision of ((20201227201751-gv0fpx2 "Kernel API")) , we will introduce a plug-in mechanism in the future.
{: id="20201224120448-hn7uqj1"}

## Why is pit.exe reported as a Trojan virus?
{: id="20201228141919-1rv31v8"}

The pit.exe located in the resources folder of the installation directory is the SiYuan update program, which is responsible for pulling the update package from and decompressing the update. As for why the Trojan horse virus was reported, we don't know. We have opened [pit source](https://github.com/siyuan-note/pit). Developers are welcome to contribute, thank you.
{: id="20201228141919-vgwyjy9"}

## Why does WebDAV report error 503 after connecting?
{: id="20201231103013-nxyusb6"}

This error is returned by the WebDAV provider interface. Generally, it is because SiYuan calls the interface too frequently, which causes the provider to limit the interface service. When connecting to WebDAV, please specify the specific folder path in the service address column, such as: `https://dav.jianguoyun.com/dav/My Notes Folder/`, please do not use `https://dav.jianguoyun.com/dav/` directly.
{: id="20201231103013-qoubp11"}

## Do I need to pay for it?
{: id="20201224120448-0rqote3"}

Before the release of v1.0.0, all functions are completely free for **personal** use. After the release of v1.0.0, [Advanced Features](https://github.com/siyuan-note/siyuan/projects/1) requires [annual subscription](https://ld246.com/subscribe/siyuan), price is $64/year。
{: id="20201224120448-20hmjfc"}

If you need to create an account and pay for a subscription in a non-Mainland China area, please send an email to us (`support@b3log.org`), we will manually create an account and create a PayPal email payment order for you, thank you.
{: id="20201224120448-8uydzg3"}


{: id="20200923234731-h3zkwm2" type="doc"}

## Why are there many things like `{: id="20201024020406"}` inserted into my Markdown?

These contents are used to store the content block identification and follow the kramdown syntax. For details, please see ((20200924095851-u5jmzr3 "{{.text}}")).

## Is there any #Note# for deleting files/folders?

For local notebooks (not WebDAV), all operations will be managed through ((20201002092058-85k2cws "Local Repository"))  for version management. If you need to restore accidentally deleted data, you can perform operations through the Git client.

## How to insert a picture?

You can insert a picture through the Markdown picture syntax `![optional picture description text](picture file path)`. You can also directly drag the image file into the editor to insert it, and the image file will be automatically copied to the assets folder at the same level of the document. For more details, please refer to ((20201210194734-v2rmiaq "{{.text}}")).

## How to insert video and audio?

You can use Markdown link syntax `[anchor text](media resource path)` to insert video, audio and other files. SiYuan will automatically load the player for rendering according to the file suffix.

## How to adjust table rows and columns?

First position the cursor on the cell that needs to be adjusted, and then right-click to see the table adjustment menu.

## Where are the configuration files stored?

The default configuration folder is located in the user's home directory `~/.siyuan/`. If there is a configuration folder in the installation directory, the installation directory will be used first. You can also specify the configuration folder path by ((20200924100717-yzwzn64 "startup parameter")).

If you need to share the configuration on multiple devices, you can synchronize the configuration folder through a third-party network disk service.

## Do you plan to support plugins?

SiYuan supports ((20201004194026-s8h2cog "Use on browser")), the functions can be extended through browser plug-ins. We are looking forward to other developers writing browser plug-ins for SiYuan.

In the later stage, we plan to introduce "View" to structure and render data in various formats. #TODO#

## Do I need to pay for it?

Before the release of v1.0.0, all functions are completely free for **personal** use. After the release of v1.0.0, [Advanced Features](https://github.com/siyuan-note/siyuan/projects/1) requires a paid subscription.

The first 512 early supporters can buy out personal lifetime subscriptions through [one-time payment of $20](https://ld246.com/sponsor?price=128&product=siyuan) (you must log in to the LianDi community to make payments). If you need to issue an invoice, please contact us by email [support@b3log.org](mailto:support@b3log.org) after the payment is completed.

LianDi community does not support registration in non-Mainland China regions. Please send an email to us and we will manually create an account for you. If you want to pay but don't have a China Alipay account, please email us, we will create a PayPal email payment order for you, thank you.


{: id="20200923234731-h3zkwm2" type="doc"}

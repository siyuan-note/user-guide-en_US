## How does SiYuan store data?
{: id="20210428222532-nfvnq4d" updated="20210428222834"}

The data is saved in the workspace folder (the default is in the user's home directory Documents/SiYuan, which can be modified in `Settings - About`), in the workspace data folder:
{: id="20210428222603-g1752n7" updated="20210428222615"}

* {: id="20210428222603-gxgx3vi"}`assets` are used to save all inserted asset files
  {: id="20210428222603-0goch51" updated="20210503100004"}
* {: id="20210428222603-vtr89xq"}`templates` are used to save ((20201204184532-3qm9l8n "Template snippet"))
  {: id="20210428222603-criebuv" updated="20210428222658"}
* {: id="20210428222603-456vgdh"}`widgets` are used to save widgets #TODO#
  {: id="20210428222603-m3djncm" updated="20210428222701"}
* {: id="20210428222603-27so3jy"}The rest of the folders are the notebook folders created by the user
  {: id="20210428222603-pwyr56t"}

  * {: id="20210428222603-zjesktk"}Files with the suffix of `.sy` in the notebook folder are used to save the document data, and the data format is JSON
    {: id="20210428222603-9gah47n"}
  {: id="20210428222603-wntbxgj"}
{: id="20210428222603-moih9fe"}

## Why is it not displayed on the doc tree after I put the Markdown file in the notebook folder?
{: id="20210120161137-0ggx9sa"}

Please use the ((20201229152405-ivntzua "Import")) function.
{: id="20210120161137-aqdjef7"}

## Is there any #Note# for deleting files/folders?
{: id="20201224120448-ygu8bzx"}

For local notebooks, all operations will be managed through ((20201002092058-85k2cws "Auto Backup")), support ((20210104091559-kgrtuyh "rollback")).
{: id="20210323173132-ob0oz44" updated="20210403163024"}

## How can I just wrap and not start a new paragraph?
{: id="20210106192438-on2fb5k"}

Please use <kbd>Shift+Enter</kbd>.
{: id="20210106192504-pgryxb1" updated="20210417112701"}

## How to adjust table rows and columns?
{: id="20201224120448-eoju3re"}

First position the cursor on the cell that needs to be adjusted, and then right-click to see the table adjustment menu.
{: id="20201224120448-yti3dvr"}

## How to turn pages in a slide show?
{: id="20210204162757-ei505a6"}

In document typesetting, you need to use `---` to separate the content of each page. For specific usage, please refer to ((20210203182642-odiolr2 "Slides Presentation")).
{: id="20210204162757-0al9jtb"}

## How to delete unnecessary history records to reduce space usage and improve performance?
{: id="20210226101133-php3e1u" updated="20210402112548"}

Open the notebook `.siyuan/backup/` folder on the file system and delete unnecessary backup history.
{: id="20210315224644-d8kjhtk" updated="20210402001829"}

## How to delete cloud asset files that are no longer needed?
{: id="20210226101134-hvw08er" updated="20210226101142"}

#TODO#
{: id="20210226101144-fknnoaz" updated="20210301220415"}

## Do you plan to support plugins?
{: id="20201224120448-yq5ziln"}

SiYuan supports ((20201004194026-s8h2cog "Use on browser")),  which can be extended by browser plug-ins. We are looking forward to other developers writing browser plug-ins for SiYuan. With the gradual provision of ((20201227201751-gv0fpx2 "Kernel API")) , we will introduce a plug-in mechanism in the future.
{: id="20201224120448-hn7uqj1"}

## Do I need to pay for it?
{: id="20201224120448-0rqote3"}

Basic functions are completely free to use, [advanced features](https://b3log.org/siyuan/advanced_features.html) requires [annual subscription](https://b3log.org/siyuan/pricing.html), price is $64/year。
{: id="20201224120448-20hmjfc"}

If you need to create an account and pay for a subscription in a non-Mainland China area, please send an email to us (`845765@qq.com`), we will manually create an account and create a PayPal email payment order for you, thank you.
{: id="20201224120448-8uydzg3"}


{: id="20200923234731-h3zkwm2" type="doc"}

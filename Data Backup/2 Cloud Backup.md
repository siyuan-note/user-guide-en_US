## Overview
{: id="20210104091603-1dzjinv" updated="20210522111625"}

The cloud backup function is the [Advanced Features](https://b3log.org/siyuan/en/advanced_features.html) of SiYuan. Backup is divided into two directions: upload and download:
{: id="20210104091603-5xeizyz" updated="20210522112437"}

* {: id="20210315224035-jrzp7fe"}When uploading, the cloud data will be overwritten with local data
  {: id="20210315224035-ne26vk7"}
* {: id="20210315224035-zzwk5bo"}When downloading, the local data will be overwritten with cloud data. When a conflict occurs, the overwritten local data will be automatically backed up to the `.siyuan/backup/` folder, and the folder will not be uploaded to the cloud when the upload is executed, which means that the backup only exists on the current local end
  {: id="20210315224035-xbcd4ua" updated="20210522111644"}
{: id="20210315224035-m0aonr0"}

## Cloud Space size
{: id="20210104091603-is1ds2d" updated="20210226100300"}

* {: id="20210104091603-qm7tv9i"}The maximum storage space of all notebooks under the same user is `8G`
  {: id="20210204192136-u0azal3" updated="20210315224120"}
* {: id="20210104091603-4xkbxbf"}After the paid subscription expires, the data will be retained for 1 month. If there is no renewal during this period, the data will be completely deleted after 1 month
  {: id="20210204192136-4f2lrqu"}
{: id="20210104091603-x70187x"}

### First download on a new device
{: id="20210327182207-gdtg2a9"}

On the new device, click <kbd>Settings</kbd> - <kbd>Backup</kbd> - <kbd>Cloud Workspace</kbd> - <kbd>Download</kbd> from the cloud.
{: id="20210327182207-teue4qk" updated="20210522112120"}

## #Note# Matters
{: id="20210327182207-19u1e23" updated="20210522111721"}

Please pay attention to confirm the direction (upload or download), because the target side data will be overwritten.
{: id="20210331084559-zzbw0lp" updated="20210522111753"}


{: id="20201002092228-8hmuss5" type="doc"}

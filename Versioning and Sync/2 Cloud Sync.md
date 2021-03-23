## Data synchronization
{: id="20210104091603-1dzjinv" updated="20210302223919"}

The data synchronization function is the [Advanced Features](https://b3log.org/siyuan/en/advanced_features.html) of SiYuan. Synchronization is divided into two directions: upload and download:
{: id="20210104091603-5xeizyz" updated="20210315224009"}

* {: id="20210315224035-jrzp7fe"}When uploading, the cloud data will be overwritten with local data
  {: id="20210315224035-ne26vk7"}
* {: id="20210315224035-zzwk5bo"}When downloading, the local data will be overwritten with cloud data. When a conflict occurs, the overwritten local data will be automatically backed up to the `.siyuan/backup/` folder of the notebook, and the folder will not be uploaded to the cloud when the upload is executed, which means that the backup only exists on the current local end
  {: id="20210315224035-xbcd4ua" updated="20210323173304"}
{: id="20210315224035-m0aonr0"}

## Cloud Space size
{: id="20210104091603-is1ds2d" updated="20210226100300"}

* {: id="20210104091603-qm7tv9i"}The maximum storage space of all notebooks under the same user is `8G`
  {: id="20210204192136-u0azal3" updated="20210315224120"}
* {: id="20210104091603-4xkbxbf"}After the paid subscription expires, the data will be retained for 1 month. If there is no renewal during this period, the data will be completely deleted after 1 month
  {: id="20210204192136-4f2lrqu"}
{: id="20210104091603-x70187x"}

## synchronization use process
{: id="20210104091603-p14ch6a" updated="20210315224140"}

1. {: id="20210226100333-rd6bfkj"}Select the notebook to be synchronized in the file tree, select settings in the right-click drop-down menu, and open the synchronization option in the settings interface
   {: id="20210226100333-x88ifnn"}
2. {: id="20210226100333-k08ocrr"}Click the sync button and choose whether to upload or download
   {: id="20210226100333-mh4hgkr" updated="20210226100456"}
3. {: id="20210226100333-d2ocsog"}On the new device, download the data from the cloud by Setting - Sync - Cloud notebook - Clone to local. The cloning operation is only required when data is first acquired on a new device. You can also create a notebook with the same name as the cloud, and then pull the cloud data to the local through synchronization - download
   {: id="20210226100333-btjrtqo" updated="20210315224319"}
{: id="20210226100333-yth7w6h" updated="20210315224235"}

#Note#: Please pay attention to confirm the direction (upload or download), because the target side data will be overwritten.
{: id="20210315224329-l3o6006" updated="20210315224515"}


{: id="20201002092228-8hmuss5" type="doc"}

## Data synchronization
{: id="20210104091603-1dzjinv" updated="20210302223919"}

The data synchronization function is the [Advanced Features](https://b3log.org/siyuan/en/advanced_features.html) of SiYuan. Synchronization is divided into Git synchronization and asset files synchronization, which can significantly improve performance and reduce space usage.
{: id="20210104091603-5xeizyz" updated="20210226100002"}

* {: id="20210226100018-izpvokp"}Git synchronization is only used to synchronize .md files, and non-.md files are automatically ignored through .gitignore synchronization
  {: id="20210226100018-lox7l34"}
* {: id="20210226100018-8nkvlmv"}The asset files referenced in the documents under the assets folder will be synchronized by uploading and downloading
  {: id="20210226100018-08if35l" updated="20210226100039"}
{: id="20210226100018-5rklteh" updated="20210301211743"}

#Note#:
{: id="20210104091603-pfg40jy"}

* {: id="20210301211837-ynwu2u0"}Each time you synchronize, .gitignore will be reset and the ignore rules will be written
  {: id="20210301211837-0uezf5a"}
* {: id="20210301211837-ndq7kev"}Because assets are not included in Git management, there will be no version history support, please confirm clearly when deleting resource files
  {: id="20210301211837-yu2mf7g"}
* {: id="20210301211837-nksud8y"}If you use other Git repository services, please turn off automatic commit in the settings
  {: id="20210301211837-6k4l71t" updated="20210301211907"}
* {: id="20210301211837-qku2a3n"}Only the asset files that have been referenced will be synchronized, and the folder reference method is not supported
  {: id="20210301211837-g8dzo9i" updated="20210301211912"}
{: id="20210301211837-nsils1w"}

## Cloud Space size
{: id="20210104091603-is1ds2d" updated="20210226100300"}

* {: id="20210104091603-qm7tv9i"}The maximum storage space of all notebooks under the same user is `4G` (including version history)
  {: id="20210204192136-u0azal3"}
* {: id="20210104091603-4xkbxbf"}After the paid subscription expires, the data will be retained for 1 month. If there is no renewal during this period, the data will be completely deleted after 1 month
  {: id="20210204192136-4f2lrqu"}
{: id="20210104091603-x70187x"}

## Synchronous use process
{: id="20210104091603-p14ch6a"}

1. {: id="20210226100333-rd6bfkj"}Select the notebook to be synchronized in the file tree, select settings in the right-click drop-down menu, and open the synchronization option in the settings interface
   {: id="20210226100333-x88ifnn"}
2. {: id="20210226100333-k08ocrr"}Click the sync button on the current device, the document data will be pushed to the cloud through the Git SSH protocol, and the cloud data will also be pulled to the local; the referenced assets files will be uploaded to the cloud via HTTPS protocol
   {: id="20210226100333-mh4hgkr" updated="20210226100456"}
3. {: id="20210226100333-d2ocsog"}On the new device, download the data from the cloud by Settings - Sync - Cloud notebook -Clone to Local. Only when you need to clone the data for the first time on the new device, you can directly click the sync button to sync later.
   {: id="20210226100333-btjrtqo" updated="20210226100548"}
4. {: id="20210226100343-uu01tk4"}After synchronization, if there is newly pulled data, the interface will be refreshed as a whole. If there is a conflict, it will be displayed in the ((20201210002930-7cvn3j6 "Git conflict markers"))
   {: id="20210226100343-oeg01ir" updated="20210226100621"}
{: id="20210226100333-yth7w6h" updated="20210226100615"}

{: id="20210204192136-gshtv2c"}


{: id="20201002092228-8hmuss5" type="doc"}

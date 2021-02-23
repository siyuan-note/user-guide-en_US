This service is the [Advanced Features](https://b3log.org/siyuan/en/advanced_features.html) of SiYuan, and you need to pay to use it.
{: id="20210223100728-zw90upp" updated="20210223100904"}

By default ((20210223100527-12ki6gl "asset files will not be included in versioning")), so asset files will not be synchronized during synchronization. For asset files, we recommend saving them through SiYuan Cloud Asset Storage Service, because this can:
{: id="20210223100811-3bejxgg" updated="20210223101637"}

* {: id="20210223100811-mygkmc8"}By separating .md documents and asset files (documents are synchronized by Git, asset files are stored in the cloud), the synchronization performance can be greatly improved
  {: id="20210223100811-5z5kf8f" updated="20210223101345"}
* {: id="20210223100811-clupm7p"}Asset files usually do not require versioning, and a separate storage service can effectively reduce storage space occupation
  {: id="20210223100811-l2zu6ig" updated="20210223101458"}
* {: id="20210223100811-r8olasx"}Asset files are stored in the cloud, which is more convenient when sharing documents to other websites or applications
  {: id="20210223100811-cden480" updated="20210223101429"}
{: id="20210223100811-wmsofvn"}

## Steps for usage
{: id="20210223100811-7jfklk4"}

* {: id="20210223100811-nkherbn"}Turn on uploading to the cloud while inserting asset files in the notebook settings. This option is turned on by default #TODO#
  {: id="20210223100811-g4h2i6q"}
* {: id="20210223100811-d4cgyzp"}In the editor, you can right-click the asset and select upload to cloud storage
  {: id="20210223100811-sjsyumu" updated="20210223101415"}
* {: id="20210223100811-o2ckyq4"}In the file tree, you can right-click the assets folder and select upload to cloud storage
  {: id="20210223100811-ccw6cwd"}
* {: id="20210223100811-kpolt3l"}Right-click on the editor tab to switch to use local assets path or use cloud path
  {: id="20210223100811-eznkon1" updated="20210223101544"}
* {: id="20210223100811-0it4ljo"}View and delete cloud asset files in Settings - Assets #TODO#
  {: id="20210223100811-5pecmnu" updated="20210223101420"}
{: id="20210223100811-3xaqkrn"}

## Security Instructions
{: id="20210223100811-vx02onm"}

SiYuan Cloud Asset Storage Service does not have any security measures, as long as the asset file URL can be obtained, the asset file can be accessed. The asset file URL is a random value of a timestamp + 7-digit alphanumeric combination, and the cloud storage has frequency access restrictions, so the possibility of brute force cracking is low.
{: id="20210223100811-olchtch" updated="20210223101646"}


{: id="20210223100728-0am7tx9" type="doc"}

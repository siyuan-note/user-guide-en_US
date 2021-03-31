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

## Synchronous use process
{: id="20210327182207-qyok4z8"}

You need to select the notebook to be synchronized in the file tree, select settings in the right-click drop-down menu, and turn on the synchronization option in the settings interface, so that the notebook will be included in the synchronization.
{: id="20210327182207-rtv8tca"}

Synchronization is divided into two modes, manual synchronization mode (default) and automatic synchronization mode.
{: id="20210327182207-fqlv61e"}

* {: id="20210327182207-i7dq2mt"}Manual synchronization: click the synchronization button, select upload or download
  {: id="20210327182207-o4nywq3"}
* {: id="20210327182207-i42jwtb"}Auto sync: Turn on the Settings - Sync - Auto sync switch. Automatic synchronization scans every 30 seconds
  {: id="20210327182207-7yoko57" updated="20210327182340"}

  * {: id="20210327182207-4kgt21u"}If new changes are found in the cloud notebook, it will be automatically downloaded
    {: id="20210327182207-50dq4tw"}
  * {: id="20210327182207-zkrgex8"}If new changes are found in the local notebook, it will be uploaded automatically
    {: id="20210327182207-9weuk8c"}
  {: id="20210327182207-3v2ustd"}
{: id="20210327182207-hqlqffy"}

### First download on a new device
{: id="20210327182207-gdtg2a9"}

On the new device, click Settings - Sync - Cloud Notebook - Download from the cloud.
{: id="20210327182207-teue4qk" updated="20210327182354"}

## Sync #Note# Matters
{: id="20210327182207-19u1e23" updated="20210331084605"}

* {: id="20210331084556-3lsfyfa"}Mobile APP sync does not support notebook names containing spaces
  {: id="20210331084556-7prqm10" updated="20210331084611"}
* {: id="20210331084559-ezgbr97"}Please pay attention to confirm the direction (upload or download) when using manual synchronization mode, because the target side data will be overwritten
  {: id="20210331084559-zzbw0lp" updated="20210331084602"}
* {: id="20210331084602-7borrsq"}When using automatic synchronization mode, please ensure that the time of each device is the same
  {: id="20210331084602-1ch6fov" updated="20210331084602"}
{: id="20210327182207-z6xrnt7" updated="20210331084556"}


{: id="20201002092228-8hmuss5" type="doc"}

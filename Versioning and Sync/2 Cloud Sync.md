## Repository synchronization
{: id="20210104091603-1dzjinv"}

The synchronization function is the [Advanced Features](https://b3log.org/siyuan/en/advanced_features.html) of SiYuan, and you need to pay to use it. After clicking the sync button on the interface, SiYuan will synchronize data through `git pull` and `git push`.
{: id="20210104091603-5xeizyz" updated="20210223100858"}

#Note#: WebDAV notebooks will not be synchronized because the WebDAV server itself is already in the cloud.
{: id="20210104091603-pfg40jy"}

We chose to use Git for version management not only because of the power and stability of Git, but also because it is open. So using our server cloud repository is not the only option. You can add other remote repositories (such as GitHub repositories) through the `git remote add` command, and then you can synchronize with these remote repositories via Git. Please refer to the operation details :
{: id="20210104091603-6fyox44" updated="20210223085923"}

* {: id="20210104091603-ate8icx"}((20201213120253-hhtskws "{{.text}}"))
  {: id="20210204192136-kg00w0v"}
* {: id="20210104091603-zrgz521"}((20201213120253-ulbi3zh "{{.text}}"))
  {: id="20210204192136-8y051pj"}
{: id="20210104091603-twlfyt0"}

## Cloud Repository
{: id="20210104091603-is1ds2d"}

The cloud repository of our server is located at `git@siyuan.b3logfile.com:/siyuan/{uid}/{notebook}.git`, and the automatically generated SSH key pair is used for identity authentication. If you encounter problems with identity authentication when using the synchronization function, please ((20200923234102-ysbri6o "Contact us for feedback")).
{: id="20210104091603-xkkiv92"}

* {: id="20210104091603-qm7tv9i"}The maximum storage space of all notebooks under the same user is `4G` (including version history)
  {: id="20210204192136-u0azal3"}
* {: id="20210104091603-4xkbxbf"}After the paid subscription expires, the data will be retained for 1 month. If there is no renewal during this period, the data will be completely deleted after 1 month
  {: id="20210204192136-4f2lrqu"}
{: id="20210104091603-x70187x"}

## Synchronous use process
{: id="20210104091603-p14ch6a"}

1. {: id="20210104091603-10njnef"}Click the sync button on the current device (if there is no repository in the cloud at this time, a cloud repository will be created), the data will be pushed to the cloud through the Git SSH protocol, and the cloud data will also be pulled locally
   {: id="20210204192136-k51xe4r"}
2. {: id="20210104091603-nl61p20"}On the new device, download the data from the cloud by Settings - Sync - Cloud notebook - Clone to local. Only when you need to clone the data for the first time on the new device, you can directly click the sync button to sync later.
   {: id="20210204192136-bxoq9z8"}
3. {: id="20210104091603-r3ojkne"}After synchronization, the interface will refresh as a whole and reload the data. If there is a conflict, it will be displayed in the ((20201210002930-7cvn3j6 "Git conflict markers"))
   {: id="20210204192136-6p52l5d"}
{: id="20210104091603-trcrdsg"}

{: id="20210204192136-gshtv2c"}


{: id="20201002092228-8hmuss5" type="doc"}

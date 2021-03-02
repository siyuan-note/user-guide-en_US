### What is "Git conflict markers"?
{: id="20201210002930-7cvn3j6" updated="20210302223923"}

The conflicting place looks like this in the document text (you can open the document through an external text editor to view):
{: id="20210104091606-v8sc1mu"}

```plaintext
<<<<<<< HEAD
Here is the original local content
=======
Here is the content pulled from the cloud
>>>>>>> feebfeb6bef44cf1384d51cdd7aef7e4197b8180
```
{: id="20210104091606-4lsb5wm"}

Need to edit manually to resolve conflicts.
{: id="20210104091606-ycjpo5x"}

## Why can't I sync empty folders?
{: id="20210104091606-3v4t3ui"}

This is the Git design. At least one file is required under the folder (the file content can be empty) to be included in version management.
{: id="20210104091606-ewcswyu"}

## How to sync to GitHub repository?
{: id="20201213120253-hhtskws"}

1. {: id="20210104091606-35a849n"}Create a repository on GitHub, and [Configure SSH](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh)
   {: id="20210226101133-m5jb3ym"}
2. {: id="20210104091606-cfkz1uz"}Configure the remote repository via `git remote add github git@github.com:user/repo.git` under the notebook folder, where:
   {: id="20210226101133-09aja7s"}

   * {: id="20210104091606-a1g1jhf"}`github` is the name of the remote repository, do not use `origin`, because `origin` is the official remote repository name of SiYuan
     {: id="20210226101133-cd73vsf"}
   * {: id="20210104091606-lchlidu"}`user/repo` please change to your own repository name
     {: id="20210226101133-f8os1b1"}
   {: id="20210104091606-2lnb23r"}
3. {: id="20210104091606-7e954xc"}Pull from remote via `git pull github main --allow-unrelated-histories`
   {: id="20210226101133-2sa4mjs"}
4. {: id="20210104091606-meitb2x"}Push the remote *master* branch through `git push github master`. Please note that the default branch name of the repository created by GitHub from October 2020 is *main*. After using this command, a `master` branch will be created on the remote repository. The default branch can be set to *master* in the repository Settings - Branches
   {: id="20210226101133-i9i3tx1"}
{: id="20210104091606-9r54ew3"}

#Note#: SiYuan official synchronization and using a third-party Git repository can only choose one of the two. If you need to use a third-party Git repository service, please disable automatic commit in Settings - Sync and reinitialize .git.
{: id="20210302090740-tb6knd5" updated="20210302090805"}

## How to sync to Gitee repository?
{: id="20201213120253-ulbi3zh"}

1. {: id="20210104091606-209mf44"}Create a repository on Gitee and [Configure SSH](https://gitee.com/help/articles/4191)
   {: id="20210226101133-ust1dnf"}
2. {: id="20210104091606-b9g1muu"}Configure the remote repository via `git remote add gitee git@gitee.com:user/repo.git` under the notebook folder, where:
   {: id="20210226101133-40vmttz"}

   * {: id="20210104091606-sfwyp0n"}`gitee` is the name of the remoterepository, please do not use `origin`, because `origin` is the official remote repository name of SiYuan
     {: id="20210226101133-xvijizh"}
   * {: id="20210104091606-o9xlaxo"}`user/repo` please change to your own repository name
     {: id="20210226101133-msm5kyr"}
   {: id="20210104091606-kxibpwr"}
3. {: id="20210104091606-e2cz0s7"}Pull from remote via `git pull gitee master --allow-unrelated-histories`
   {: id="20210226101133-wa5dhn4"}
4. {: id="20210104091606-12q4ndh"}Push remote *master* branch through `git push gitee master`
   {: id="20210226101133-php3e1u"}
{: id="20210104091606-6lab5s5"}

## How to delete unnecessary commit history to reduce space usage and improve performance?
{: id="20210104091606-i4hpgus"}

1. {: id="20210104091606-lwgyibw"}Please confirm that the cloud data has been completely pulled locally, and that complete data is already stored locally
   {: id="20210226101133-kwj3602"}
2. {: id="20210104091606-pz4p7pl"}Delete the cloud repository in Settings - Sync
   {: id="20210226101133-192g2ca"}
3. {: id="20210104091606-0nf9jm9"}Delete the .git metadata folder on the file system
   {: id="20210226101133-v7wjgl6"}
4. {: id="20210104091606-etzwcbz"}Close then re-open this notebook
   {: id="20210226101133-svtw32g" updated="20210301220348"}
5. {: id="20210104091606-fuijdda"}Click Sync to synchronize the data to the cloud repository
   {: id="20210226101133-wg8moci"}
{: id="20210104091606-cy60yx2"}

## How to delete cloud asset files that are no longer needed?
{: id="20210226101134-hvw08er" updated="20210226101142"}

#TODO#
{: id="20210226101144-fknnoaz" updated="20210301220415"}


{: id="20201210002859-thjj328" type="doc"}

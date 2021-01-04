### What is "Git conflict markers"?
{: id="20201210002930-7cvn3j6"}

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

You can edit it manually, or you can use the diff tool to edit it.
{: id="20210104091606-ycjpo5x"}

## Why can't I sync empty folders?
{: id="20210104091606-3v4t3ui"}

This is the Git design. At least one file is required under the folder (the file content can be empty) to be included in version management.
{: id="20210104091606-ewcswyu"}

## How to sync to GitHub repository?
{: id="20201213120253-hhtskws"}

1. {: id="20210104091606-35a849n"}Create a repository on GitHub, and [Configure SSH](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh)
2. {: id="20210104091606-cfkz1uz"}Configure the remote repository via `git remote add github git@github.com:user/repo.git` under the notebook folder, where:
   * {: id="20210104091606-a1g1jhf"}`github` is the name of the remote repository, do not use `origin`, because `origin` is the official remote repository name of SiYuan
   * {: id="20210104091606-lchlidu"}`user/repo` please change to your own repository name
   {: id="20210104091606-2lnb23r"}
3. {: id="20210104091606-7e954xc"}Pull from remote via `git pull github main --allow-unrelated-histories`
4. {: id="20210104091606-meitb2x"}Push the remote *master* branch through `git push github master`. Please note that the default branch name of the repository created by GitHub from October 2020 is *main*. After using this command, a `master` branch will be created on the remote repository. The default branch can be set to *master* in the repository Settings - Branches
{: id="20210104091606-9r54ew3"}

## How to sync to Gitee repository?
{: id="20201213120253-ulbi3zh"}

1. {: id="20210104091606-209mf44"}Create a repository on Gitee and [Configure SSH](https://gitee.com/help/articles/4191)
2. {: id="20210104091606-b9g1muu"}Configure the remote repository via `git remote add gitee git@gitee.com:user/repo.git` under the notebook folder, where:
   * {: id="20210104091606-sfwyp0n"}`gitee` is the name of the remoterepository, please do not use `origin`, because `origin` is the official remote repository name of SiYuan
   * {: id="20210104091606-o9xlaxo"}`user/repo` please change to your own repository name
   {: id="20210104091606-kxibpwr"}
3. {: id="20210104091606-e2cz0s7"}Pull from remote via `git pull gitee master --allow-unrelated-histories`
4. {: id="20210104091606-12q4ndh"}Push remote *master* branch through `git push gitee master`
{: id="20210104091606-6lab5s5"}

## How to delete unnecessary commit history to reduce space usage and improve performance?
{: id="20210104091606-i4hpgus"}

1. {: id="20210104091606-lwgyibw"}Please confirm that the cloud data has been completely pulled locally, and that complete data is already stored locally
2. {: id="20210104091606-pz4p7pl"}Delete the cloud repository in Settings - Sync
3. {: id="20210104091606-0nf9jm9"}Delete the .git metadata folder on the file system
4. {: id="20210104091606-etzwcbz"}Restart SiYuan (it will automatically generate a .git metadata folder based on existing data)
5. {: id="20210104091606-fuijdda"}Click Sync to synchronize the data to the cloud repository
{: id="20210104091606-cy60yx2"}


{: id="20201210002859-thjj328" type="doc"}

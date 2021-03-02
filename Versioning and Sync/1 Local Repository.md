SiYuan uses [Git](https://git-scm.com/) to implement version management. After opening the local folder (not WebDAV), the folder will be automatically initialized as a Git repository (the .git folder is generated to store Git metadata).
{: id="20210104091559-td6jgn8"}

## Commit changes
{: id="20210104091559-374fm0g"}

All changes to documents (such as creating, editing, renaming, and deleting) will be included in the version management. The timing of the change commit:
{: id="20210104091559-ydyr9y3" updated="20210223100607"}

* {: id="20210104091559-8hz2c8h"}The default interval is 10 minutes for automatic submission, which can be adjusted in the Settings - Sync
  {: id="20210223100524-7h68uqu" updated="20210302090850"}
* {: id="20210104091559-tl3mi3v"}The commit operation will also be performed when you click Sync
  {: id="20210223100524-62vae48"}
{: id="20210104091559-tzwh8fj"}

Only .md files are committed in the automatically created .gitignore by default, and other types of files will not be included in the version management.
{: id="20210223100527-12ki6gl" updated="20210302090443"}

## Browse commit history
{: id="20210104091559-14n7e2m"}

* {: id="20210104091559-52na08q"}Select History from the right-click drop-down menu of the editor tab
  {: id="20210223100524-mz5sicl"}
* {: id="20210104091559-3cov491"}Select History from the right-click drop-down menu of the file tree
  {: id="20210223100524-lxq8gng"}
{: id="20210104091559-kbfabo4"}

Currently only supports browsing the latest 32 commits history.
{: id="20210104091559-00iidlv"}

## Rollback version
{: id="20210104091559-kgrtuyh"}

In the time list column on the left side of the commit history interface, there is a revert button behind each commit. After clicking it, a confirmation dialog box will pop up. If the revert is confirmed, the commit will be reverted.
{: id="20210104091559-ejqvg9b"}

After reverting this commit, subsequent commits will still be retained, but the content may conflict and need to be manually edited and resolved.
{: id="20210121111547-j6brm6n"}

If you need to rollback or support more Git operations, please use the Git tool. #Note#: After using external tools, you need to restart SiYuan.
{: id="20210121111544-qe48tuf"}

{: id="20210121105905-k775koz"}


{: id="20201002092058-85k2cws" type="doc"}

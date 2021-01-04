SiYuan uses [Git](https://git-scm.com/) to implement version management. After opening the local folder (not WebDAV), the folder will be automatically initialized as a Git repository (the .git folder is generated to store Git metadata).
{: id="20210104091559-td6jgn8"}

## Commit changes
{: id="20210104091559-374fm0g"}

All changes to documents and resource files (such as creating, editing, renaming, and deleting) will be included in the version management. The timing of the change commit:
{: id="20210104091559-ydyr9y3"}

* {: id="20210104091559-8hz2c8h"}The default interval is 10 minutes for automatic submission, which can be adjusted in the Settings -Editor
* {: id="20210104091559-tl3mi3v"}The commit operation will also be performed when you click Sync
{: id="20210104091559-tzwh8fj"}

## Browse commit history
{: id="20210104091559-14n7e2m"}

* {: id="20210104091559-52na08q"}Select History from the right-click drop-down menu of the editor tab
* {: id="20210104091559-3cov491"}Select History from the right-click drop-down menu of the file tree
{: id="20210104091559-kbfabo4"}

Currently only supports browsing the latest 32 commits history.
{: id="20210104091559-00iidlv"}

## Rollback version
{: id="20210104091559-kgrtuyh"}

At present, SiYuan only supports browsing history. If you need to rollback or support more Git operations, please use the Git tool. #Note#: After using external tools, you need to restart SiYuan.
{: id="20210104091559-ejqvg9b"}


{: id="20201002092058-85k2cws" type="doc"}

SiYuan uses [Git](https://git-scm.com/) to implement version management. After opening the local folder (not WebDAV), the folder will be automatically initialized as a Git repository (the .git folder is generated to store Git metadata).

## Commit changes

All changes to documents and resource files (such as creating, editing, renaming, and deleting) will be included in the version management. The timing of the change commit:

* The default interval is 10 minutes for automatic submission, which can be adjusted in the Settings -Editor
* The commit operation will also be performed when you click Sync

## Browse commit history

* Select History from the right-click drop-down menu of the editor tab
* Select History from the right-click drop-down menu of the file tree

Currently only supports browsing the latest 32 commits history.

## Rollback version

At present, SiYuan only supports browsing history. If you need to rollback or support more Git operations, please use the Git tool. #Note#: After using external tools, you need to restart SiYuan.


{: id="20201002092058-85k2cws" type="doc"}

## Repository synchronization

The synchronization function is the [Advanced Features](https://github.com/siyuan-note/siyuan/projects/1) of SiYuan, and you need to pay to use it. After clicking the sync button on the interface, SiYuan will synchronize data through `git pull` and `git push`. If you encounter a data conflict, please use the Git tool to resolve the conflict. We will gradually increase the built-in support for Git operations in subsequent versions #TODO#.

#Note#: WebDAV notebooks will not be synchronized because the WebDAV server itself is already in the cloud.

We chose to use Git for version management not only because of the power and stability of Git, but also because it is open. So using our server cloud repository is not the only option. You can add other remote repositories (such as GitHub repositories) through the `git remote add` command, and then you can synchronize with these remote repositories via git. Please refer to the operation details :

* ((20201213120253-hhtskws "{{.text}}"))
* ((20201213120253-ulbi3zh "{{.text}}"))

## Cloud Repository

The cloud repository of our server is located at `git@siyuan.b3logfile.com:/siyuan/{uid}/{notebook}.git`, and the automatically generated SSH key pair is used for identity authentication. If you encounter problems with identity authentication when using the synchronization function, please check the public key in "Settings - Synchronization" and confirm whether the public key has been automatically added to the chain drop community individual [Settings - Public Key](https:/ /ld246.com/settings/key), if it is not added, please check the program log to determine whether it is a network problem. If the problem still cannot be solved, please ((20200923234102-ysbri6o "Contact us for feedback")).

* The maximum storage space of all notebooks under the same user is `4G` (including version history)
* After the paid subscription expires, the data will be retained for 1 month. If there is no renewal during this period, the data will be completely deleted after 1 month

## Synchronous use process

1. Click the sync button on the current device (if there is no repository in the cloud at this time, a cloud repository will be created), the data will be pushed to the cloud through the Git SSH protocol, and the cloud data will also be pulled locally
2. On the new device, download the data from the cloud by Settings - Sync - Cloud notebook - Clone to local. Only when you need to clone the data for the first time on the new device, you can directly click the sync button to sync later.
3. After synchronization, the interface will refresh as a whole and reload the data. If there is a conflict, it will be displayed in the ((20201210002930-7cvn3j6 "Git conflict markers")) (currently the rendering conflict in the editor is flawed, so it looks strange #TODO#)


{: id="20201002092228-8hmuss5" type="doc"}

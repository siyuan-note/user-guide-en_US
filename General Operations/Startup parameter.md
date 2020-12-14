## SiYuan Electron

### `--conf`

Used to specify the configuration file folder path, the default value when not specified is `~/.siyuan/`, this parameter will be passed to the kernel.

## SiYuan Kernel

### `--conf`

The meaning is the same as the parameter with the same name as Electron.

### `--wd`

Kernel working directory path, automatically obtained according to the kernel executable file entry if it is not specified.

### `--servePath`

Used to specify the server path, the default value is `window.location.hostname+":6806"`.

If you need to use `xxx.com/custom/` as a virtual directory or location, please specify this parameter.

### `--resident`

After specifying with `--resident=true`, the kernel will be resident in memory and will not automatically exit even if there is no active session. The default is `false`.

Set it to `true` This is useful when the kernel is used separately (such as through a browser). Even if you are not currently using SiYuan (the browser has not established a session with the kernel), the kernel process will not exit. By default `false`, the kernel process will scan the session every 7 seconds, and exit the process if there is no session.

### `readonly`

After specifying with `--readonly=true`, the kernel will run in read-only mode and all write operations will be prohibited.

### `auth`

After using `--auth=true`, the user data in conf.json will be used for authentication. This parameter is mainly used for the authentication of SiYuan online workspace. Please do not specify it during self-hosting.

### `linkBaseURL`

This parameter is used to specify the link and picture address prefix, and will only be added when using a relative path.


{: id="20200924100717-yzwzn64" type="doc"}

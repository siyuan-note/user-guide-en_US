The currently supported startup parameters are as follows:

## `--conf`

Used to specify the configuration file folder path, the default value when not specified is `~/.siyuan/`.

## `--resident`

`--resident=true` Use resident memory, even if there is no active session, it will not automatically exit. The default is `false`.

Set it to `true` This is useful when the kernel is used separately (such as through a browser). Even if you are not currently using SiYuan Notes (the browser has not established a session with the kernel), the kernel process will not exit. By default `false`, the kernel process will scan the session every 7 seconds, and exit the process if there is no session.

## `--servePath`

Used to specify the server path, the default value is `window.location.hostname+":6806"`.

If you need to use `xxx.com/custom/` as the virtual directory or location, please specify this parameter.

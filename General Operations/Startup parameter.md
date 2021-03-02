## SiYuan Electron
{: id="20201225172241-ifimln0" updated="20210302223756"}

### `--conf`
{: id="20201225172241-pkqsaon"}

Used to specify the configuration file folder path, the default value when not specified is `~/.siyuan/`, this parameter will be passed to the kernel.
{: id="20201225172241-p1fcj43"}

## SiYuan Kernel
{: id="20201225172241-w8hdt9o"}

### `--conf`
{: id="20201225172241-237rz9o"}

The meaning is the same as the parameter with the same name as Electron.
{: id="20201225172241-546q8dx"}

### `--wd`
{: id="20201225172241-m3ffs88"}

Kernel working directory path, automatically obtained according to the kernel executable file entry if it is not specified.
{: id="20201225172241-oyntdl9"}

### `--servePath`
{: id="20201225172241-iwddhe5"}

Used to specify the server path, the default value is `window.location.hostname+":6806"`.
{: id="20201225172241-ylc62tv"}

If you need to use `xxx.com/custom/` as a virtual directory or location, please specify this parameter.
{: id="20201225172241-stpgyx1"}

### `--resident`
{: id="20201225172241-r2u4sx1"}

After specifying with `--resident=true`, the kernel will be resident in memory, the default is `true`.
{: id="20201225172241-1ikfkn1"}

After set to `false`, the list of active sessions will be checked every 30 seconds, and the kernel process will be exited if there are no active sessions.
{: id="20201225172241-gon6cqc"}

### `--readonly`
{: id="20201225172241-asmvg1c"}

After specifying with `--readonly=true`, the kernel will run in read-only mode and all write operations will be prohibited.
{: id="20201225172241-2j3s1dc"}

### `--authCode`
{: id="20210117224305-alzt1xr"}

Used to specify the browser access ((20210104091447-3vmymbk "authentication password")), which will overwrite the authCode in conf.json after setting.
{: id="20210117224305-vyqi75g"}

### `--auth`
{: id="20201225172241-l0qn9q9"}

After using `--auth=true`, the user data in conf.json will be used for authentication. This parameter is mainly used for the authentication of SiYuan online workspace. Please do not specify it during self-hosting.
{: id="20201225172241-ar4975r"}

### `--ssl`
{: id="20201225172550-cmwure7"}

After using `--ssl=true`, https and wss protocols will be used for serving.
{: id="20201225172550-zxiz2vb"}


{: id="20200924100717-yzwzn64" type="doc"}

## Browser usage
{: id="20210104091447-8iiuxlt"}

SiYuan Desktop is an standalone application packaged based on [Electron](https://www.electronjs.org), but this is not the only way to use it. As long as the kernel of SiYuan is started, it can be used directly on the browser, supporting mobile browsers.
{: id="20210104091447-3oeqhre" updated="20210302223804"}

* {: id="20210104091447-2cfema8"}Desktop Web version: the experience is almost the same as the Electron standalone application
  {: id="20210302223802-g5brri7"}
* {: id="20210104091447-i60nkht"}Mobile Web version: specially designed for mobile-end user experience
  {: id="20210302223802-ju54kjt"}
{: id="20210104091447-35vbebb"}

After visiting `http://127.0.0.1:6806/`, the desktop or mobile version will be automatically switched according to the browser version.
{: id="20210104091447-3gpw4m6"}

If you need to use it in a local area network, just replace `127.0.0.1` with the local area network IP address. In addition to local LAN use, here are two self-service solutions for public network use:
{: id="20210104091447-ztky9z6"}

* {: id="20210104091447-2wey9jj"}Publish local kernel services on the public network through the "intranet penetration" technology (more troublesome and unstable, not recommended)
  {: id="20210302223802-1mbrz5a"}
* {: id="20210104091447-oo5sodh"}Build your own SiYuanServer (recommended)
  {: id="20210302223802-ghpurq7"}
{: id="20210104091447-6y4386v"}

Before embarking on these two solutions, please start with understanding [SiYuan Technical Architecture](https://ld246.com/article/1619868273581#%E6%8A%80%E6%9C%AF%E6%9E%B6%E6%9E%84).
{: id="20210104091447-br9zpri" updated="20210522214311"}

### Access authentication
{: id="20210104091447-dluat0m"}

In <kbd>Settings</kbd> - <kbd>About</kbd>, you can configure the browser access authentication password. Leaving it blank means that authentication is not enabled. This is more useful in open networks (such as office spaces and public networks), and only after authentication can you enter the work space.
{: id="20210104091447-3vmymbk" updated="20210522214406"}

{: id="20210117211053-tq2km4f"}


{: id="20201004194026-s8h2cog" type="doc"}

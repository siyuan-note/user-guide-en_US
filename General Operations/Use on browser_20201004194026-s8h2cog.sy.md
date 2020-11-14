## Workspace

SiYuan Desktop is an standalone application packaged based on [Electron](https://www.electronjs.org), but this is not the only way to use it. As long as the kernel of SiYuan is started, it can be used directly on the browser, supporting mobile browsers.

* Desktop Web version: the experience is almost the same as the Electron standalone application
* Mobile Web version: specially designed for mobile-end user experience

After visiting `http://127.0.0.1:6806/`, the desktop or mobile version will be automatically switched according to the browser version.

If you need to use it in a local area network, just replace `127.0.0.1` with the local area network IP address. In addition to local LAN use, here are two self-service solutions for public network use:

* Publish local kernel services on the public network through the "intranet penetration" technology (more troublesome and unstable, not recommended)
* Build your own SiYuanServer (recommended)

Before embarking on these two solutions, please start with understanding ((20201004194439-vd30x8i "SiYuan Technical Architecture")). In addition to the above solutions, paying users can directly use the Web [SiYuan Online Workspace](https://ld246.com/xanadu/) of our server.

### Access authentication

In Settings - About, you can configure the browser access authentication password. By default, leaving it blank means that authentication is not enabled. This is more useful in open networks (such as office spaces and public networks), and only after authentication can you enter the work space.

## Sharing and Publishing

In addition to using SiYuan Online Workspace, paid users can also use [SiYuan Online Sharing and Publishing](https://ld246.com/udanax/). After sharing the published notebook in Settings - Sync - Cloud Notebook, you can browse through "View my shared publishing space".

The shared publishing space can be accessed without logging in. Visitors browse in read-only mode and support most features, such as browsing relationship diagrams, searching, browsing tags, bookmarks, and multi-window tabs.

### Content block URL #TODO#

Open it in the editor tab by visiting `/blocks/{id}`.

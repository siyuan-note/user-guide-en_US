## Workspace

SiYuan Desktop is an standalone application packaged based on [Electron](https://www.electronjs.org), but this is not the only way to use it. As long as the kernel of SiYuan is started, it can be used directly on the browser, supporting mobile browsers.

* `http://127.0.0.1:6806/assets/build/desktop/`: Desktop web version, the experience is almost the same as the Electron standalone application
* `http://127.0.0.1:6806/assets/build/mobile/`: Mobile web version, specially designed for mobile-end user experience

You can also directly visit `http://127.0.0.1:6806/`, the program will automatically switch between desktop or mobile according to the browser version.

If you need to use it in a local area network, just replace `127.0.0.1` with the local area network IP address. In addition to local LAN use, here are two self-service solutions for public network use:

* Publish local kernel services on the public network through the "intranet penetration" technology (more troublesome and unstable, not recommended)
* Build your own SiYuanServer (recommended)

Before embarking on these two solutions, please start with understanding ((20201004194439-vd30x8i "SiYuan Technical Architecture")). In addition to the above solutions, paying users can directly use the web [SiYuan Online Workspace](https://ld246.com/xanadu/) of our server.

## Sharing and Publishing

In addition to using SiYuan Online Workspace, paid users can also use [Siyuan Online Sharing and Publishing](https://ld246.com/udanax/). After sharing the published notebook in Settings-Sync-Cloud Notebook, you can browse through "View my shared publishing space".

The shared publishing space can be accessed without logging in. Visitors browse in read-only mode and support most features, such as browsing relationship diagrams, searching, browsing tags, bookmarks, and multi-window tabs.

### Content block URL #TODO#

Open it in the editor tab by visiting `/blocks/{id}`.

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

In addition to using SiYuan Online Workspace, paid users can also use the sharing and publishing function. After sharing and publishing the notebook in Settings - Sync - Cloud Notebook, you can click "Share and Publish" to open the browser and browse.

The shared publishing space can be accessed without logging in. Visitors browse in read-only mode and support most features, such as browsing relationship graphs, searching, browsing tags, bookmarks, and multi-window tabs.

#Note#: If you want to share the link with others, please use your share and publish entry link (`https://ld246.com/udanax/youruid`), do not use the link after entering the main interface (ie do not use the `/stage/` link).

### Content block URL

Open it in the editor tab by visiting `/blocks/{id}`, the URL can be provided to other software for content block positioning, or used for local area network sharing.

The document block id is fixed on the file name, so as long as the file name is not modified externally, the id of the document block is persistent. Right-click the document in the file tree and then select "Copy URL" to get the URL of the document, which can be opened on the browser.

For other types of content block ids, you can see "Copy URL" after clicking the content block identifier in the editor. #Note#: The id of the non-document block may be not persistent. When the SiYuan kernel is closed, the unreferenced content block id will be automatically cleaned up, and the id will be regenerated at the next startup, which will cause the previously copied content block The URL is invalid. It is recommended to persist all content block ids, please turn on the option to keep content block ids in Settings - Editor.


{: id="20201004194026-s8h2cog" type="doc"}

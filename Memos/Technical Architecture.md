On the whole, SiYuan adopts the technical architecture of separation of front and back ends, and realizes front and back end communication through HTTP.

### Frontend

The frontend is currently mainly based on browser technology to implement user interaction interfaces and business logic related to the operating system platform.

* Electron
* Browser

The frontend can be extended to any client based on HTTP communication in the future.

### Backend

The backend is a resident HTTP server, which implements core business logic and state persistence. Listening port:

* `6806`: HTTP/WebSocket, listen to this port on all network cards (`0.0.0.0`), traffic under the path of `/siyuan/` will be automatically forwarded to the local port `127.0.0.1:6807`
* `6807`: HTTP/WebDAV, listen on this port at `127.0.0.1`

### Publish package

* Desktop application: Based on Electron packaging, the main process starts the kernel process after it is started. Static resources related to the kernel HTTP server interface, the Electron main window loads the interface through `loadURL`
* Server application: Only package resources such as the kernel, appearance, and documentation, and distribute them through the Docker image `b3log/siyuan`


{: id="20201004194439-vd30x8i" type="doc"}

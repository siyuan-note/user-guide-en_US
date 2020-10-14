On the whole, SiYuan adopts the technical architecture of separation of front and back ends, and realizes front and back end communication through HTTP.
{: id="20201004194451-nq4hmk3"}

### Frontend
{: id="20201004194451-tah88kh"}

The frontend is currently mainly based on browser technology to implement user interaction interfaces and business logic related to the operating system platform.
{: id="20201004194451-8shomp0"}

* Electron
* Browser
{: id="20201004194451-pplq39q"}

The frontend can be extended to any client based on HTTP communication in the future.
{: id="20201004194451-eeuzg7p"}

### Backend
{: id="20201004194451-zhggkdk"}

The backend is a resident HTTP server, which implements core business logic and state persistence. Listening port:
{: id="20201004194451-d0bwxmy"}

* `6806`: HTTP/WebSocket, listen to this port on all network cards (`0.0.0.0`), traffic under the path of `/siyuan/` will be automatically forwarded to the local port `127.0.0.1:6807`
* `6807`: HTTP/WebDAV, listen on this port at `127.0.0.1`
{: id="20201008111858-dyhp3l0"}

### Publish package
{: id="20201004194451-n9hb82w"}

* Desktop application: Based on Electron packaging, the main process starts the kernel process after it is started. Static resources related to the kernel HTTP server interface, the Electron main window loads the interface through `loadURL`
* Server application: Only package resources such as the kernel, appearance, and documentation, and distribute them through the Docker image `b3log/siyuan`
{: id="20201004194451-cv25ntt"}

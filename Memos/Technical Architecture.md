## B/S Style
{: id="20210104091528-gaw4kc8" updated="20210302223844"}

On the whole, SiYuan adopts the technical architecture of separation of front and back ends, and realizes front and back end communication through HTTP.
{: id="20210104091528-tucfsql"}

### Frontend
{: id="20210104091528-sy5xtbs"}

The frontend is currently mainly based on browser technology to implement user interaction interfaces and business logic related to the operating system platform.
{: id="20210104091528-8sb1hi3"}

* {: id="20210104091528-enerv2l"}Electron
  {: id="20210301203428-w2bj3sc"}
* {: id="20210104091528-vwpufj2"}Browser
  {: id="20210301203428-dovlbda"}
{: id="20210104091528-tlv0dml"}

The frontend can be extended to any client based on HTTP communication in the future.
{: id="20210104091528-82tumkq"}

### Backend
{: id="20210104091528-w3wp8hv"}

The backend is a resident HTTP server, which implements core business logic and state persistence. Listening port:
{: id="20210104091528-324x39i"}

* {: id="20210104091528-4dfx2yf"}`6806`: HTTP/WebSocket, listen to this port on all network cards (`0.0.0.0`), traffic under the path of `/siyuan/` will be automatically forwarded to the local port `127.0.0.1:6807`
  {: id="20210301203428-hcgij2m"}
* {: id="20210104091528-n239x1p"}`6807`: HTTP/WebDAV, listen on this port at `127.0.0.1`
  {: id="20210301203428-gj4nbec"}
{: id="20210104091528-v17cbhc"}

## Data state
{: id="20210104091528-8v3v84k"}

* {: id="20210104091528-v3ltm5q"}Persistent data is realized based on the file system of the operating system and stored in files and folders
  {: id="20210301203428-xxzpfsl"}
* {: id="20210104091528-e1v8ppd"}Read-only data is stored in SQLite database
  {: id="20210301203428-cxckeg9"}

  * {: id="20210104091528-bahjy9y"}Edit changes will be automatically synchronized to the database
    {: id="20210301203428-0p7h1ym"}
  * {: id="20210104091528-a59dhnd"}The database is created temporarily and only exists when the kernel is running
    {: id="20210301203428-zgt88cj"}
  {: id="20210104091528-ozud1lv"}
{: id="20210104091528-brco3rs"}

### Release delivery
{: id="20210104091528-mweeta8"}

* {: id="20210104091528-1rmn38g"}Desktop application: Based on Electron packaging, the main process starts the kernel process after it is started. Static resources related to the kernel HTTP server interface, the Electron main window loads the interface through `loadURL`
  {: id="20210301203428-tnsq6h4"}
* {: id="20210104091528-xz39ajx"}Server application: Only package resources such as the kernel, appearance, and documentation, and distribute them through the Docker image `b3log/siyuan`
  {: id="20210301203428-9hlk3sw"}
* {: id="20210301203657-wdawky8"}Mobile application: compiled into a mobile terminal library through golang mobile, and loaded the interface through WebView
  {: id="20210301203657-8uspge3" updated="20210301203657"}
{: id="20210104091528-793ahgx" updated="20210301203658"}


{: id="20201004194439-vd30x8i" type="doc"}

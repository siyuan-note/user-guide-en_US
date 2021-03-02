The simplest solution to serve SiYuan on the server is to deploy through Docker. The image name is `b3log/siyuan`. There is currently no version tag, only the latest version.
{: id="20201227201128-8jq61mc" updated="20210302223726"}

## File structure
{: id="20201227201751-w3gbqzd"}

The overall program is located under `/opt/siyuan/`, which is basically the structure under the resources folder of the Electron installation package:
{: id="20201227201751-oe2am4n"}

* {: id="20201227201751-eu0nvks"}appearance: icon, theme, languages
  {: id="20210208152449-owk20ip"}
* {: id="20201227201751-gd22k42"}guide: user guide document
  {: id="20210208152449-qmejh91"}
* {: id="20201227201751-8bhzm9k"}stage: interface and static resources
  {: id="20210208152449-5c6c485"}
* {: id="20201227201751-qy982a8"}kernel: kernel program
  {: id="20210208152449-69f23q7"}
{: id="20201227201751-ep0guzc"}

## Entrypoint
{: id="20201227201751-5d6snqe"}

The entry point is set when building the Docker image: `ENTRYPOINT ["/opt/siyuan/kernel" ]`, use `docker run b3log/siyuan` with parameters to start:
{: id="20201227201751-tbpaexo" updated="20210301202831"}

* {: id="20201227201751-n5o2ot2"}`--conf` specifies the configuration folder path, the configuration folder is mounted to the container via `-v` on the host
  {: id="20210208152449-9gz7jy5"}
* {: id="20210301202834-kgtx12h"}`--data` specifies the data folder path, the data folder is mounted to the container via `-v` on the host
  {: id="20210301202834-3itacib" updated="20210301202901"}
* {: id="20201227201751-cxo94yt"}`--resident` specified as true resident in memory
  {: id="20210208152449-og2hpgc"}
{: id="20201227201751-gmofu4a" updated="20210301202856"}

More parameters can refer to ((20201225172241-w8hdt9o "here")). The following is an example of a startup command:
{: id="20210301202938-prn2v5a" updated="20210301203044"}

`docker run -v conf_dir_host:conf_dir_container -v data_dir_host:data_dir_container -p 6806:6806 b3log/siyuan --resident=true --conf=conf_dir_container --data=data_dir_container`
{: id="20201227201751-20ez9rs" updated="20210301203103"}

* {: id="20201227201751-8l5oixx"}`conf_dir_host`: the configuration folder path on the host
  {: id="20210208152449-7fj2x6h"}
* {: id="20201227201751-pw8tdgg"}`conf_dir_container`: The path of the configuration folder in the container, which is the same as specified in `--conf`
  {: id="20210208152449-y2ogxyt"}
* {: id="20201227201751-wn3qqvc"}`data_dir_host`: the path of the host data folder
  {: id="20210208152449-fmxop31"}
* {: id="20201227201751-3k8gqkf"}`data_dir_container`: the path of the data folder in the container
  {: id="20210208152449-4bow85v" updated="20210301203118"}
{: id="20201227201751-pt653to"}

To simplify, it is recommended to configure the conf and data folder paths to be consistent on the host and container respectively, such as:
{: id="20201227201751-yyfayag"}

* {: id="20201227201751-jx3yrvy"}`conf_dir_host` and `conf_dir_container` are configured as /siyuan/conf
  {: id="20210208152449-1zeadz0"}
* {: id="20201227201751-xlea56k"}`data_dir_host` and `data_dir_container` are configured as /siyuan/data
  {: id="20210208152449-5qsmhee"}
{: id="20201227201751-wr70ypz"}

Examples of corresponding startup commands:
{: id="20201227201751-ii5q18q"}

`docker run -v /siyuan/conf:/siyuan/conf -v /siyuan/data:/siyuan/data -p 6806:6806 b3log/siyuan --resident=true --conf=/siyuan/conf/ --data=/siyuan/data/`
{: id="20201227201751-n5c4xje" updated="20210301203147"}

## Kernel API
{: id="20201227201751-gv0fpx2"}

### Open folder
{: id="20201227201751-jknx8vo"}

POST `/notebook/mount`, parameters:
{: id="20201227201751-z4trsir"}

* {: id="20201227201751-41dzs8v"}`url`: fixed incoming `http://127.0.0.1:6806/siyuan/`, which is box.url
  {: id="20210208152449-2peeuwd"}
* {: id="20201227201751-1plgjv1"}`path`: a folder path under the kernel data folder, which is box.path
  {: id="20210208152449-cr5leoe"}
{: id="20201227201751-k6540a2"}

### Close folder
{: id="20201227201751-vjvztxc"}

POST `/notebook/unmount`, parameters:
{: id="20201227201751-4vxvbmh"}

* {: id="20201227201751-f88y1qh"}`url`: fixed incoming `http://127.0.0.1:6806/siyuan/`, which is box.url
  {: id="20210208152449-a0rfkn6"}
{: id="20201227201751-3uuxh8x"}


{: id="20201227201128-m1wrouw" type="doc"}

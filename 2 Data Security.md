{: id="20210524221103-alpvx6e"}

## Overview
{: id="20210524221104-v1dw8e1"}

Data security is mainly divided into two aspects:
{: id="20210524221104-c493sem"}

1. {: id="20210524221104-55p4rbu"}Availability: no data loss, no conflict, keep the data integrity and consistency
   {: id="20210524221104-o0qiulk"}
2. {: id="20210524221104-pncmgx4"}Confidentiality: data will not be leaked or tampered with
   {: id="20210524221104-r5hvq6f"}
{: id="20210524221104-kxe4z7v"}

SiYuan supports both of these aspects to a certain extent, but due to environmental factors, we can only do our best to achieve what we can do. Below we describe some security restrictions and usage recommendations.
{: id="20210524221104-8ka9zj6" updated="20210524221111"}

## Plaintext storage
{: id="20210524221104-8xhfndh"}

* {: id="20210524221104-wd2jz54"}The data is stored in plain text in text files, and anyone or software who can access these text files can read the data
  {: id="20210524221104-3m1slkc"}
* {: id="20210524221104-19m97vd"}The availability of data depends on the availability of hardware disks and operating systems
  {: id="20210524221104-oltwnro"}
{: id="20210524221104-eqqbjvd"}

## Cloud backup
{: id="20210524221104-wlauarl"}

* {: id="20210524221104-5xoa6dq"}Implement secure network transmission through SSH protocol, and Rsync implements incremental data transmission
  {: id="20210524221104-wen47n8" updated="20210524221158"}
* {: id="20210524221104-86tj6m6"}The cloud uses the block storage service provided by Alibaba Cloud and the disk snapshot once every three days, theoretically reliability can be guaranteed
  {: id="20210524221104-egbptu2"}
* {: id="20210524221104-1ejjdmr"}The backup data is encrypted end-to-end (AES GCM), unless the password is known, it is almost impossible to decrypt (the developer cannot decrypt it)
  {: id="20210524221104-efcef3d" updated="20210525115904"}
{: id="20210524221104-oxv9mpv"}

## Suggest
{: id="20210524221104-umgsrpl"}

* {: id="20210524221104-98hi3um"}Data is regularly backed up to multiple offline devices
  {: id="20210524221104-m5reabu"}
* {: id="20210524221104-8386owm"}It is recommended to use special software, equipment or offline storage for important passwords, keys or core secrets
  {: id="20210524221104-5e4dtzy"}
{: id="20210524221104-osopyev"}


{: id="20210117215840-jcl17fx" type="doc"}

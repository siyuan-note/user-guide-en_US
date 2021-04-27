## Overview
{: id="20210117215840-wb362dh" updated="20210302223948"}

Data security is mainly divided into two aspects:
{: id="20210117215851-96wajhx" updated="20210302223934"}

1. {: id="20210117215851-hfpmff7"}Availability: data is not lost or conflicted, keeping data integrity and consistency
   {: id="20210302223933-rakcwo6"}
2. {: id="20210117215851-m7ke2ur"}Confidentiality: data will not be leaked or tampered with
   {: id="20210302223933-ficb94k"}
{: id="20210117215851-nc0bird"}

SiYuan supports both of these aspects to a certain extent, but due to environmental factors, we can only try our best to do as much as we can. Below we describe some security restrictions and usage recommendations.
{: id="20210117215851-ddrlqbt"}

## Plaintext storage
{: id="20210117215851-ix28le8"}

* {: id="20210117215851-p3xgi3t"}The data of SiYuan is stored in plain text in text files, and anyone or software who can access these text files can read the data
  {: id="20210302223933-aalghw5"}
* {: id="20210117215851-crybuhe"}The availability of local notebook data depends on the availability of hardware disks and operating systems
  {: id="20210302223933-9zi49ox"}
* {: id="20210117215851-gl6eiyi"}Data integrity and consistency are the same as above. Special note is needed here: if the synchronization network disk is enabled locally, consistency may be reduced (the synchronization disk may produce multiple data copies)
  {: id="20210302223933-srkhpyt"}
{: id="20210117215851-ldx930v"}

## Cloud synchronization
{: id="20210117215851-o3132ir"}

* {: id="20210117215851-jog6r3y"}Implement secure network transmission through SSH protocol
  {: id="20210302223933-ezje4tk" updated="20210402001608"}
* {: id="20210117215851-hwz4dk1"}The cloud uses the block storage service provided by Alibaba Cloud and the disk snapshot every three days, and theoretically reliability can be guaranteed
  {: id="20210302223933-77a9z22"}
* {: id="20210117220828-8ejo3gi"}The cloud repository is not encrypted, and the two core developers of the SiYuan team and related operation and maintenance personnel of Alibaba Cloud can see the data
  {: id="20210302223933-w5zbu1r"}
{: id="20210117215851-amwpvg0"}

If there is content that needs to be kept secret, please do not use the cloud sync function. This is mainly limited by network-related laws and regulations: as a service provider, we need to be able to see the plaintext of the data when necessary. This applies to all Internet services that operate in compliance in Mainland China.
{: id="20210117215851-jjjbmcj"}

## Suggest
{: id="20210117215851-1knwkrg"}

* {: id="20210117215851-3lroyeu"}Try not to edit simultaneously through multiple editing software
  {: id="20210302223933-iuf0h5x"}
* {: id="20210117215851-9jl3t6i"}Data is regularly backed up to multiple offline devices
  {: id="20210302223933-x3pehyy"}
* {: id="20210117215851-0p85gl7"}If the data is very important (such as important passwords, keys or core secrets, etc.), do not use any software or services to save it (operating system software, network environment, etc. have security risks)
  {: id="20210302223933-s4eelga"}
{: id="20210117215851-2t1bh8i"}


{: id="20210117215840-jcl17fx" type="doc"}

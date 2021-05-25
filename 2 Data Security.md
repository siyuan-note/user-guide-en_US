{: id="20210524221104-m5reabu" updated="20210525221056"}

## Overview
{: id="20210525221058-r31kj66"}

Data security is mainly divided into two aspects:
{: id="20210525221058-fa7kgu1"}

* {: id="20210525221058-anc2ab3"}Availability: no data loss, no conflict, keep the data complete and consistent
  {: id="20210525221058-mup5sfq"}
* {: id="20210525221058-dfjbta4"}Confidentiality: data will not be leaked or tampered with
  {: id="20210525221058-2ohczk0"}
{: id="20210525221058-fazkwe1"}

SiYuan supports both of these aspects. The following is an explanation about data security.
{: id="20210525221058-iyw9lks" updated="20210525221105"}

## Plaintext storage
{: id="20210525221058-kpw9brv"}

SiYuan uses plaintext to store data on the local file system, which means:
{: id="20210525221058-1seentt" updated="20210525221108"}

* {: id="20210525221058-tldy3gt"}Anyone or software who can use the operating system can read the data in it
  {: id="20210525221058-y6hnqfc"}
* {: id="20210525221058-1a0eyku"}The availability of data depends on the availability of hardware disks and operating systems
  {: id="20210525221058-k0iejbl"}
{: id="20210525221058-g14qmg0"}

## End-to-end encrypted backup
{: id="20210525221058-xl0yey6"}

SiYuan encrypts the workspace when it generates backup, and the backup data can be safely transmitted and hosted over the network.
{: id="20210525221058-r08diix" updated="20210525221122"}

* {: id="20210525221058-548v2tj"}End-to-end encryption, encryption and decryption are performed locally
  {: id="20210525221058-hhhr9bg"}
* {: id="20210525221058-rmgbcvv"}The encryption algorithm is AES GCM, which is recognized as safe in the industry
  {: id="20210525221058-b4vcxmd"}
* {: id="20210525221058-ev4g515"}Unless the password is known or brute force cracking, it cannot be decrypted (the developer cannot decrypt it either)
  {: id="20210525221058-hsm7qrz"}
* {: id="20210525221058-dziwuag"}The password is not stored, and the user needs to input when encrypting and decrypting
  {: id="20210525221058-vt07uf5"}
{: id="20210525221058-f7tzw3t"}

## Suggest
{: id="20210525221058-glc6a4g"}

* {: id="20210525221058-crmh93b"}Regularly back up data to the cloud and offline devices at the same time
  {: id="20210525221058-wan6o29"}
* {: id="20210525221058-gviygqc"}It is recommended to use special software, equipment or offline storage for important passwords, keys or core secrets
  {: id="20210525221058-mevfl0t"}
{: id="20210525221058-9rvlvm1"}



{: id="20210117215840-jcl17fx" type="doc"}

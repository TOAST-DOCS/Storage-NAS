<!-- pre-align:aligned sig=b4ad2412c335 -->

<a id="storage-nas-offline-overview"></a>
## Storage > NAS (offline) > Overview { #storage-nas-offline-overview }

With NAS, data sharing becomes easier by connecting a shared storage to an instance.   

<a id="glossary"></a>
## Glossary { #glossary }

<a id="nas-network-attached-storage"></a>
### NAS (Network Attached Storage) { #nas-network-attached-storage }

A file-level data storage device connected to a computer network which provides control of access by heterogeneous clients.  

<a id="volume"></a>
### Volume { #volume }

A logical unit of data storage space of NAS. 
An instance can mount NAS volume to save or read data.   

<a id="snapshot"></a>
### Snapshot { #snapshot }

A backup of NAS volume as reference of data duplication of a time. With snapshot, data can be recovered to a particular point in time.   
NAS service allows saving a snapshot per day, for three times, and data may be reverted back to records of three days before.     
However, saving snapshots may not be used, as it uses a part of NAS volume. 


<a id="features"></a>
## Features { #features }

<a id="sharing"></a>
### Sharing { #sharing }

NAS volume can be mounted to more than one instance.
Supported Protocol: NFS v3(Linux)

<a id="convenient"></a>
### Convenient { #convenient }

No additional file system configuration is required as file-level volume is mounted.

<a id="flexible"></a>
### Flexible { #flexible }

Even while NAS volume is used, storage volume can be scaled up or down.  

<a id="secure"></a>
### Secure { #secure }

Accessing NAS volume is made via a project network, which is isolated from a different project network. 


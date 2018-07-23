## Storage > NAS (offline) > Console Guide

## Apply for NAS

1. Go to **Storage > NAS (offline)** and click **Apply for Product Use** on the **Pricing** tab.  
  ![NAS 신청 화면 갈무리](http://static.toastoven.net/prod_infrastructure/nas/nas-request.png)

2. Enter information as follows: 
  * Application Type 
    To apply for a product use, **Create Volume** is automatically set. 
  * Block Storage Name 
    Enter a name with less than 8 characters in combination of alphabets and numbers: an actual NAS Volume is created in the name of the volume.
  * Application Size (GB) 
    NAS can be applied for at least 300 GB: select a size in the drop-down menu.  
  * Use Snapshot  
    Apply Nas Volume to save snapshot data: to restore by snapshot, contact administrator. 
  * NAS Information 
    NAS information refers to the name of NAS Volume that is actually assigned: to be created and entered by professional engineers.

3. NAS Volume, when completely created, shall be notified by email.  


## NAS Usage Details 

Shows details of usage at **Storage > NAS (offline) > Usage Details**.

![NAS 이용내역 화면 갈무리](http://static.toastoven.net/prod_infrastructure/nas/nas-volume-list.png)


## Increase Volume 

You can increase volume at NAS Usage Details: it is available only when the status of NAS is **Application Received**, or **In Service**.  

1. Click **Increase Volume**.  
  ![NAS 용량증설 화면 갈무리](http://static.toastoven.net/prod_infrastructure/nas/nas-extend-request.png)

2. Enter volume information to add in the dialogue box and click **Apply**. 


## Delete Volume 

Delete volume from NAS Usage Details. 

1. Click **Delete Volume**.  
  ![NAS volume 삭제 화면 갈무리](http://static.toastoven.net/prod_infrastructure/nas/nas-volume-del-request.png)

2. Check information to delete in the dialogue box and click **Apply**.


## Attach Volume 

### Install nfs Package

* Debian, Ubuntu: nfs-common, rpcbind  
  ```
  sudo apt-get install nfs-common rpcbind
  ```
* CentOS: nfs-utils, rpcbind  
  ```
  sudo yum install nfs-utils rpcbind
  ```

### Execute rpcbind 

```
sudo service rpcbind start
```

### Mount NAS Volume 

```
sudo mount -t nfs {nas source} {mount point}
```

* NAS Source: NAS volume information 
  e.g) 192.168.0.241:/data
* Mount Point: Directory to mount NAS volume   
  e.g) /mnt


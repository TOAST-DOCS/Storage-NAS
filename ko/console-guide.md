## Storage > NAS(Offline) > 콘솔 사용 가이드

## NAS 신청

1. [Infrastructure] > [Compute & Network] > [NAS(offline)]으로 이동한 뒤, [이용요금] 탭의 [상품 이용 신청]버튼을 클릭합니다.  
  [스크린샷]  

2. [그림 2] 의 대화창에서 NAS 관련 정보를 입력합니다. 필요한 정보는 다음과 같습니다.  
  [스크린샷]  
  * 신청유형  
    상품 이용 신청일 경우 [Volume 생성]으로 자동으로 입력됩니다.
  * volume 이름  
    NAS Volume 이름으로 영문/숫자 형태로 8자리 이하의 이름을 입력합니다. 입력된 Volume 이름으로 실제 Nas Volume 이 생성이 됩니다.
  * 크기(GB)  
    NAS 는 신규 생성시 300GB 이상부터 신청이 가능합니다. 필요한 용량을 스크롤을 이용하여 선택합니다
  * Snapshot  
    Snapshot 기능을 사용할 경우, Snapshot 은 1일 1회 3일 NAS 의 Snapshot 을 관리합니다. Snapshot 사용시 Snapshot 기능은 Nas Volume 을 사용합니다. Snapshot 을 이용한 복구는 별도 문의 바랍니다
  * NAS 정보
    NAS 정보는 실제 할당된 NAS Volume 명입니다. 전문 엔지니어가 NAS Volume 생성 후 입력하는 정보입니다.

3. NAS Volume 생성이 완료되면 아래와 같은 메일로 안내가 됩니다.


## NAS 이용내역

[Infrastructure] > [Compute & Network] > [NAS(offline)]의 상품 이용 신청 후, [이용내역] 탭을 선택합니다.  

[스크린샷] 

## Volume 증설

NAS 이용내역에서 Volume 증설을 할 수 있습니다. Volume증설은 NAS 의 상태가 [신청접수], [이용중] 일 경우에만 버튼이 활성화됩니다. [그림 5]에서 [Volume 증설] 버튼을 클릭합니다. [그림 6]의 대화창에서 증설할 추가 용량 정보를 입력합니다.

[스크린샷]

## Volume 삭제

NAS 이용내역에서 Volume 을 삭제 할 수 있습니다. [그림 7]의 내용 확인 후 [신청] 버튼을 클릭합니다.

[스크린샷]

## Volume 연결

### nfs 패키지 설치

  * Debian, Ubuntu: nfs-common, rpcbind  
    ```
    sudo apt-get install nfs-common rpcbind
    ````
  * CentOS: nfs-utils, rpcbind  
    ```
    sudo yum install nfs-utils rpcbind
    ```

### rpcbind 서비스 실행

```
sudo service rpcbind start
```

### NAS volume 마운트

```
sudo mount -t nfs {nas source} {mount point}
```

* nas source: NAS volume 정보  
  예) 192.168.0.241:/data
* mount point: NAS volume 을 마운트 할 디렉터리  
  예) /mnt


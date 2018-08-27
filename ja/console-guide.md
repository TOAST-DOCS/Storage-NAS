## Storage > NAS(Offline) > コンソール使用ガイド

## NASの申請

1. **Storage > NAS (offline)**を選択して **利用料金**から **サービス利用申請** ボタンをクリックします。  
  ![NAS申請画面キャプチャ](http://static.toastoven.net/prod_infrastructure/nas/nas-request.png)

2. 関連情報を入力します。
  * 申請タイプ 
   商品利用申請の場合、 **Volume作成**が自動的に入力されます。
  * Block Storageの名前 
    NASボリュームの名前です。英数字8桁以内の名前を入力します。入力されたボリューム名で実際のNASのボリュームが作成されます。
  * 申請サイズ(GB)  
    NASは新規作成時、 300GB以上から申請できます。スライドバーを調整して希望するサイズを設定します。
  * Snapshotの使用 
    Snapshotのデータ保存にはNASボリュームを使用します。 Snapshotを利用した復旧は別途お問い合わせください。
  * NASの情報  
    NASの情報は実際に割り当てられたNASのボリューム名です。専門エンジニアがNASのボリュームを作成した後に入力する情報です。

3. NASのボリューム作成が完了すると、メールで案内されます。


## NASの利用内訳

**Storage > NAS(offline)**を選択し、 **利用内訳**でNASを利用した内訳を確認できます。![NAS利用内訳画面キャプチャ](http://static.toastoven.net/prod_infrastructure/nas/nas-volume-list.png)


## ボリュームの増設

NAS利用内訳でボリュームを増設できます。NASの状態が**申請受付**、 **利用中**の時のみ増設できます。

1. **Volume増設** ボタンをクリックします。
  ![NAS容量増設画面のキャプチャ](http://static.toastoven.net/prod_infrastructure/nas/nas-extend-request.png)

2. 増設する追加容量の情報を指定し、**申請** ボタンをクリックします。


## ボリュームの削除

NAS利用内訳でボリュームを削除できます。

1. **Volume削除** ボタンをクリックします。
  ![NAS volume削除画面キャプチャ](http://static.toastoven.net/prod_infrastructure/nas/nas-volume-del-request.png)

2. ダイアログボックスで削除する情報を確認し、**申請** ボタンをクリックします。


## ボリュームの接続

### nfsパッケージのインストール

* Debian、 Ubuntu: nfs-common、 rpcbind  
  ```
  sudo apt-get install nfs-common rpcbind
  ```
* CentOS: nfs-utils、 rpcbind  
  ```
  sudo yum install nfs-utils rpcbind
  ```

### rpcbindサービスの実行

```
sudo service rpcbind start
```

### NASボリュームのマウント

```
sudo mount -t nfs {nas source} {mount point}
```

* nas source: NASボリューム情報  
 例) 192.168.0.241:/data
* mount point: NASボリュームをマウントするディレクトリ  
 例) /mnt


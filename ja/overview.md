<!-- pre-align:aligned sig=b4ad2412c335 -->

<a id="storage-nas-offline-overview"></a>
## Storage > NAS(Offline) > 概要 { #storage-nas-offline-overview }

NASサービスを使用すると、インスタンスに共有ストレージを接続してデータを簡単に共有できます。

<a id="glossary"></a>
## 用語 { #glossary }

<a id="nas-network-attached-storage"></a>
### NAS(Network Attached Storage) { #nas-network-attached-storage }

コンピュータネットワークに接続されたファイル水準の記憶装置です。他のクライアントからのデータアクセスを制御できます。

<a id="volume"></a>
### Volume { #volume }

NASでデータを保管する論理的な保存スペースを意味します。  
インスタンスはNASのvolumeをマウントしてデータの保存や読み取りができます。

<a id="snapshot"></a>
### Snapshot { #snapshot }

NAS volumeの特定時点の複製データの参照です。NAS volumeのバックアップを意味します。  
Snapshotを使用すると、特定時点のデータに復元をできます。  
NASサービスは1日1回ずつ、3日分のsnapshotを保存して最大3日前のデータに復元できます。
ただし、 Snapshotの保存はNAS volumeの一部を使用するため、使用しない場合があります。


<a id="features"></a>
## 特徴 { #features }

<a id="sharing"></a>
### 共有 { #sharing }

NAS volumeを1つ以上のインスタンスにマウントして使用できます。  
サポートするプロトコル：NFS v3(Linux)

<a id="convenient"></a>
### 利便性 { #convenient }

ファイル水準のvolumeをマウントするため、別途のfilesystem構成が必要ありません。

<a id="flexible"></a>
### 柔軟性 { #flexible }

NAS volumeの使用中にも保存場所の容量拡張および縮小ができます。

<a id="secure"></a>
### セキュリティー { #secure }

プロジェクトのネットワークを経由してNAS volumeにアクセスするため、別のプロジェクトのネットワークと隔離されています。

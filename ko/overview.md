<!-- pre-align:aligned sig=b4ad2412c335 -->

<a id="storage-nas-offline-overview"></a>
## Storage > NAS(Offline) > 개요 { #storage-nas-offline-overview }

NAS 서비스를 사용하면 인스턴스에 공유 스토리지를 연결하여 데이터를 쉽게 공유할 수 있습니다.

<a id="glossary"></a>
## 용어 { #glossary }

<a id="nas-network-attached-storage"></a>
### NAS(Network Attached Storage) { #nas-network-attached-storage }

컴퓨터 네트워크에 연결된 파일 수준의 저장장치를 뜻하며 다른 클라이언트로 부터의 데이터 접근을 제어할 수 있습니다.

<a id="volume"></a>
### Volume { #volume }

NAS 에서 데이터를 보관하는 논리적인 저장공간을 뜻합니다.  
인스턴스는 NAS 의 volume 을 마운트하여 데이터를 저장하거나 읽을 수 있습니다.

<a id="snapshot"></a>
### Snapshot { #snapshot }

NAS volume 의 시점 복제 데이터의 참조로 NAS volume 의 백업을 뜻합니다.  
Snapshot 을 사용하면 특정 시점의 데이터로 복원을 할 수 있습니다.  
NAS 서비스는 1일 1회씩 3일분 snapshot 을 저장하여 최대 3일 전의 데이터로 복원 할 수 있습니다.
단, Snapshot 저장은 NAS volume 의 일부를 사용하게 되기 때문에 사용하지 않을 수 있습니다.


<a id="features"></a>
## 특징 { #features }

<a id="sharing"></a>
### 공유 { #sharing }

NAS volume 을 하나 이상의 인스턴스에 마운트하여 사용할 수 있습니다.  
지원하는 프로토콜: NFS v3(Linux)

<a id="convenient"></a>
### 편리성 { #convenient }

파일 수준의 volume 을 마운트하기 때문에 별도의 filesystem 구성이 필요하지 않습니다.

<a id="flexible"></a>
### 유연성 { #flexible }

NAS volume 을 사용중에도 저장소 용량의 확장 및 축소가 가능합니다.

<a id="secure"></a>
### 보안성 { #secure }

프로젝트의 네트워크를 통해서 NAS volume 에 접근하기 때문에 다른 프로젝트의 네트워크와 격리 되어있습니다.


---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522288"
---
# ServiceFabric 모듈 AzureRM
## 설명은
보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.

## ServiceFabric Cmdlet AzureRM
### [추가-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다. 인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.

### [추가-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.

### [추가-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
클러스터에 보조 클러스터 인증서를 추가 합니다.

### [추가-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
클러스터의 특정 노드 형식에 노드를 추가 합니다.

### [추가-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
기존 클러스터에 새 노드 형식을 추가 합니다.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
클러스터 리소스 세부 정보를 가져옵니다.

### [새로운 AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다. 제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다. 자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다. 

### [제거-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.

### [제거-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.

### [제거-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.

### [제거-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
클러스터에서 전체 노드 유형을 제거 합니다.

### [제거-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.

### [업데이트-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.

### [업데이트-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.


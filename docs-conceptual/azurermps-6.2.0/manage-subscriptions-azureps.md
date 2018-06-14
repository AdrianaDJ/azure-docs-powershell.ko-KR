---
title: Azure PowerShell을 사용하여 Azure 구독 관리
description: Azure PowerShell을 사용하여 Azure 구독 관리
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: fbd2fe315efbdfb2147218229d51e983e2b61361
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323478"
---
# <a name="manage-multiple-azure-subscriptions"></a>여러 Azure 구독 관리

Azure를 처음 접하는 분들은 아마도 구독을 하나만 갖고 계실 것입니다. 하지만 한동안 Azure를 사용해 오신 분들 중에는 Azure 구독을 여러 개 만든 분도 있을 것입니다. 특정 구독에 대해 명령을 실행하도록 Azure PowerShell을 구성할 수 있습니다.

1. 계정의 모든 구독 목록을 가져옵니다.

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. 기본 구독을 설정합니다.

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. `Get-AzureRmContext` cmdlet을 실행하여 변경 내용을 확인합니다.

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

기본 구독을 설정한 이후부터는 모든 Azure PowerShell 명령이 기본 구독에 대해 실행됩니다.

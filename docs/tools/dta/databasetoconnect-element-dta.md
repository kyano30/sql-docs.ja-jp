---
title: DatabaseToConnect 要素 (DTA)
description: dta ユーティリティでは、DatabaseToConnect 要素により、データベース エンジン チューニング アドバイザーがワークロードのチューニング時に最初に接続するデータベースを指定します。
ms.prod: sql
ms.prod_service: sql-tools
ms.technology: tools-other
ms.topic: conceptual
dev_langs:
- XML
helpviewer_keywords:
- DatabaseToConnect element
ms.assetid: 65153a66-3aee-4429-99b7-0816ac23c285
author: markingmyname
ms.author: maghan
ms.reviewer: ''
ms.custom: seo-lt-2019
ms.date: 03/01/2017
ms.openlocfilehash: 1d03125d005d1374f75799813a355c5165713bfc
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "85732112"
---
# <a name="databasetoconnect-element-dta"></a>DatabaseToConnect 要素 (DTA)

 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

データベース エンジン チューニング アドバイザーがワークロードのチューニング時に最初に接続するデータベースを指定します。  
  
## <a name="syntax"></a>構文  
  
```  
  
    <TuningOptions>  
...code removed here...  
      <DatabaseToConnect>...</DatabaseToConnect>  
```  
  
## <a name="element-characteristics"></a>要素の特性  
  
|特徴|説明|  
|--------------------|-----------------|  
|**データ型と長さ**|**string**、長さは無制限です。|  
|**既定値**|[なし] :|  
|**個数**|省略可能。 **TuningOptions** 要素につき 1 回使用できます。|  
  
## <a name="element-relationships"></a>要素の関係  
  
|リレーションシップ|要素|  
|------------------|--------------|  
|**親要素**|[TuningOptions 要素 &#40;DTA&#41;](../../tools/dta/tuningoptions-element-dta.md)|  
|**子要素**|なし|  
  
## <a name="remarks"></a>解説  
 **DatabaseToConnect** は、データベース エンジン チューニング アドバイザーがチューニング セッションの開始時に最初に接続するデータベースの名前を指定するために使用します。 この要素では、データベースを 1 つだけ指定できます。 複数のデータベース名が指定されていると、データベース エンジン チューニング アドバイザーはエラーを返します。  
  
## <a name="example"></a>例  
 使用例については、「[インライン ワークロードを指定した XML 入力ファイルのサンプル &#40;DTA&#41;](../../tools/dta/xml-input-file-sample-with-inline-workload-dta.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [XML 入力ファイル リファレンス &#40;データベース エンジン チューニング アドバイザー&#41;](../../tools/dta/xml-input-file-reference-database-engine-tuning-advisor.md)  
  
  

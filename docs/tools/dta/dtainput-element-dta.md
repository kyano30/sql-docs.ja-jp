---
title: DTAInput 要素 (DTA)
description: dta ユーティリティでは、DTAInput 要素にデータベース エンジン チューニング アドバイザーに対する XML 入力の定義が含まれます。
ms.prod: sql
ms.prod_service: sql-tools
ms.technology: tools-other
ms.topic: conceptual
dev_langs:
- XML
helpviewer_keywords:
- DTAInput element
ms.assetid: 40c19abf-ded5-43de-be96-5b43b1b81b03
author: markingmyname
ms.author: maghan
ms.reviewer: ''
ms.custom: seo-lt-2019
ms.date: 03/01/2017
ms.openlocfilehash: d954f229bae8db22abdfb034d950dd96c54bf706
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "85786011"
---
# <a name="dtainput-element-dta"></a>DTAInput 要素 (DTA)

 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

データベース エンジン チューニング アドバイザーに対する XML 入力の定義が含まれます。  
  
## <a name="syntax"></a>構文  
  
```  
  
<DTAXML>  
    <DTAInput>  
    ...code removed here...  
    </DTAInput>  
```  
  
## <a name="element-characteristics"></a>要素の特性  
  
|特性|説明|  
|---------------------|-----------------|  
|**データ型と長さ**|[なし] :|  
|**既定値**|[なし] :|  
|**個数**|**DTAXML** 要素につき 1 回 (省略可)。|  
  
## <a name="element-relationships"></a>要素の関係  
  
|リレーションシップ|要素|  
|------------------|--------------|  
|**親要素**|[DTAXML 要素 &#40;DTA&#41;](../../tools/dta/dtaxml-element-dta.md)|  
|**子要素**|[Server 要素 &#40;DTA&#41;](../../tools/dta/server-element-dta.md)<br /><br /> [Workload 要素 &#40;DTA&#41;](../../tools/dta/workload-element-dta.md)<br /><br /> [TuningOptions 要素 &#40;DTA&#41;](../../tools/dta/tuningoptions-element-dta.md)<br /><br /> [Configuration 要素 &#40;DTA&#41;](../../tools/dta/configuration-element-dta.md)|  
  
## <a name="remarks"></a>解説  
 この要素は、データベース エンジン チューニング アドバイザーの入力スキーマ階層のルートです。 データベース エンジン チューニング アドバイザーへの入力としては、チューニング対象のデータベースのサーバー、ワークロード、チューニング オプション、ユーザー指定の構成などを指定した引数を使用できます。  
  
## <a name="example"></a>例  
 **DTAInput** 要素の使用例については、「[XML 入力ファイルの簡単なサンプル &#40;DTA&#41;](../../tools/dta/simple-xml-input-file-sample-dta.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [XML 入力ファイル リファレンス &#40;データベース エンジン チューニング アドバイザー&#41;](../../tools/dta/xml-input-file-reference-database-engine-tuning-advisor.md)  
  
  

---
description: fn_cdc_has_column_changed (Transact-sql)
title: fn_cdc_has_column_changed (Transact-sql) |Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.fn_cdc_has_column_changed_TSQL
- sys.fn_cdc_has_column_changed
- fn_cdc_has_column_changed_TSQL
- fn_cdc_has_column_changed
dev_langs:
- TSQL
helpviewer_keywords:
- sys.fn_cdc_has_column_changed
- fn_cdc_has_column_changed
ms.assetid: 2b9e6278-050d-4ffc-8d1a-09606180facc
author: rothja
ms.author: jroth
ms.openlocfilehash: b89b4a42df7e0f1481d55fb7d011e947d3e12cf3
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2020
ms.locfileid: "88322018"
---
# <a name="sysfn_cdc_has_column_changed-transact-sql"></a>fn_cdc_has_column_changed (Transact-sql)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  指定した更新マスクが、関連付けられている変更行で指定した列が更新されたことを示すかどうかを識別します。  
  
 ![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>構文  
  
```  
  
sys.fn_cdc_has_column_changed ( 'capture_instance','column_name' , update_mask )  
```  
  
## <a name="arguments"></a>引数  
 **'** *capture_instance* **'**  
 キャプチャ インスタンスの名前を指定します。 *capture_instance* は **sysname**です。  
  
 **'** *column_name* **'**  
 指定したキャプチャ インスタンスのレポート対象となるキャプチャ対象列を指定します。 *column_name* は **sysname**です。  
  
 *update_mask*  
 関連する変更行の更新された列を識別するマスクを指定します。 *update_mask* は **varbinary (128)** です。  
  
## <a name="return-type"></a>戻り値の型  
 **bit**  
  
## <a name="remarks"></a>解説  
 この関数を使用すると、変更データのクエリで返された更新マスクから情報を抽出できます。 これは、関連する変更行の特定の列が変更されているかどうかを知る必要がある場合に、更新マスクを後処理するときに最も役立ちます。 詳細については、「[変更データ キャプチャについて &#40;SQL Server&#41;](../../relational-databases/track-changes/about-change-data-capture-sql-server.md)」を参照してください。  
  
 この情報が変更データクエリの一部として返される場合は、この関数の代わりに、関数 [sys. fn_cdc_get_column_ordinal](../../relational-databases/system-functions/sys-fn-cdc-get-column-ordinal-transact-sql.md) と [sys. fn_cdc_is_bit_set](../../relational-databases/system-functions/sys-fn-cdc-is-bit-set-transact-sql.md) を使用することをお勧めします。 必要な列序数が 1 回しか計算されないようにするために、変更データを照会する前に fn_cdc_get_column_ordinal 関数を使用します。 クエリ内で fn_cdc_is_bit_set を使用して、返された各行の更新マスクから情報を抽出します。  
  
## <a name="permissions"></a>アクセス許可  
 Sysadmin 固定サーバーロールまたは db_owner 固定データベースロールのメンバーシップが必要です。 他のすべてのユーザーに対して、ソーステーブルのすべてのキャプチャ対象列に対する SELECT 権限が必要です。また、キャプチャインスタンスのゲートロールが定義されている場合は、そのデータベースロールのメンバーシップが必要です。  
  
## <a name="see-also"></a>参照  
 [cdc. &#60;capture_instance&#62;_CT &#40;Transact-sql&#41;](../../relational-databases/system-tables/cdc-capture-instance-ct-transact-sql.md)   
 [cdc. captured_columns &#40;Transact-sql&#41;](../../relational-databases/system-tables/cdc-captured-columns-transact-sql.md)  
  
  

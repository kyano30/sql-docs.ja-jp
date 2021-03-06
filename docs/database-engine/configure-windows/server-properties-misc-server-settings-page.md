---
title: サーバーのプロパティ ([その他のサーバーの設定] ページ) | Microsoft Docs
description: SQL Server のサーバー設定について説明します。 新しいユーザーの既定の言語、クエリのタイムアウトなどの動作を制御するオプションについて説明します。
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ''
ms.technology: configuration
ms.topic: conceptual
f1_keywords:
- sql13.swb.serverproperties.miscserversettings.f1
ms.assetid: b170c066-30cd-42dd-8d34-aa129ea09551
author: markingmyname
ms.author: maghan
ms.openlocfilehash: cd0f964c344901da4309605949ecb31d8c893adc
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "85726609"
---
# <a name="server-properties---misc-server-settings-page"></a>[サーバーのプロパティ] - [その他のサーバーの設定] ページ
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  このページを使用すると、サーバーの設定を表示したり、変更したりできます。  
  
## <a name="options"></a>Options  
 **[ユーザーの既定の言語]**  
 新しく作成するすべてのログインの既定の言語を指定します。  
  
 **[トリガーによる他のトリガーの起動を許可する]**  
 トリガーによって別のトリガーを起動するアクションを実行するかどうかを制御します。 このオプションをオフにすると、トリガーは別のトリガーによって起動されません。 このオプションをオンにすると、トリガーは最大 32 レベルまで別のトリガーによって起動されます。  
  
 **[クエリの実行時間が長くならないようにクエリ ガバナーを使用する]**  
 クエリを実行する最大時間を指定します。 クエリ コストとは、特定のハードウェア構成でクエリを実行するために必要とされる予測所要時間を秒単位で表したものです。 既定では、クエリ カバナはオフになっており、すべてのクエリは実行が許可されています。 このオプションをオンにする場合は、下のテキスト ボックスに時間制限を入力する必要があります。 0 以外の正の値を指定すると、クエリ ガバナーは、見積コストがこの値を超えるクエリの実行を許可しません。  
  
 **[2 桁の年を以下の間にある年として解釈]**  
 2 桁の年の値を解釈するために 100 年の日付範囲を指定します。 [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] は、2 桁の日付値を解釈するときに、その 2 桁で終わる年を、指定された範囲の中から参照します。  
  
 右のボックスで終了年を設定します。 終了年が保存されると、 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] の左のボックスに自動的に開始年が入力されます。  
  
 **[構成した値]**  
 このペインの各オプションに構成されている値を表示します。 これらの値を変更した場合は、 **[実行中の値]** をクリックして、変更後の値が反映されているかどうかを確認してください。 値が反映されていない場合は、先に [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] のインスタンスを再指定する必要があります。  
  
 **[実行中の値]**  
 このペイン上のオプションの、現在実行中の値を表示します。 これらの値は読み取り専用です。  
  
## <a name="see-also"></a>参照  
 [サーバー構成オプション &#40;SQL Server&#41;](../../database-engine/configure-windows/server-configuration-options-sql-server.md)  
  
  

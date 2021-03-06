---
title: プラン ガイドへのクエリ ヒントのアタッチ | Microsoft Docs
description: クエリ ヒントは、有効なものであれば、任意の組み合わせでプラン ガイドに使用できます。 SQL Server でプラン ガイドにヒントをアタッチする方法について説明します。
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: performance
ms.topic: conceptual
ms.assetid: 2131f796-6359-4f9e-9047-da0b3d4dedaf
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 6d2980803fb7a3361d74ccd86c0bcef4da734317
ms.sourcegitcommit: 0e0cd9347c029e0c7c9f3fe6d39985a6d3af967d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2020
ms.locfileid: "96505390"
---
# <a name="attach-query-hints-to-a-plan-guide"></a>プラン ガイドへのクエリ ヒントのアタッチ
[!INCLUDE [SQL Server Azure SQL Database](../../includes/applies-to-version/sql-asdb.md)]
  クエリ ヒントは、有効なものであれば、任意の組み合わせでプラン ガイドに使用できます。 プラン ガイドをクエリと照合する際、コンパイルや最適化が行われる前に、そのプラン ガイドのヒント句で指定されている OPTION 句がクエリに追加されます。 プラン ガイドと照合するクエリで既に OPTION 句が使用されている場合、クエリ内のクエリ ヒントがプラン ガイドで指定されているクエリ ヒントに置換されます。 ただし、既に OPTION 句が使用されているクエリと照合するプラン ガイドでは、sp_create_plan_guide ステートメントで照合するクエリのテキストを指定するときに、そのクエリの OPTION 句を含める必要があります。 プラン ガイドで指定されたヒントを、クエリの既存のヒントに代わりに使用するのではなく、既存のヒントに追加する場合は、既存のヒントと追加するヒントの両方をプラン ガイドの OPTION 句で指定する必要があります。  
  
> [!CAUTION]  
>  クエリ ヒントの使用方法が正しくないプラン ガイドは、コンパイル、実行、またはパフォーマンスに関する問題の原因になることがあります。 プラン ガイドは、上級開発者とデータベース管理者のみが使用するようにしてください。  
  
## <a name="common-query-hints-used-in-plan-guides"></a>プラン ガイドで使用される一般的なクエリ ヒント  
 通常、プラン ガイドからメリットを得られる可能性があるクエリは、パラメーター ベースのものです。このようなクエリはキャッシュされたクエリ プランを使用しますが、最悪のシナリオや最も典型的なシナリオにパラメーター値が対応していないために、クエリのパフォーマンスが低くなることがあります。 この問題に対処するのに、OPTIMIZE FOR クエリ ヒントと RECOMPILE クエリ ヒントを使用できます。 OPTIMIZE FOR は、クエリの最適化時にパラメーターに特定の値を使用するように [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] に指示するクエリ ヒントです。 RECOMPILE は、クエリ プランを実行後に破棄し、次に同じクエリが実行されるときに、クエリ オプティマイザーにより新しいクエリ プランに強制的に再コンパイルされるようにサーバーに指示するクエリ ヒントです。 例については、「 [プラン ガイド](../../relational-databases/performance/plan-guides.md)」を参照してください。  
  
 また、INDEX、FORCESCAN、および FORCESEEK のテーブル ヒントをクエリ ヒントとして指定できます。 クエリ ヒントとして指定すると、これらのヒントはインライン テーブルまたはビュー ヒントと同じように動作します。 INDEX ヒントは、指定したインデックスのみを使用して、参照されているテーブルやビューのデータにアクセスするよう、クエリ オプティマイザーに指示します。 FORCESEEK ヒントは、インデックスのシーク操作のみを使用して参照先テーブルやビューのデータにアクセスするよう、オプティマイザーに指示します。 これらのヒントによってプラン ガイド機能が拡張され、プラン ガイドを使用するクエリをさらに最適化することができます。  
  
  

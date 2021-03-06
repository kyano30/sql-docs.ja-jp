---
title: 階層
description: 階層は、類似したメンバーをグループ化し、マスターデータサービスでレポートと分析のためにメンバーを統合/要約するために使用できるツリー構造です。
ms.custom: ''
ms.date: 04/01/2016
ms.prod: sql
ms.prod_service: mds
ms.reviewer: ''
ms.technology: master-data-services
ms.topic: conceptual
helpviewer_keywords:
- hierarchies [Master Data Services]
- hierarchies [Master Data Services], about hierarchies
ms.assetid: 70dbb1fc-ead7-45be-9552-a45e3ccd8d21
author: lrtoyou1223
ms.author: lle
ms.openlocfilehash: 5990a9f60700f034c372bf74382908b261a43608
ms.sourcegitcommit: 6be9a0ff0717f412ece7f8ede07ef01f66ea2061
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "85812731"
---
# <a name="hierarchies-master-data-services"></a>階層 (Master Data Services)

[!INCLUDE [SQL Server - Windows only ASDBMI  ](../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)]の階層とは、次の処理に使用できるツリー構造です。  
  
-   編成を目的として、類似するメンバーをグループ化する。  
  
-   レポートと分析のために、メンバーを統合し集計する。  
  
## <a name="what-hierarchies-contain"></a>階層の内容  
 各階層には、1 つ以上のエンティティのメンバーが含まれます。 メンバーを追加、変更、または削除すると、すべての階層が更新されます。 これにより、すべての階層でデータの正確さが確保されます。 また、階層を使用すると、各メンバーが 1 回だけカウントされるようにすることができます。  
  
 メンバーのサブセットのグループを作成する場合は、コレクションの使用を検討してください。 詳細については、「 [コレクション (マスター データ サービス)](../master-data-services/collections-master-data-services.md)」を参照してください。  
  
## <a name="kinds-of-hierarchies"></a>階層の種類  
 さまざまな方法でメンバーを表示したり編成したりするために、複数の階層を作成できます。 次の階層を作成できます。  
  
-   明示的階層と呼ばれる、単一エンティティから作成される不規則階層。 詳細については、「 [明示的階層 (マスター データ サービス)](../master-data-services/explicit-hierarchies-master-data-services.md)」を参照してください。  
  
-   派生階層と呼ばれる、複数のエンティティと属性間の既存のリレーションシップに基づいて作成されるレベル ベースの階層。 詳細については、「 [派生階層 (マスター データ サービス)](../master-data-services/derived-hierarchies-master-data-services.md)」を参照してください。  
  
> [!NOTE]  
>  階層内のすべてのメンバーは、同じモデル内に含める必要があります。  
  
## <a name="hierarchies-are-not-taxonomies"></a>階層と分類の相違  
 階層は分類とは異なります。 分類ではメンバーを一度に複数の属性で編成しますが、階層ではメンバーを一度に 1 つの属性で編成します。 分類には同じメンバーを複数回含めることができますが、階層には一度しか含めることができません。  
  
 たとえば、分類には同じ自転車を 2 回含めることができます。つまり、一度は赤色という理由で、もう一度はサイズが 38 という理由で含めることができます。 階層には、自転車は一度しか含められないので、色かサイズのどちらの関連で示すかを決定する必要があります。  
  
## <a name="hierarchy-example"></a>階層の例  
 次の例では、製品メンバーはサブカテゴリ メンバーごとにグループ化されます。  
  
 ![サブカテゴリごとにグループ化された階層の例](../master-data-services/media/mds-conc-hierarchy.gif "サブカテゴリごとにグループ化された階層の例")  
  
## <a name="related-tasks"></a>Related Tasks  
  
|タスクの説明|トピック|  
|----------------------|-----------|  
|明示的階層を作成する。|[明示的階層を作成する (マスター データ サービス)](../master-data-services/create-an-explicit-hierarchy-master-data-services.md)|  
|派生階層を作成する。|[派生階層を作成する (マスター データ サービス)](../master-data-services/create-a-derived-hierarchy-master-data-services.md)|  
|既存の派生階層のレベルを非表示にするか、または削除する。|[派生階層のレベルを非表示にするか削除する (マスター データ サービス)](../master-data-services/hide-or-delete-levels-in-a-derived-hierarchy-master-data-services.md)|  
  
## <a name="related-content"></a>関連コンテンツ  
  
-   [明示的階層 (マスター データ サービス)](../master-data-services/explicit-hierarchies-master-data-services.md)  
  
-   [派生階層 (マスター データ サービス)](../master-data-services/derived-hierarchies-master-data-services.md)  
  
-   [再帰型階層 (マスター データ サービス)](../master-data-services/recursive-hierarchies-master-data-services.md)  
  
-   [明示的なキャップを持つ派生階層 (マスター データ サービス)](../master-data-services/derived-hierarchies-with-explicit-caps-master-data-services.md)  
  
-   [コレクション (マスター データ サービス)](../master-data-services/collections-master-data-services.md)  
  
  

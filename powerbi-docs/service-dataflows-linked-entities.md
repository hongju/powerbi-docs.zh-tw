---
title: 連結 Power BI 中資料流程之間的實體
description: 了解如何連結 Power BI 中資料流程內的實體
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 11/06/2018
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: b69b84c7c61227ef7a827722c86f54100bd2f3b7
ms.sourcegitcommit: b23fdcc0ceff5acd2e4d52b15b310068236cf8c7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51266835"
---
# <a name="link-entities-between-dataflows-in-power-bi-preview"></a>連結 Power BI 中資料流程之間的實體 (預覽)

使用 Power BI 中的資料流程，您就會有單一組織性資料儲存體來源，商務分析師只要一次準備及管理好他們的資料，就可以在組織內的不同分析應用程式之間重複使用。 

當您連結資料流程之間的實體時，可以重複使用已由其他人擁有的資料流程所內嵌、清理及轉換的實體，不需要維護該資料。 連結實體只會指向其他資料流程中的實體，而且*不*會複製或複寫資料。

![Power BI 中的連結實體](media/service-dataflows-linked-entities/linked-entities_00.png)

連結實體是**唯讀**的。 如果您想要為連結實體建立轉換，必須建立具有對已連結實體之參照的新計算實體。

## <a name="linked-entity-availability"></a>連結實體可用性

連結實體需要重新整理 [Power BI Premium](service-premium.md) 訂用帳戶。 您可以在裝載於 Power BI Premium 容量之工作區上的任何資料流程中使用連結實體。 來源資料流程沒有任何限制。

連結實體只能在新的 Power BI 工作區中正常運作。 您可以深入了解[新 Power BI 工作區](service-create-the-new-workspaces.md)。 所有連結資料流程都必須位於新的工作區，才能正常運作。

## <a name="how-to-link-entities-between-dataflows"></a>如何在資料流程之間連結實體

有幾個方式可以連結 Power BI 中資料流程之間的實體。 您可以從資料流程製作工具選取 [新增已連結實體]，如下圖所示。 

![Power BI 中的連結實體](media/service-dataflows-linked-entities/linked-entities_00.png)

您也可以從 Power BI 服務中的 [新增實體] 功能表項目選取 [新增已連結實體]。

![Power BI 中的連結實體](media/service-dataflows-linked-entities/linked-entities_01.png)

若要連結實體，必須使用您的 Power BI 認證登入。

此時會開啟 [Navigator] 視窗，讓您選擇一組可以連接的實體。 顯示的實體是您在您的 Power BI 租用戶中跨所有工作區擁有權限的實體。 

一旦選取您的連結實體，它們會出現在製作工具中您資料流程的實體清單中，並且會有可識別它們是連結實體的特殊圖示。

您也可以從連結實體的資料流程設定檢視來源資料流程。

## <a name="refresh-logic-of-linked-entities"></a>重新整理連結實體的邏輯
連結實體的預設重新整理邏輯會根據來源資料流程是否位於和目的地資料流程相同的工作區而變更。 下列各節會輪番說明每個行為。

### <a name="links-between-workspaces"></a>工作區之間的連結

重新整理不同工作區中實體連結的運作行為類似於外部資料來源。 重新整理資料流程時，會從來源資料流程取得實體的最新資料。 如果重新整理來源資料流程，它不會自動影響目的地資料流程中的資料。

### <a name="links-in-the-same-workspace"></a>相同工作區中的連結

重新整理來源資料流程的資料時，該事件會自動觸發相同工作區中所有目的地資料流程內相依實體的重新整理程序，包括以它們為依據的任何計算實體。 目的地資料流程中的所有其他實體都會根據資料流程排程重新整理。 相依於多個來源的實體會在它們的任何來源順利更新時，更新它們的資料。

建議您一次就確認個重新整理程序。 如此一來，如果目的地資料流程重新整理失敗，重新整理來源資料流程也會失敗。

## <a name="permissions-when-viewing-reports-from-dataflows"></a>檢視來自資料流程的報表時的權限

建立 Power BI 報表 (包括以資料流程為基礎的資料) 時，使用者只會在擁有來源資料流程的存取權時，才能看到任何連結實體。

## <a name="limitations-and-considerations"></a>限制與考量

使用連結實體時，需記住幾個限制：

* 最多只能有 5 個參考躍點
* 不允許連結實體循環相依性
* 資料流程必須位於[新的 Power BI 工作區](service-create-the-new-workspaces.md)中


## <a name="next-steps"></a>後續步驟

在您建立或使用資料流程時，下列文章可能會很有用。 

* [Power BI 中的自助資料準備 (預覽)](service-dataflows-overview.md)
* [在 Power BI 中建立及使用資料流程](service-dataflows-create-use.md)
* [在 Power BI Premium 中使用計算實體 (預覽)](service-dataflows-computed-entities-premium.md)
* [搭配內部部署資料來源使用資料流程 (預覽)](service-dataflows-on-premises-gateways.md)
* [適用於 Power BI 資料流程的開發人員資源 (預覽)](service-dataflows-developer-resources.md)

如需 Power Query 和排程重新整理的詳細資訊，您可以閱讀下列文章：
* [Power BI Desktop 中的查詢概觀](desktop-query-overview.md)
* [設定排定的重新整理](refresh-scheduled-refresh.md)

如需 Common Data Service 的詳細資訊，您可以閱讀它的概觀文章：
* [Common Data Service - 概觀](https://docs.microsoft.com/powerapps/common-data-model/overview)

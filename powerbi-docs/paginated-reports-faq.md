---
title: Power BI 中的編頁報表：常見問題集 (預覽)
description: 此文章將回答有關編頁報表的常見問題集。 這些報表均為已高度格式化且具完美像素的輸出，並已基於列印或產生 PDF 用途進行最佳化。
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: overview
ms.date: 11/05/2018
ms.openlocfilehash: cedf72585d7aa4f2ece39739dc0bdba33ca66e21
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "60987777"
---
# <a name="paginated-reports-in-power-bi-faq-preview"></a>Power BI 中的編頁報表：常見問題集 (預覽)

此文章將回答有關編頁報表的常見問題集。 這些報表均為已高度格式化且具完美像素的輸出，並已基於列印或產生 PDF 用途進行最佳化。 它們稱為「編頁」，因為已將它們格式化，使其可適當地符合多個頁面。 編頁報表會以 SQL Server Reporting Services 中的 RDL 報表技術為基礎。 

此文章將回答人們關於 Power BI Premium 中的編頁報表，以及關於報表產生器 (此為用來製作編頁報表的單獨工具) 的許多常見問題。 您需要 Power BI Pro 授權，才能將報表發佈至服務。 只要工作區位於 Power BI Premium 容量，您就可以在 [我的工作區] 或應用程式工作區中發佈及共用編頁報表。 

## <a name="administration"></a>系統管理

### <a name="what-size-premium-capacity-do-i-need-for-paginated-reports"></a>我需要針對編頁報表使用何種大小的 Premium 容量？

編頁報表工作負載可在適用於公開預覽的 P1 - P3 SKU 上使用。  您也可以將它用於具有 A4 - A6 SKU 的測試/開發人員案例。

### <a name="what-is-the-maximum-memory-threshold-i-can-put-for-paginated-reports-in-my-capacity"></a>我可以在容量中針對編頁報表放置的記憶體閾值上限為何？

您目前可能只能針對此工作負載保留 50% 的記憶體。 

### <a name="how-does-user-access-work-for-paginated-reports"></a>使用者存取如何針對編頁報表運作？

對於編頁報表的使用者存取，與 Power BI 服務中對於所有其他內容的使用者存取相同。 

### <a name="how-do-i-turn-onoff-my-paginated-reports-workload"></a>如何開啟/關閉我的編頁報表工作負載？

容量管理員可以在容量管理員入口網站頁面中，啟用或停用編頁報表工作負載。  

### <a name="how-can-i-monitor-usage-of-paginated-reports-in-my-tenant"></a>如何在租用戶中監視編頁報表的使用情況？

Office 365 稽核記錄會在下列事件下方，詳述此報表類型的使用情況： 

- 檢視 Power BI 報表
- 刪除 Power BI 報表
- 建立 Power BI 報表
- 下載 Power BI 報表

相對於 Power BI 報表，ReportType 欄位含有可識別已編頁的值 “PaginatedReport”。

此外，稽核記錄還會針對編頁報表提供下列事件：

- 已將 Power BI 資料集繫結至閘道
- 探索 Power BI 資料來源
- TakeOverDatasource

### <a name="can-i-monitor-this-workload-through-the-premium-capacity-monitoring-app"></a>我可以透過 Premium 容量監視應用程式來監視此工作負載嗎？

您可以透過新索引標籤使用監視功能，其中含有您 Power BI 資料集擁有的相同相關詳細資料。

### <a name="do-i-need-a-pro-license-to-create-and-publish-paginated-reports"></a>我需要 Pro 授權，才能建立並發佈報表嗎？

是。 如果沒有 Pro 授權，您就無法將報表上傳至工作區。 我們建議您下載並使用 Power BI 報表產生器，即使沒有 Pro 授權，但您無法發佈您建立沒有它的編頁的報表。 

### <a name="what-if-i-have-a-paginated-report-in-a-workspace-and-the-paginated-report-workload-is-turned-off"></a>如果我在工作區中具有編頁報表，而編頁報表工作負載已關閉，該怎麼辦？

您會收到錯誤訊息，而且在重新開啟工作負載之前，將無法檢視報表。 您仍然可以從工作區刪除報表。

### <a name="what-is-the-default-memory-for-each-of-the-premium-skus-supported-for-paginated-reports"></a>針對編頁報表支援的每個 Premium SKU 的預設記憶體為何？

適用於編頁報表之每個 Premium SKU 中的預設記憶體：

- **P1/A4**：20% 預設值；10% 最小值
- **P2/A5**：20% 預設值；5% 最小值
- **P3/A6**：20% 預設值；2.5% 最小值

## <a name="general"></a>一般

### <a name="when-should-i-use-a-paginated-report-vs-a-power-bi-report"></a>何時應使用編頁報表與 Power BI 報表？

如果案例需要已高度格式化且具完美像素的輸出，並已基於列印或產生 PDF 用途進行最佳化，則最適合使用編頁報表。  損益表就是一個您可能想要建立來作為編頁報表之報表類型的良好範例。  

Power BI 報表已針對探索和互動進行最佳化。  銷售報表可讓不同的銷售人員針對其特定區域/產業/客戶，在同一份報表中為資料進行配量，並查看數字如何變化，而此報表最好透過 Power BI 報表來提供。

### <a name="the-documentation-says-power-bi-report-builder-is-the-preferred-authoring-tool-can-i-create-paginated-reports-in-sql-server-data-tools-for-power-bi"></a>說明文件指出 Power BI 報表產生器是慣用的撰寫工具。 我可以在適用於 Power BI 的 SQL Server Data Tools 中建立編頁報表嗎？

是，但 Power BI 服務僅允許您一次上傳單一項目，因此，尚不支援製作者搭配 SQL Server Data Tools (SSDT) 使用的許多案例。 請參閱稍後可在此常見問題集中取得的完整[不支援功能清單](#what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi)。  

### <a name="what-versions-of-report-builder-do-you-support"></a>您支援哪些版本的報表產生器？

我們最近發行 Power BI 報表產生器，為主要的撰寫工具，在 Power BI 服務中的編頁報表。 安裝[Power BI 報表產生器，從 Microsoft 下載中心取得](https://go.microsoft.com/fwlink/?linkid=2086513)。

### <a name="how-do-i-move-existing-reports-i-have-saved-in-sql-server-reporting-services-to-power-bi"></a>如何將已儲存於 SQL Server Reporting Services 中的現有報表移至 Power BI？

您需要從伺服器下載報表，然後透過入口網站將它上傳至 Power BI。  目前並未提供任何移轉工具，但我們正在考慮要在完成公開預覽，並在產品之間取得功能同位的正確層級之後建立一個。

### <a name="can-i-open-reports-and-publish-directly-to-the-service"></a>我可以開啟報表並直接發佈至服務嗎？

目前不行。 我們將新增開啟報表，和它們直接發行至服務從 Power BI 報表產生器之前 GA，您可以使用 Power BI Desktop 的支援。

### <a name="what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi"></a>在 Power BI 中，目前尚未支援 SSRS 中的哪些編頁報表功能？

編頁報表目前不支援下列項目：

- 共用資料來源
- 共用資料集
- 子報表
- 點選連結與鑽研動作
- 連結的報表
- 書籤
- Bing 地圖圖層
- 自訂字型

如果您嘗試上傳的檔案具有 Power BI 服務中不支援的功能 (切換/排序以外的功能)，就會收到錯誤訊息。

### <a name="what-data-sources-do-you-support-currently-for-paginated-reports"></a>您目前針對編頁報告支援哪些資料來源？

我們支援下列資料來源- 

- Power BI Premium 的資料集
- Azure Analysis Services （透過單一登入 (SSO)）
- Azure SQL Database
- SQL Server*
- SQL Server Analysis Services (SSAS) 表格式 (DAX) 和多維度 (MDX) 模型 * 
- Oracle* 
- Teradata * 

* 需要內部部署閘道。

透過閘道存取 SSAS 時，已儲存認證的使用者需要在 SSAS 中提高權限，才能透過閘道運作。

### <a name="what-authentication-methods-do-you-support"></a>您支援哪些驗證方法？

我們會支援 Azure Analysis Services 和 Power BI Premium 的資料來源的 SSO。  對於所有其他資料來源，您目前需要儲存在入口網站或閘道的使用者名稱和密碼，與資料來源。  

### <a name="can-i-use-a-power-bi-dataset-as-a-data-source-for-my-paginated-report"></a>我可以使用 Power BI 資料集作為編頁報表的資料來源嗎？

是，我們現在支援 Power BI Premium 的資料集做為您的編頁報表的資料來源。

### <a name="can-i-use-stored-procedures-through-the-gateway"></a>我可以透過閘道使用預存程序嗎？

您可以透過閘道來使用預存程序，不過如果預存程序有參數，在某些情況下可能會遇到一些問題。

### <a name="what-export-formats-are-available-for-my-report-in-the-power-bi-service"></a>在 Power BI 服務中，哪些匯出格式可供我的報表使用？

您可以匯出至 Microsoft Excel、Microsoft Word、Microsoft PowerPoint、PDF、.CSV、XML 和 MHTML。

### <a name="can-i-print-paginated-reports"></a>我可以列印編頁報表嗎？

列印功能是供編頁報表，包括全新和改進的列印預覽體驗。 

### <a name="are-e-mail-subscriptions-available-yet-for-paginated-reports"></a>可以針對編頁報表提供電子郵件訂閱嗎？

不可以，不過後續將會推出電子郵件訂閱。

### <a name="what-features-from-ssrs-will-you-be-supporting-in-the-power-bi-service"></a>您將在 Power BI 服務中支援哪些來自 SSRS 的功能？

我們的計劃是在大多數情況下提供功能同位，但為了符合現有 SSRS 模式而嘗試變更 SSRS 與 Power BI 的特定項目，可能不具任何意義。  舉例而言，Power BI 中的不同權限模型無法對應回 SSRS。  我們會尋求客戶和合作夥伴的意見反應來進行這類決策。

### <a name="can-i-run-custom-code-in-my-report"></a>我可以在報表中執行自訂程式碼嗎？

是，我們支援在報表中執行程式碼的功能，就像您可以在 SSRS 中所做的。

### <a name="does-this-mean-ssrs-is-going-away"></a>這表示 SSRS 即將淘汰嗎？

完全不是這個意思。  這個新的供應項目會針對客戶的編頁報表，為客戶提供雲端式選項。  

### <a name="can-i-use-power-bi-embedded-to-embed-my-paginated-reports-into-an-app-im-hosting"></a>我可以使用 Power BI Embedded，將編頁報表內嵌到我代管的應用程式嗎？

我們計劃使用現有的 Power BI API 來支援此案例，但還沒有此案例何時可供使用的時間表。

### <a name="can-i-drill-through-from-a-power-bi-report-to-a-paginated-report"></a>我可以從 Power BI 報表鑽研至編頁報表嗎？

還不行，但我們絕對有計畫要支援此案例。

### <a name="can-i-share-my-paginated-report-content-through-a-power-bi-app"></a>我可以透過 Power BI 應用程式共用編頁報表的內容嗎？

是，編頁的報表支援從 v1 與 v2 的工作區的應用程式一起部署。 

### <a name="will-other-report-specific-features-in-power-bi-like-pinning-to-report-tiles-to-dashboards-work-with-paginated-reports"></a>Power BI 中的其他報表特有功能 (例如，將報表磚釘選到儀表板) 將能搭配編頁報表來運作嗎？

我們計畫要讓報表盡可能地支援服務中相同的主要案例。  在理想的情況下，雖然用來製作它們的工具不同，但從取用者觀點來看，它只是他們在入口網站之清單中的另一份報表。 他們不在意建立它的方式，他們可以完成所需的作業。  此功能同位有個很好的範例就是計劃性的註解支援。 儘管功能本身針對每個報表類型的運作方式可能稍有不同，但您還是能夠針對這兩者使用註解。

### <a name="is-a-migration-tool-planned-so-ssrs-customers-can-move-their-existing-reports-and-assets-to-power-bi"></a>是否規劃了移轉工具，讓 SSRS 客戶可將其現有的報表和資產移至 Power BI？

我們會繼續評估選項，以透過自動化的方式，將內容移至 Power BI，但這會在正式運作時才提供。

### <a name="will-i-ever-be-able-to-create-both-paginated-reports-and-power-bi-reports-in-a-single-authoring-tool"></a>我是否能夠在單一製作工具中同時建立編頁報表和 Power BI 報表？

未來有可能。  我們目前正在思考可以實現這個案例的方法，也在研究要以單一 BI 套件形式一併散發多個製作工具，還是提供個別下載/商標。

### <a name="is-there-a-report-viewer-control-for-paginated-reports-in-the-power-bi-service"></a>Power BI 服務中是否有適用於編頁報表的報表檢視器控制項？

否，目前尚未提供報表檢視器控制項。

### <a name="can-you-search-for-paginated-reports-from-the-new-home-experience-in-the-power-bi-service"></a>您可以從 Power BI 服務中的新 [常用] 體驗搜尋編頁報表嗎？

否，您目前無法從 [常用] 搜尋編頁報表。  不過，您可以在新 [常用] 體驗的其他部分中看見它們。

## <a name="next-steps"></a>後續步驟

- [從 Microsoft 下載中心安裝 Power BI 報表產生器](https://go.microsoft.com/fwlink/?linkid=2086513)
- [教學課程：建立編頁報表](paginated-reports-quickstart-aw.md)

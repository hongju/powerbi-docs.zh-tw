---
title: Power BI 設計工具的儀表板磚簡介
description: Power BI 中儀表板磚的所有相關資訊。 這包括從 SQL Server Reporting Services (SSRS) 報表建立的磚。
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 11/21/2018
ms.author: maggies
LocalizationGroup: Dashboards
ms.openlocfilehash: c8b5728c951bc1a25e71da8885997814c5485cd4
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "61138711"
---
# <a name="intro-to-dashboard-tiles-for-power-bi-designers"></a>Power BI 設計工具的儀表板磚簡介

圖格是您釘選到儀表板的資料快照。 您可以從報表、資料集、儀表板、問與答方塊、Excel 和 SQL Server Reporting Services (SSRS) 報表等來建立磚。  這個螢幕擷取畫面顯示許多釘選到儀表板的不同磚。

![Power BI 儀表板](media/service-dashboard-tiles/power-bi-dashboard.png)

儀表板和儀表板磚是 Power BI 服務的功能，而不是 Power BI Desktop 的功能。 您無法在行動裝置上建立儀表板，但可以在該處[檢視和共用](mobile-apps-view-dashboard.md)儀表板。

除了釘選，您也可以使用[新增磚](service-dashboard-add-widget.md)直接在儀表板上建立獨立的磚。 獨立磚包括：文字方塊、影像、視訊、串流資料和 Web 內容。

您想要了解構成 Power BI 的建置組塊嗎？  請參閱 [Power BI - 基本概念](service-basic-concepts.md)。

> [!NOTE]
> 如果用來建立圖格的原始視覺效果有了變更，也不會改變圖格。  例如，如果您已從報表釘選折線圖，然後將折線圖變更為長條圖，則儀表板磚仍會顯示折線圖。 資料會重新整理，但視覺效果類型不會。
> 
> 

## <a name="pin-a-tile-from"></a>釘選圖格，從...
有很多不同的方式，可以將磚新增 (釘選) 至儀表板。 磚的釘選來源：

* [Power BI 問與答](service-dashboard-pin-tile-from-q-and-a.md)
* [報表](service-dashboard-pin-tile-from-report.md)
* [其他儀表板](service-pin-tile-to-another-dashboard.md)
* [商務用 OneDrive 上的 Excel 活頁簿](service-dashboard-pin-tile-from-excel.md)
* [Power BI Publisher for Excel](publisher-for-excel.md)
* [Quick Insights (深入資訊摘要)](service-insights.md)
* [Reporting Services](https://docs.microsoft.com/sql/reporting-services/pin-reporting-services-items-to-power-bi-dashboards)

可以使用[新增磚](service-dashboard-add-widget.md)，直接在儀表板上建立影像、文字方塊、視訊、串流資料和 Web 內容的獨立磚。

  ![新增磚圖示](media/service-dashboard-tiles/add_widgetnew.png)

## <a name="interacting-with-tiles-on-a-dashboard"></a>與儀表板上的圖格互動
### <a name="move-and-resize-a-tile"></a>移動和調整圖格大小
抓取磚並[在儀表板上移動](service-dashboard-edit-tile.md)。 將滑鼠暫留並選取控點 ![控點](media/service-dashboard-tiles/resize-handle.jpg) 以調整圖格大小。

### <a name="hover-over-a-tile-to-change-the-appearance-and-behavior"></a>將滑鼠暫留在圖格上以變更其外觀和行為
1. 將滑鼠暫留在圖格上以顯示省略符號。
   
    ![磚省略符號](media/service-dashboard-tiles/ellipses_new.png)
2. 選取省略符號開啟圖格的 [動作] 功能表。
   
    ![省略符號圖示](media/service-dashboard-tiles/power-bi-tile-menu.png)
   
    從這裡您可以：
   
   * [開啟用於建立此磚的報表](service-reports.md) ![報表圖示](media/service-dashboard-tiles/chart-icon.jpg)  
   
   * [開啟用於建立此磚的工作表](service-reports.md) ![工作表圖示](media/service-dashboard-tiles/power-bi-open-worksheet.png)  
     
    * [以焦點模式檢視](service-focus-mode.md) ![焦點圖示](media/service-dashboard-tiles/fullscreen-icon.jpg)  
     * [匯出磚中所使用的資料](visuals/power-bi-visualization-export-data.md) ![匯出資料圖示](media/service-dashboard-tiles/export-icon.png)
     * [編輯標題和副標題、加入超連](service-dashboard-edit-tile.md) ![編輯圖示](media/service-dashboard-tiles/pencil-icon.jpg)
     * [執行深入解析](service-insights.md) ![深入解析圖示](media/service-dashboard-tiles/power-bi-insights.png)
     * [將磚釘選到另一個儀表板 ](service-pin-tile-to-another-dashboard.md)
       ![釘選圖示](media/service-dashboard-tiles/pin-icon.jpg)
     * [移除磚](service-dashboard-edit-tile.md)
     ![刪除圖示](media/service-dashboard-tiles/trash-icon.png)
3. 若要關閉動作功能表，選取畫布中的空白區域。

### <a name="select-click-a-tile"></a>選取 (按一下) 圖格
當您選取磚時，接下來情況取決於您建立該磚的方式。 此外，如果有[自訂連結](service-dashboard-edit-tile.md)，則選取磚會帶您前往該連結。 否則，選取磚會帶您前往建立此磚所使用的報表、Excel Online 活頁簿、內部部署 Reporting Services 報表或問與答問題。

> [!NOTE]
> 使用 [新增磚]  直接在儀表板上建立的影片圖格為例外。 選取影片磚 (以此方式建立) 會直接在儀表板上播放視訊。   
> 
> 

## <a name="considerations-and-troubleshooting"></a>考量與疑難排解

* 如未儲存建立視覺效果所用的報表，則選取該圖格不會執行任何動作。
* 如果磚是從 Excel Online 的活頁簿建立，您至少需要該活頁簿的讀取權限。 否則，選取磚並不會在 Excel Online 中開啟活頁簿。
* 假設您使用 [新增磚]  直接在儀表板上建立磚，並為其設定自訂超連結。 如此一來，在您選取標題、子標題或磚時，就會開啟該 URL。 否則，當您選取針對影像、Web 程式碼或文字方塊直接在儀表板上建立的磚時，預設不會有任何反應。
* 如果您無權使用 Reporting Services 內的報表，則選取從 Reporting Services 報表建立的磚時會帶您前往一個頁面，指出您沒有存取權 (rsAccessDenied)。
* 如果您無權存取 Reporting Services 伺服器所在的網路，則選取從 Reporting Services 建立的磚時會帶您前往一個頁面，指出找不到伺服器 (HTTP 404)。 您的裝置需要報表伺服器的網路存取權，才能檢視報表。
* 如果用來建立圖格的原始視覺效果有了變更，也不會改變圖格。  例如，您從報表釘選折線圖之後，將折線圖變更為長條圖，儀表板磚會繼續顯示折線圖。 資料會重新整理，但視覺效果類型不會。

## <a name="next-steps"></a>後續步驟
[建立儀表板的卡片 (大數字圖格)](power-bi-visualization-card.md)

[Power BI 中的儀表板](service-dashboards.md)  

[資料重新整理](refresh-data.md)

[Power BI - 基本概念](service-basic-concepts.md)

[將磚匯出至 Power Point](http://blogs.msdn.com/b/powerbidev/archive/2015/09/28/integrating-power-bi-tiles-into-office-documents.aspx)

[將 Reporting Services 項目釘選至 Power BI 儀表板](https://msdn.microsoft.com/library/mt604784.aspx)

有其他問題嗎？ [試試 Power BI 社群](http://community.powerbi.com/)


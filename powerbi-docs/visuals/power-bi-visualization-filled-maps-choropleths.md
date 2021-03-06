---
title: Power BI 中的區域分布圖 (分區著色圖)
description: 有關在 Power BI 中建立區域分布圖 (分級著色圖) 的文件
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 09/27/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: ef03a562351b8f4487e4822ef28b89009ee5cbb4
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "61143552"
---
# <a name="filled-maps-choropleths-in-power-bi"></a>Power BI 中的區域分布圖 (分區著色圖)
區域分布圖使用陰影、濃淡或圖樣，顯示值的比例如何隨著地理位置或地區而有所不同。  可使用範圍介於淺色 (較不常見/較低) 到深色 (較常見/較多) 的陰影，快速顯示這些相對差異。    

![美國地圖](media/power-bi-visualization-filled-maps-choropleths/large_map.png)

## <a name="what-is-sent-to-bing"></a>傳送至 Bing 的項目
Power BI 與 Bing 整合以提供預設地圖座標 (這個程序稱為地理編碼)。 當您在 Power BI 服務或 Power BI Desktop 中建立地圖視覺效果時，[位置]  、[緯度]  和 [經度]  貯體中的資料 (用來建立該視覺效果) 會傳送至 Bing。

您或您的系統管理員可能需要更新防火牆，以允許存取 Bing 用以進行地理編碼的 URL。  這些 URL 是：
- https://dev.virtualearth.net/REST/V1/Locations    
- https://platform.bing.com/geo/spatial/v1/public/Geodata    
- https://www.bing.com/api/maps/mapcontrol

如需有關傳送至 Bing 之資料的詳細資訊，以及提升地理編碼成功率的祕訣，請參閱[地圖視覺效果的祕訣和訣竅](power-bi-map-tips-and-tricks.md)。

## <a name="when-to-use-a-filled-map"></a>使用區域分布圖的時機
區域分布圖極適合：

* 當您要在地圖上顯示量化資訊。
* 當您要顯示空間模式和關聯性。
* 當您的資料已標準化。
* 當您使用的是社會經濟資料。
* 當定義的區域相當重要。
* 當您要取得跨地理位置的分佈概觀。

### <a name="prerequisites"></a>先決條件
- Power BI 服務或 Power BI Desktop
- 銷售與行銷範例

若要跟著做，請留意到本教學課程使用的是 Power BI 服務，而非 Power BI Desktop。

## <a name="create-a-basic-filled-map"></a>建立基本的區域分布圖
在這段影片中，Kim 會建立一個基本地圖，並將其轉換成區域分布圖。

<iframe width="560" height="315" src="https://www.youtube.com/embed/ajTPGNpthcg" frameborder="0" allowfullscreen></iframe>

### <a name="get-data-and-add-a-new-blank-page-to-the-report"></a>取得資料，並將新的空白頁面新增至報表
1. 若要建立您自己的區域分布圖，請[下載銷售與行銷範例](../sample-datasets.md)，方法是登入 Power BI，然後選取 [取得資料] \> [範例] \> [銷售與行銷] \> [連線]  。
2. 出現成功訊息時，關閉它並選取 [報表]  索引標籤。然後選擇 [銷售與行銷範例]  開啟報表。

   ![報表內容清單](media/power-bi-visualization-filled-maps-choropleths/power-bi-content-reports2.png)
3. Power BI 會開啟報表。 選取 [編輯報表]  以在[編輯檢視](../service-interact-with-a-report-in-editing-view.md)中開啟報表。

4. 選取報表畫布底部的黃色加號符號以新增頁面。

    ![[報表] 索引標籤](media/power-bi-visualization-filled-maps-choropleths/power-bi-new-page.png)

### <a name="create-a-filled-map"></a>建立區域分布圖
1. 從 [欄位] 窗格中，選取 [地理]  \> [州]  欄位。    

   ![[狀態] 旁的黃色核取記號](media/power-bi-visualization-filled-maps-choropleths/power-bi-state.png)
5. [將圖表轉換](power-bi-report-change-visualization-type.md)成區域分布圖。 請注意，[州]  現在處於 [位置]  部分。 Bing 地圖服務會使用 [位置]  部分中的欄位來建立地圖。  此位置可以是各種不同的有效位置：國家/地區、州、縣市、城市、郵遞區號或其他郵遞區號等。Bing 地圖服務提供世界各地位置的區域分布圖。 如果 [位置] 部分沒有有效項目，Power BI 就不能建立區域分布圖。  

   ![已醒目提示區域分布圖圖示的範本](media/power-bi-visualization-filled-maps-choropleths/img003.png)
6. 篩選地圖，只顯示美國本土。

   a.  在 [視覺效果] 窗格底部尋找 [篩選]  區域。

   b.  將滑鼠指標暫留在 [州]  ，然後按一下展開Ｖ形箭號  
   ![顯示 [狀態(全部)] 的視覺效果層級篩選](media/power-bi-visualization-filled-maps-choropleths/img004.png)

   c.  在 [全部]  旁邊放置一個核取記號，然後移除 [AK]  旁邊的核取記號。

   ![未選取 [全部] 和 [AK] 的 [狀態] 下拉式清單](media/power-bi-visualization-filled-maps-choropleths/img005.png)
7. 選取 [SalesFact]  \>[人氣]  ，將其新增到 [色彩飽和度]  部分。 [色彩飽和度]  部分的欄位會控制地圖的明暗。  
   ![[色彩飽和度] 欄位區中的 [人氣]](media/power-bi-visualization-filled-maps-choropleths/power-bi-filled-map.png)
8. 區域分布圖會呈綠色，並以紅色代表人氣指數較低，而綠色代表人氣較高、較為正向。  我們在此將懷俄明州 (WY) 反白顯示，發現人氣相當高，達 74。  
   ![顯示狀態和人氣的黑色對話方塊](media/power-bi-visualization-filled-maps-choropleths/power-bi-wy.png)
9. [儲存報表](../service-report-save.md)。
##    <a name="adjust-the-color-formatting"></a>調整色彩格式化
Power BI 提供您眾多對區域分布圖外觀的控制。
1. 選取油漆滾筒圖示來開啟 [格式化] 窗格。

    ![[格式化] 窗格](media/power-bi-visualization-filled-maps-choropleths/power-bi-data-colors.png)

2. 選取 [資料色彩]  以顯示色彩選項。
3. 將最小值和最大值色彩設定為黃色和藍色。 並根據您的資料新增最小值和最大值。 試玩這些控制項，直到獲得您想要的外觀。 

    ![非發散色彩](media/power-bi-visualization-filled-maps-choropleths/power-bi-color.png)

## <a name="highlighting-and-cross-filtering"></a>反白顯示和交叉篩選
如需使用 [篩選] 窗格的資訊，請參閱[將篩選加入報表](../power-bi-report-add-filter.md)。

在區域分布圖中醒目提示位置，會交叉篩選報表頁面上的其他視覺效果，反之亦然。

1. 若要跟著做，請先選取 [檔案] > [儲存]  來儲存此報表。 

2. 使用 CTRL-C 複製區域分布圖。

3. 從報表畫布底部，選取 [人氣]  索引標籤，開啟 [人氣] 報表頁面。

    ![已選取 [人氣] 索引標籤](media/power-bi-visualization-filled-maps-choropleths/power-bi-sentiment-tab.png)

4. 移動並調整頁面上視覺效果的大小以便挪出空間空間，然後按 CTRL-V 從先前的報表貼上區域分布圖。

   ![區域分布圖已新增至 [人氣] 頁面](media/power-bi-visualization-filled-maps-choropleths/power-bi-map.png)

5. 在區域分布圖中選取一個州。  這會反白顯示頁面上的其他視覺效果。 例如，選取 [德州]  ，會顯示人氣為 74，德州位於中央區 \#23。   
   ![已選取 [德州]](media/power-bi-visualization-filled-maps-choropleths/power-bi-texas.png)
2. 選取 [VanArsdel - 依月份的人氣] 折線圖上的資料點。 這樣會篩選區域分布圖，來顯示 VanArsdel 的人氣，而不顯示其競賽的人氣。  
   ![新的陰影](media/power-bi-visualization-filled-maps-choropleths/power-bi-yes.png)

## <a name="considerations-and-troubleshooting"></a>考量與疑難排解
地圖資料可能模稜兩可。  例如，有在法國的巴黎，但也有「德州，巴黎」(Paris, Texas)。 您的地理資料可能會儲存在個別資料行 (縣市名稱的資料行、州或省名稱的資料行等等)，所以 Bing 可能無法判斷這裡的巴黎是哪個巴黎。 如果您的資料集已經包含經度和緯度資料，Power BI 有特殊欄位可協助避免地圖資料模稜兩可。 直接將包含緯度資料的欄位拖曳到 [視覺效果] \> [緯度] 區域。  然後對經度資料執行相同的動作。    

![[視覺效果] 和 [欄位] 窗格](media/power-bi-visualization-filled-maps-choropleths/pbi_latitude.png)

如果您有權限可編輯 Power BI Desktop 中的資料集，請觀賞這段影片，以協助解決地圖模稜兩可的情況。

<iframe width="560" height="315" src="https://www.youtube.com/embed/Co2z9b-s_yM" frameborder="0" allowfullscreen></iframe>

如果您沒有經度和緯度資料的存取權，請[遵循這些指示來更新您的資料集](https://support.office.com/article/Maps-in-Power-View-8A9B2AF3-A055-4131-A327-85CC835271F7)。

如需地圖視覺效果的更多說明，請參閱[地圖視覺效果的祕訣和訣竅](../power-bi-map-tips-and-tricks.md)。

## <a name="next-steps"></a>後續步驟

[圖形地圖](desktop-shape-map.md)

[Power BI 中的視覺效果類型](power-bi-visualization-types-for-reports-and-q-and-a.md)
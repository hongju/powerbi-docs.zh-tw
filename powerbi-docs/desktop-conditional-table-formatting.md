---
title: 在 Power BI Desktop 中設定資料表格式化的條件
description: 將自訂格式套用至資料表
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/07/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: e23fd2aca90ee14c2376b0175c7c8b5132cf9a9f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "66222269"
---
# <a name="conditional-formatting-in-tables"></a>設定資料表格式化的條件 
設定資料表格式化的條件時，您可以根據資料格值或根據其他值或欄位 (包括漸層色彩) 來指定自訂資料格色彩。 您也可以使用資料橫條來顯示資料格的值。 

若要存取條件式格式設定，請在 Power BI Desktop [視覺效果]  窗格的 [欄位]  集區，選取您要格式化的 [值]  集區中，值旁邊的向下箭號 (或以滑鼠右鍵按一下欄位)。 您只能管理 [欄位]  集區之 [值]  區域中的欄位條件式格式設定。

![條件式格式設定功能表](media/desktop-conditional-table-formatting/table-formatting-0-popup-menu.png)

下列各節將逐一描述這些條件式格式設定選項。 一或多個選項可以組合在一個資料表資料行中。

> [!NOTE]
> 套用至資料表時，條件式格式設定會覆寫套用至條件式設定資料格之格式的任何自訂資料表樣式。

若要從視覺效果移除條件式格式設定，只要以滑鼠右鍵再按一次欄位，選取 [移除條件式格式設定]  ，然後選取要移除的格式設定類型即可。

![移除條件式格式設定功能表](media/desktop-conditional-table-formatting/table-formatting-1-remove.png)

## <a name="background-color-scales"></a>背景色階

選取 [條件式格式設定]  然後選取 [背景色階]  ，下列對話方塊隨即開啟。

![背景色階對話方塊](media/desktop-conditional-table-formatting/table-formatting-1-default-dialog.png)

您可以從您的資料模型選取色彩依據的欄位，方法為設定 該欄位的[色彩依據]  。 此外，您可以使用**摘要**值指定所選欄位的彙總類型。 在 [將色彩套用到]  欄位中指定要上色的欄位，以便您可以追蹤。您可以將設定格式化的條件套用至文字和日期欄位，只要您選擇數值作為格式設定基礎。

![色彩依據欄位](media/desktop-conditional-table-formatting/table-formatting-1-apply-color-to.png)

若要針對指定的值範圍使用離散色彩值，請選取 [依規則上色]  。 若要使用色彩頻譜，請將 [依規則上色]  保留未核取狀態。 

![背景色階對話方塊](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-dialog.png)

### <a name="color-by-rules"></a>依規則上色

當您選取 [依規則上色]  時，您可以輸入一或多個值範圍，每個都具有一個設定色彩。  每個值範圍都以「如果值」  條件、「和」  值條件以及一個色彩開始。

![依規則色彩值範圍](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-if-value.png)

每個範圍中含有值的資料表資料格都會以指定色彩填滿。 下圖有三個規則。

![依規則上色範例](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules.png)

範例資料表現在如下所示：

![使用依規則上色的範例資料表](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-table.png)


### <a name="color-minimum-to-maximum"></a>最小到最大色彩

您可以設定 [最小]  和 [最大]  值以及其色彩。 如果您選取 [發散]  方塊，您也可以設定選擇性的「中間」值  。

![[發散] 按鈕](media/desktop-conditional-table-formatting/table-formatting-1-diverging.png)

範例資料表現在如下所示：

![使用發散色彩的範例資料表](media/desktop-conditional-table-formatting/table-formatting-1-diverging-table.png)

## <a name="font-color-scales"></a>字型色階

選取 [條件式格式設定]  然後選取 [字型色階]  ，下列對話方塊隨即開啟。 此對話方塊類似於 [背景色階]  對話方塊，但會變更字型色彩，而不是資料格背景色彩。

![字型色階對話方塊](media/desktop-conditional-table-formatting/table-formatting-2-diverging.png)

範例資料表現在如下所示：

![範例資料表與字型色階](media/desktop-conditional-table-formatting/table-formatting-2-table.png)

## <a name="data-bars"></a>資料橫條

選取 [條件式格式設定]  然後選取 [資料橫條]  ，下列對話方塊隨即開啟。 

![資料橫條對話方塊](media/desktop-conditional-table-formatting/table-formatting-3-default.png)

根據預設，未核取 [只顯示橫條]  選項，因此資料表資料格會顯示橫條與實際值兩者。

![範例資料表與資料橫條和值](media/desktop-conditional-table-formatting/table-formatting-3-default-table.png)

如果 [只顯示橫條]  選項已核取，則資料表資料格只會顯示橫條。

![範例只顯示資料橫條](media/desktop-conditional-table-formatting/table-formatting-3-default-table-bars.png)

## <a name="color-formatting-by-field-value"></a>依欄位值指定格式色彩

您可以使用指定色彩的量值或資料行，搭配文字值或十六進位碼，將該色彩套用至資料表或矩陣視覺效果之字型色彩的背景。 您也可以建立指定欄位的自訂邏輯，並讓該邏輯將所需的色彩套用至字型或背景。

例如，在下表中，每個產品型號都有相關聯的色彩。 

![ProductName 欄位和色彩名稱](media/desktop-conditional-table-formatting/conditional-table-formatting_01.png)

若要根據其欄位值來格式化該資料格，請選取 [條件式格式設定]  對話方塊，方法是以滑鼠右鍵按一下該視覺效果的 [色彩]  資料行，然後在本例中從功能表選取 [背景色彩]  。 

![從功能表選取 [背景色彩]](media/desktop-conditional-table-formatting/conditional-table-formatting_02.png)

在顯示的對話方塊中，選取 [格式化依據]  下拉式清單區域中的 [欄位值]  ，如下列影像所示。

![依欄位值格式化](media/desktop-conditional-table-formatting/conditional-table-formatting_03.png)

您可以針對字型色彩重複該程序，而視覺效果中的結果會是 [色彩]  資料行中的單色，如下列畫面所示。

![依欄位值格式化](media/desktop-conditional-table-formatting/conditional-table-formatting_04.png)

您也可以建立以商務邏輯為基礎的 DAX 計算，來根據您偏好的條件輸出不同的十六進位碼。 這通常比在 [條件式格式設定] 對話方塊中建立多項規則更容易。 請考慮下列範例影像中的 *ColorKPI* 欄位。

![DAX 計算](media/desktop-conditional-table-formatting/conditional-table-formatting_05.png)

然後，您可以透過下列方式來設定 [背景色彩]  的欄位值。

![根據 KPI 設定欄位色彩](media/desktop-conditional-table-formatting/conditional-table-formatting_06.png)

然後，您可以取得類似下列矩陣的結果。

![矩陣視覺效果及以 KPI 值為基準的色彩](media/desktop-conditional-table-formatting/conditional-table-formatting_07.png)

只要運用您的想像力和一點 DAX，您還可以建立更多版本。

您可以使用任何 CSS 色彩規格，在中所列的值[ https://www.w3.org/TR/css-color-3/ ](https://www.w3.org/TR/css-color-3/)色彩視覺效果：
* 3、 6 或 8 位數十六進位碼例如 #3E4AFF。 請確定您包含在程式碼的開頭為 # 符號。 不接受 「 3E4AFF"。 
* RGB 或 RGBA 值例如 RGBA （234、 234、 234，0.5）
* HSL 或 HSLA 值例如 HSLA （123、 75%、 75%，0.5）
* 色彩名稱例如綠色 SkyBlue PeachPuff 

## <a name="next-steps"></a>後續步驟
如需詳細資訊，請參閱下列文章：  

* [在 Power BI 中色彩格式設定的秘訣和訣竅](visuals/service-tips-and-tricks-for-color-formatting.md)  


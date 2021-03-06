---
title: 在 Power BI Desktop 中自訂工具提示
description: 使用拖放功能建立視覺效果的自訂工具提示
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/07/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: d5259ba22287a8a2ade3107e4320c39713dcb45e
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "65239757"
---
# <a name="customizing-tooltips-in-power-bi-desktop"></a>在 Power BI Desktop 中自訂工具提示
工具提示很適合用來為視覺效果的資料點提供更多關聯式資訊和詳細資料。 下圖顯示套用至 Power BI Desktop 中圖表的工具提示。

![預設工具提示](media/desktop-custom-tooltips/custom-tooltips-1.png)

建立視覺效果時，預設的工具提示會顯示資料點的值與類別。 自訂工具提示資訊非常有用，並無法提供額外的內容和檢視視覺效果之使用者的資訊時，有許多執行個體。 自訂工具提示可讓您指定額外的資料點，以當做工具提示的一部分顯示。

## <a name="how-to-customize-tooltips"></a>如何自訂工具提示
若要建立自訂的工具提示中，在**欄位**部分**視覺效果**窗格將欄位拖曳至**工具提示**貯體，如下圖所示。 在下圖中，已將兩個欄位放入 [工具提示]  值區。

![新增工具提示欄位](media/desktop-custom-tooltips/custom-tooltips-2.png)

在工具提示新增到下層欄位之後，當滑鼠暫留在視覺效果的資料點上時，就會顯示工具提示中這些欄位的值。

![自訂工具提示](media/desktop-custom-tooltips/custom-tooltips-3.png)

## <a name="customizing-tooltips-with-aggregation-or-quick-calcs"></a>使用彙總或快速計算來自訂工具提示
您可以選取彙總函數或 [快速計算]  來進一步自訂工具提示，方法是選取 [工具提示]  值區中欄位旁邊的箭號，然後從可用的選項中進行選取。

![具快速計算功能的工具提示](media/desktop-custom-tooltips/custom-tooltips-4.png)

有許多方式來自訂**工具提示**，傳達快速資訊和深入解析來檢視您的儀表板或報表的使用者使用您的資料集的任何欄位。


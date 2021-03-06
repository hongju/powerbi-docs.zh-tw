---
title: 在 Power BI 行動裝置應用程式中依地理位置篩選報表
description: 了解如何在 Power BI mobile apps 中，依地理位置篩選報表 (若報表擁有者已設定地理標記)。
author: mshenhav
manager: kfile
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 02/09/2018
ms.author: mshenhav
ms.openlocfilehash: 828dcb4aeb8b7c5e69292685470f112a2d85cb71
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "61348652"
---
# <a name="filter-a-report-by-geographic-location-in-the-power-bi-mobile-apps"></a>在 Power BI 行動裝置應用程式中依地理位置篩選報表
適用於︰

| ![iPhone](./media/mobile-apps-geographic-filtering/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-geographic-filtering/ipad-logo-50-px.png) | ![Android 手機](./media/mobile-apps-geographic-filtering/android-phone-logo-50-px.png) | ![Android 平板電腦](./media/mobile-apps-geographic-filtering/android-tablet-logo-50-px.png) | ![Android 平板電腦](./media/mobile-apps-geographic-filtering/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone |iPad |Android 手機 |Android 平板電腦 |Windows 10 手機 |

當您在行動裝置中查看 Power BI 報表時，是否看到右上角有小圖釘圖示？ 如果有的話，即可按您的地理位置來篩選該報表。

> [!NOTE]
> 只有在報表中的地理名稱是英文時 (例如 "New York City" 或 "Germany")，您才能依位置篩選報表。 Windows 10 平板電腦與電腦不支援地理篩選，但 Windows 10 手機支援。
> 
> 

## <a name="filter-your-report-by-your-geographic-location"></a>依地理位置篩選您的報表
1. 在行動裝置的 Power BI 行動裝置應用程式中，開啟報表。
2. 如果報表具有地理資料，您會看到訊息要求您允許 Power BI 存取您的位置。 按一下 [允許]  ，然後再次點選 [允許]  。
3. 點選圖釘 ![圖釘圖示](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-icon.png). 根據報表中的資料，您可以篩選城市、縣/市或國家/地區。 篩選器只會列出符合您目前位置的選項。
   
    ![圖釘篩選](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-map-set-filter.png)

## <a name="why-dont-i-see-location-tags-on-a-report"></a>為何會在報表上看到位置標記？
這三項條件都必須為符合，您才能看到位置標記。 

* 在 Power BI Desktop 中建立報表的人，將[地理資料分類](../../desktop-mobile-geofiltering.md)為至少一個資料行，例如縣 (市)、省或國家/地區。
* 您位在該資料行中具有資料的位置。
* 您使用下列其中一部行動裝置︰
  * iOS (iPad、iPhone、iPod)。
  * Android 手機或平板電腦。
  * Windows 10 電話 (電腦和平板電腦等其他不支援地理篩選的 Windows 10 裝置)。

深入了解如何在 Power BI Desktop 中[設定地理篩選](../../desktop-mobile-geofiltering.md)。

### <a name="next-steps"></a>後續步驟
* 透過行動裝置應用程式[實際連接 Power BI 資料](mobile-apps-data-in-real-world-context.md)
* [Power BI Desktop 中的資料分類](../../desktop-data-categorization.md) 
* 有問題嗎？ [嘗試在 Power BI 社群提問](http://community.powerbi.com/)


---
title: Power BI 與 Azure 輸出
description: 了解 Azure 的輸出費用，以及基於租用戶位置與 Power BI Premium 的 Power BI
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Data from databases
ms.openlocfilehash: 720ef2f059c3c87be84c3d8db98e89400c161ad0
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "65514393"
---
# <a name="power-bi-and-azure-egress"></a>Power BI 與 Azure 輸出

當使用 Power BI 與 Azure 的資料來源時，您可以藉由確定您的 Power BI 租用戶位於與 Azure 資料來源相同區域，來避免 Azure 輸出費用。

當您將 Power BI 租用戶部署在與部署資料來源相同的 Azure 區域中時，不會因排程的重新整理和 DirectQuery 互動而產生輸出費用。 

## <a name="determining-where-your-power-bi-tenant-is-located"></a>判斷您的 Power BI 租用戶所在位置

若要了解 Power BI 租用戶所在位置，請參閱[我的 Power BI 租用戶位於何處](service-admin-where-is-my-tenant-located.md)一文。

針對 Power BI Premium 多地理位置客戶，如果您的 Power BI 租用戶並非位於某些 Azure 型資料來源最佳位置，您可以在所需的 Azure 區域部署 Power BI Premium 多地理位置，並從將 Power BI 租用戶和 Azure 資料來源放在相同 Azure 區域中受益。

## <a name="next-steps"></a>後續步驟

如需 Power BI Premium 或多地理位置的詳細資訊，請查看下列資源：

* [Microsoft Power BI Premium 是什麼？](service-premium-what-is.md)
* [如何購買 Power BI Premium](service-admin-premium-purchase.md)
* [Power BI Premium 的多地理位置支援 (預覽)](service-admin-premium-multi-geo.md)
* [我的 Power BI 租用戶位於何處？](service-admin-where-is-my-tenant-located.md)
* [Power BI Premium 常見問題集](service-premium-faq.md)



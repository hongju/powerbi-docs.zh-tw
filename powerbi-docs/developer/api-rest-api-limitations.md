---
title: Power BI REST API 限制
description: Power BI REST API 具有下列限制
author: markingmyname
manager: kfile
ms.author: maghan
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: df17563d384359fe33123ed87743754bb33bf04d
ms.sourcegitcommit: c8c126c1b2ab4527a16a4fb8f5208e0f7fa5ff5a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/15/2019
ms.locfileid: "54277955"
---
# <a name="power-bi-rest-api-limitations"></a>Power BI REST API 限制  
  
**POST 資料列**  
  
* 最多 75 個資料行
* 最多 75 個資料表
* 單次 POST 的資料列要求上限為 10,000  
* 每小時將 1,000,000 個資料列加入每個資料集  
* 每個資料集最多 5 個暫止的 POST 資料列要求  
* 每分鐘每個資料集可有 120 POST 資料列要求
* 若資料表包含 250,000 (含) 個以上的資料列，每小時每個資料集可有 120 POST 資料列要求    
* 最多有 200,000 個資料列儲存在 FIFO 資料集的每個資料表  
* 最多有 5,000,000 個資料列儲存在「無保留原則」資料集的每個資料表  
* POST 資料列作業中每個字串資料行的值可有 4,000 個字元
  
## <a name="see-also"></a>另請參閱

[Azure AD服務限制](https://docs.microsoft.com/azure/active-directory/active-directory-service-limits-restrictions)   
[Power BI REST API 概觀](https://docs.microsoft.com/rest/api/power-bi/)
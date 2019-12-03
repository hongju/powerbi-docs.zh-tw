---
title: Power BI 資料來源
description: 本文列出 Power BI 支援的資料來源，包括 DirectQuery 和內部部署資料閘道的相關資訊。
author: mgblythe
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 11/22/2019
ms.author: mblythe
ms.openlocfilehash: 5f0161afc2174ac3511c03fda6ada09f2a5e41de
ms.sourcegitcommit: f1f57c5bc6ea3057007ed8636ede50188ed90ce1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "74414295"
---
# <a name="power-bi-data-sources"></a>Power BI 資料來源

下表顯示 Power BI 支援的資料來源，包括 DirectQuery 和內部部署資料閘道的相關資訊。

| 資料來源 | 從桌面連線 | 從服務連線並重新整理 | DirectQuery/即時連線限制 | 閘道 (支援) | 閘道 (必要) |
|---|---|---|---|---|---|---|---|
| Access 資料庫 | 是 | 是 | 否 | 是 <sup>1</sup> | 是 |
| ActiveDirectory | 是 | 是 | 否 | 是 | 是 |
| Adobe Analytics | 是 | 是 | 否 | 否 | 否 |
| Amazon Redshift | 是 | 是 | 是 | 是 | 否 |
| appFigures | 是 | 是 | 否 | 否 | 否 |
| AtScale Cube | 是 | 是 | 是 | 是 | 否 |
| Azure Analysis Services | 是 | 是 | 是 | 是 <sup>2</sup> | 否 |
| Azure Blob 儲存體 | 是 | 是 | 否 | 是 | 否 |
| Azure Cosmos DB | 是 | 是 | 否 | 否 | 否 |
| Azure 成本管理 | 是 | 是 | 否 | 否 | 否 |
| Azure 資料總管 (kusto) | 是 | 是 | 是 | 否 | 否 |
| Azure Data Lake Storage Gen1 | 是 | 是 | 否 | 否 | 否 |
| Azure Data Lake Storage Gen2 | 是 | 是 | 否 | 否 | 否 |
| Azure DevOps | 是 | 是 | 否 | 否 | 否 |
| Azure DevOps Server | 是 | 是 | 否 | 是 | 是 |
| Azure HDInsight (HDFS) | 是 | 是 | 否 | 否 | 否 |
| Azure HDInsight Spark | 是 | 是 | 是 | 否 | 否 |
| Azure SQL Database | 是 | 是 | 是 | 是 <sup>2</sup> | 否 |
| Azure SQL 資料倉儲 | 是 | 是 | 是 | 否 | 否 |
| Azure 表格儲存體 | 是 | 是 | 否 | 是 | 否 |
| BI 連接器 | 是 | 是 | 是 | 是 | 是 |
| BI360 - Budgeting & Financial Reporting | 是 | 是 | 否 | 否 | 否 |
| Common Data Service | 是 | 是 | 否 | 否 | 否 |
| Data.World - 取得資料集 | 是 | 是 | 否 | 否 | 否 |
| Denodo | 是 | 是 | 是 | 是 | 是 |
| Dremio | 是 | 是 | 是 | 是 | 是 |
| Dynamics 365 (線上) | 是 | 是 | 否 | 否 | 否 |
| Dynamics 365 Business Central | 是 | 是 | 否 | 否 | 否 |
| Dynamics 365 Business Central (內部部署) | 是 | 是 | 否 | 否 | 否 |
| Dynamics 365 Customer Insights | 是 | 是 | 否 | 否 | 否 |
| Dynamics NAV | 是 | 是 | 否 | 否 | 否 |
| Emigo 資料來源 | 是 | 是 | 否 | 否 | 否 |
| Entersoft 商務套件 | 是 | 是 | 否 | 否 | 否 |
| Essbase | 是 | 是 | 是 | 是 | 是 |
| Exasol | 是 | 是 | 是 | 是 | 是 |
| Excel | 是 <sup>3</sup> | 是 <sup>3</sup> | 否 | 是 <sup>3</sup> | 否 <sup>4</sup> |
| Facebook | 是 | 是 | 否 | 否 | 否 |
| 檔案 | 是 | 是 | 否 | 是 | 是 |
| 資料夾 | 是 | 是 | 否 | 是 | 是 |
| GitHub | 是 | 是 | 否 | 否 | 否 |
| Google Analytics | 是 | 是 | 否 | 否 | 否 |
| Google BigQuery | 是 | 是 | 否 | 否 | 否 |
| Hadoop 檔案 (HDFS) | 是 | 否 | 否 | 否 | 否 |
| HDInsight 互動式查詢 | 是 | 是 | 是 | 否 | 否 |
| IBM DB2 | 是 | 是 | 是 | 是 | 是 |
| IBM Informix 資料庫 | 是 | 是 | 否 | 是 | 是 |
| IBM Netezza | 是 | 是 | 是 | 是 | 是 |
| Impala | 是 | 是 | 是 | 是 | 是 |
| Indexima | 是 | 是 | 是 | 是 | 是 |
| 企業 App Store | 是 | 是 | 否 | 否 | 否 |
| Information Grid | 是 | 是 | 否 | 否 | 否 |
| Intersystems IRIS | 是 | 是 | 是 | 是 | 是 |
| Intune 資料倉儲 | 是 | 是 | 否 | 否 | 否 |
| Jethro ODBC | 是 | 是 | 是 | 是 | 是 |
| JSON | 是 | 是 | 否 | 是** | 否 <sup>4</sup> |
| Kyligence Enterprise | 是 | 是 | 是 | 是 | 是 |
| MailChimp | 是 | 是 | 否 | 否 | 否 |
| Marketo | 是 | 是 | 否 | 否 | 否 |
| MarkLogic ODBC | 是 | 是 | 是 | 是 | 是 |
| Microsoft Azure 使用量見解 | 是 | 是 | 否 | 否 | 否 |
| Microsoft Exchange | 是 | 是 | 否 | 是 | 否 |
| Microsoft Exchange Online | 是 | 是 | 否 | 否 | 否 |
| Microsoft Graph 安全性 | 是 | 是 | 否 | 是 | 否 |
| Mixpanel | 是 | 是 | 否 | 否 | 否 |
| MySQL | 是 | 是 | 否 | 是 | 是 |
| OData | 是 | 是 | 否 | 是 | 否 |
| ODBC | 是 | 是 | 否 | 是 | 是 |
| OleDb | 是 | 是 | 否 | 是 | 是 |
| Oracle | 是 | 是 | 是 | 是 | 是 |
| Paxata | 是 | 是 | 否 | 是 | 否 |
| PDF | 是 | 是 | 否 | 是 | 否 <sup>4</sup> |
| Planview Enterprise One - CTM | 是 | 是 | 否 | 否 | 否 |
| Planview Enterprise One - PRM | 是 | 是 | 否 | 否 | 否 |
| Planview Projectplace | 是 | 是 | 否 | 否 | 否 |
| PostgreSQL | 是 | 是 | 否 | 是 | 是 |
| Power BI 資料流程 | 是 | 是 | 否 | 否 | 否 |
| Power BI 資料集 | 是 | 是 | 是 | 否 | 否 |
| Power Platform 資料流程 | 是 | 是 | 否 | 否 | 否 |
| Python 指令碼 | 是 | 是 <sup>5</sup> | 否 | 是 <sup>5</sup> | 是 |
| QubolePresto | 是 | 是 | 是 | 是 | 是 |
| Quick Base | 是 | 是 | 否 | 是 | 是 |
| QuickBooks Online | 是 | 是 | 否 | 否 | 否 |
| R 指令碼 | 是 | 是 <sup>5</sup> | 否 | 是 <sup>5</sup> | 否 |
| Roamler | 是 | 是 | 否 | 是 | 否 |
| Salesforce 物件 | 是 | 是 | 否 | 否 | 否 |
| Salesforce 報表 | 是 | 是 | 否 | 否 | 否 |
| SAP Business Warehouse 訊息伺服器 | 是 | 是 | 是 | 是 | 是 |
| SAP Business Warehouse 伺服器 | 是 | 是 | 是 | 是 | 是 |
| SAP HANA | 是 | 是 | 是 | 是 | 是 |
| SharePoint 資料夾 | 是 | 是 | 否 | 是 | 否 <sup>4</sup> |
| SharePoint 清單 | 是 | 是 | 否 | 是 | 否 <sup>4</sup> |
| SharePoint Online 清單 | 是 | 是 | 否 | 是 <sup>2</sup> | 否 |
| Smartsheet | 是 | 是 | 否 | 否 | 否 |
| Snowflake | 是 | 是 | 是 | 是 | 是 |
| Spark | 是 | 是 | 是 | 是 | 否 |
| SparkPost | 是 | 是 | 否 | 否 | 否 |
| SQL Server | 是 | 是 | 是 | 是 | 是 |
| SQL Server Analysis Services | 是 | 是 | 是 | 是 | 是 |
| Stripe | 是 | 是 | 否 | 否 | 否 |
| SurveyMonkey | 是 | 是 | 否 | 是 | 否 |
| SweetIQ | 是 | 是 | 否 | 否 | 否 |
| Sybase | 是 | 是 | 否 | 是 | 是 |
| TeamDesk | 是 | 是 | 否 | 是 | 否 |
| Tenforce | 是 | 是 | 否 | 否 | 否 |
| Teradata | 是 | 是 | 是 | 是 | 是 |
| 文字/CSV | 是 | 是 | 否 | 是 | 否 <sup>4</sup> |
| Twilio | 是 | 是 | 否 | 否 | 否 |
| tyGraph | 是 | 是 | 否 | 否 | 否 |
| Vertica | 是 | 是 | 是 | 是 | 是 |
| Web | 是 | 是 | 否 | 是 | 是 |
| Webtrends | 是 | 是 | 否 | 否 | 否 |
| Workforce Dimensions | 是 | 是 | 否 | 是 | 否 |
| XML | 是 | 是 | 否 | 是 | 否 <sup>4</sup> |
| Zendesk | 是 | 是 | 否 | 否 | 否 |
| | | | | | | | |

<sup>1</sup> 支援 [ACE OLEDB 提供者](https://www.microsoft.com/download/details.aspx?id=54920)，其與閘道安裝在同一部電腦上。

<sup>2</sup> 支援與內部部署版本相同的 M 函式。

<sup>3</sup> Excel 1997-2003 檔案 (.xls) 需要 [ACE OLEDB 提供者](https://www.microsoft.com/download/details.aspx?id=54920)。

<sup>4</sup> 技術的內部部署版本所需。

<sup>5</sup> 僅支援[個人閘道](service-gateway-personal-mode.md)。

## <a name="single-sign-on-sso-for-directquery-sources"></a>DirectQuery 來源的單一登入 (SSO)

若已啟用 SSO 選項，且您使用者存取建置在資料來源上的報告，則 Power BI 會在對基礎資料來源的查詢中傳送其已驗證 Azure AD 認證。 這可讓 Power BI 遵從在資料來源層級所設定的安全性設定。
SSO 選項會在使用此資料來源的所有資料集中生效。 它不會影響用於匯入案例的驗證方法。 下列資料來源支援透過 DirectQuery 進行連線的 SSO：

- Azure SQL Database
- Azure SQL 資料倉儲
- Impala
- SAP HANA
- SAP BW
- SAP BW 訊息伺服器
- Spark
- SQL Server
- Teradata

> [!Note]
> 不支援 Azure Multi-Factor Authentication (MFA)。 想要搭配 DirectQuery 使用 SSO 的使用者必須豁免於 MFA 之外。

## <a name="next-steps"></a>後續步驟

[在 Power BI Desktop 中連線至資料](desktop-quickstart-connect-to-data.md)  
[使用 Power BI 中的 DirectQuery](desktop-directquery-about.md)  
[Power BI 中的 SQL Server Analysis Services 即時資料](sql-server-analysis-services-tabular-data.md)  
[什麼是內部部署的資料閘道？](service-gateway-onprem.md)  
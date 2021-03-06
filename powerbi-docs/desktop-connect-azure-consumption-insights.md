---
title: 從 Power BI Desktop 連線至 Azure 的成本和用量
description: 輕鬆地連線到 Azure，並使用 Power BI Desktop 深入了解耗用量和使用
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 12/06/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 4c2ef62dc3ea8aac9c4a0d30ba4dba58e2279490
ms.sourcegitcommit: 57a12aa42c8549debc60ff1c8e78533dc42e1b86
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2019
ms.locfileid: "66469832"
---
# <a name="analyze-azure-cost-and-usage-data-in-power-bi-desktop"></a>在 Power BI Desktop 中分析 Azure 成本和使用量資料

Power BI Desktop 可連線至 Azure，並取得有關貴組織 Azure 服務使用量的深入資料。 有了它，您就可以建立自訂報表和量值，以便更充分了解和分析您的 Azure 費用。

Power BI 目前支援連線至 Enterprise 合約及客戶合約的帳單帳戶。

* **Enterprise 合約**使用者應該與「Azure 使用量見解連接器」  進行連線。

* **客戶合約**使用者則應該與 **Azure 成本管理連接器**進行連線。

## <a name="connect-with-azure-consumption-insights"></a>與 Azure 使用量見解進行連線

Azure 使用量見解可讓您連線至 Azure Enterprise 合約的帳單帳戶。

在本節中，您將了解如何取得所需的資料、如何從使用 Azure 企業版連接器移轉，且您會發現「使用量詳細資料資料行」  的對應，這提供於 **ACI** (Azure 使用量見解) API。

若要成功使用 **Azure 使用深入解析**連接器進行連線，您必須能夠存取 Azure 入口網站內的企業功能。

若要使用 **Azure 使用深入解析**連接器進行連線，請在 **Power BI Desktop** 的 [首頁]  功能區中選取 [取得資料]  。 從左邊的類別選取 [線上服務]  ，您將會看到 **Microsoft Azure 使用深入解析 (搶鮮版 (Beta))** 。 選取 [連接]  。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_01b.png)

在出現的對話方塊，提供您的「註冊號碼」  。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_02.png)

* 您可以從 [Azure 企業版入口網站](https://ea.azure.com)取得註冊號碼，位置如下圖所示：

  ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_08.png)

  這個版本的連接器僅支援從 https://ea.azure.com 進行的企業註冊。 中國目前不支援註冊。

接下來，提供連接用的「存取金鑰」  。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_03.png)

* 您的註冊用存取金鑰可以在 [Azure 企業版入口網站](https://ea.azure.com)找到。

  ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_09.png)

提供「存取金鑰」  並選取 [連線]  之後，[導覽器]  視窗隨即出現，並顯示九個您可取得的資料表：
* **預算**：提供預算詳細資料，以檢視實際成本或現有預算目標的使用情況。
* **Marketplace**：提供用量型 Azure Marketplace 費用。
* **PriceSheets**：藉由註冊的計量提供適用的費率。
* **RICharges**：提供過去 24 個月與您的保留執行個體相關聯的費用。
* **RIRecommendations_Single**：根據您單一訂用帳戶上，過去 7、30 或 60 天的使用量趨勢所提供的保留執行個體購買建議。
* **RIRecommendations_Shared**：根據您所有訂用帳戶上，過去 7、30 或 60 天的使用量趨勢所提供的保留執行個體購買建議。
* **RIUsage**：提供您現有保留執行個體過去一個月的使用詳細資料。
* **Summaries**：提供包含餘額、新購買、Azure Marketplace 服務費用、調整和超額費用的每月摘要。
* **UsageDetails**：使用量的細目和註冊的估計費用。

您可以選取任何資料表旁邊的核取方塊，以便查看預覽。 您可以藉由核取名稱旁邊的方塊，選取一或多個資料表，然後選擇 [載入]  。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_04b.png)

> [!NOTE]
> *Summary* 和 *PriceSheet* 資料表只可供註冊層級 API 金鑰之用。 此外，這些資料表中的資料預設具有目前月份的 *Usage* 和 *PriceSheet* 資料。 *Summary* 和 *MarketPlace* 資料表不受限於目前月份。
>
>

當您選取 [載入]  時，資料會載入到 **Power BI Desktop**。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_05.png)

您選取的資料載入後，可以在 [欄位]  窗格看到您所選取的資料表和欄位。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_06.png)

## <a name="using-azure-consumption-insights"></a>使用 Azure 使用深入解析
若要使用 **Azure 使用深入解析**連接器，您必須能夠存取 Azure 入口網站內的企業功能。

成功使用 **Azure 使用深入解析**連接器載入資料之後，您可以使用查詢編輯器  建立自己的自訂量值和資料行，而且可以建立視覺效果、報表和儀表板，並且可以在 **Power BI 服務**中共用。

Azure 也包含範例自訂查詢的集合，您可以使用空的查詢來擷取。 若要這樣做，請在 **Power BI Desktop** 的 [首頁]  功能區，選取 [取得資料]  的下拉式箭號，然後選取 [空的查詢]  。 您也可以在查詢編輯器  這麼做，方法是以滑鼠右鍵按一下左邊的 [查詢]  窗格，然後從出現的功能表選取 [新查詢] > [空的查詢]  。

在 [公式列]  中鍵入以下內容：

    = MicrosoftAzureConsumptionInsights.Contents

隨即出現範例集合，如下圖所示：

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_07.png)

當處理報表和建立查詢時，請使用下列各項：

* 若要定義從目前日期開始的月份數，請使用 *numberOfMonth*
  * 使用介於 1 到 36 的值來代表您要匯入的月份數，從目前日期開始。 我們建議您不要取得超過 12 個月的資料，以避免匯入條件約束的臨界值，以及 Power BI 中查詢允許的資料量。
* 若要定義歷程記錄時間範圍中的月份期間，請使用 *startBillingDataWindow* 和 *endBillingDataWindow*
* 請「勿」將  *numberOfMonth* 與 *startBillingDataWindow* 或 *endBillingDataWindow* 搭配使用

## <a name="migrating-from-the-azure-enterprise-connector"></a>從 Azure 企業版連接器移轉
有些客戶使用 *Azure 企業版連接器 (搶鮮版 (Beta))* 建立視覺效果，這最終將會中止服務，並取代為 **Azure 使用深入解析**連接器。 **Azure 使用深入解析**連接器的功能和增強功能包括：

* 適用於 *Balance Summary* 和 *Marketplace Purchases* 的其他資料來源
* 新參數和進階參數，例如 *startBillingDataWindow* 和 *endBillingDataWindow*
* 較佳的效能和回應

為了協助客戶轉換到較新的 **Azure 使用深入解析**連接器，並保留他們在建立自訂儀表板或報表方面已完成的工作，下列步驟顯示如何移至新的連接器。

### <a name="step-1-connect-to-azure-using-the-new-connector"></a>步驟 1：使用新的連接器連線到 Azure
第一個步驟是使用 **Azure 使用深入解析**連接器進行連線，如本文稍早所詳述。 在此步驟中，從 **Power BI Desktop** 的 [首頁]  功能區選取 **[取得資料] > [空的查詢]** 。

### <a name="step-2-use-the-advanced-editor-to-create-a-query"></a>步驟 2：使用進階編輯器來建立查詢
在查詢編輯器  中，從 [首頁]  功能區的 [查詢]  區段，選取 [進階編輯器]  。 在出現的 [進階編輯器]  視窗中，輸入下列查詢：

    let    
        enrollmentNumber = "100",
        optionalParameters = [ numberOfMonth = 6, dataType="DetailCharges" ],
        data = MicrosoftAzureConsumptionInsights.Contents(enrollmentNumber, optionalParameters)   
    in     
        data

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_10.png)

當然，您必須將 *enrollmentNumber* 的值取代為您自己的註冊號碼，您可以從 [Azure 企業版入口網站](https://ea.azure.com)取得。 *NumberOfMonth* 參數是您要傳回幾個月的資料，從目前的日期起算。 使用零 (0) 代表目前的月份。

在 [進階編輯器]  視窗中選取 [完成]  之後，預覽會重新整理，您會在資料表中看到來自指定月份範圍的資料。 選取 [關閉並套用]  然後返回。

### <a name="step-3-move-measures-and-custom-columns-to-the-new-report"></a>步驟 3：將量值和自訂資料行移至新的報表
接下來，您必須將任何自訂資料行或您建立的量值移至新的詳細資料資料表。 以下是步驟。

1. 開啟 [記事本] \(或其他文字編輯器)。
2. 選取您想要移動的量值，並從 [公式]  欄位複製文字且放在 [記事本] 中。

   ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_11.png)
3. 將 *Query1* 重新命名為原始的詳細資料資料表名稱。
4. 在資料表中建立新的量值和自訂資料行，方法是以滑鼠右鍵按一下資料表，選擇 [新增量值]  ，然後剪下並貼上您儲存的量值和資料行，直到全部完成。

### <a name="step-4-re-link-tables-that-had-relationships"></a>步驟 4：重新連結有關聯性的資料表
許多儀表板有其他用來查閱或篩選的資料表，例如日期資料表或用於自訂專案的資料表。 重新建立這些關聯性，可以解決大部分剩餘的問題。 以下說明如何執行這項作業。

- 在 **Power BI Desktop**的 [模型]  索引標籤中，選取 [管理關聯性]  ，以顯示視窗讓您管理模型內的關聯性。 視需要重新連結您的資料表。

    ![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_12.png)

### <a name="step-5-verify-your-visuals-and-adjust-field-formatting-as-needed"></a>步驟 5：驗證視覺效果，然後視需要調整欄位格式設定
到目前為止，您大部分的原始視覺效果、資料表和鑽研應該會正常運作。 不過，可能有一些格式設定所需的細微調整，讓一切看來正如您所想要。 需要一些時間查看每個儀表板和視覺效果，以確保它們看來如您所想要。

## <a name="using-the-azure-consumption-and-insights-aci-api-to-get-consumption-data"></a>使用 Azure 使用深入解析 (ACI) API 來取得使用資料
Azure 也提供 [**Azure 使用深入解析 (ACI) API**](https://azure.microsoft.com/blog/announcing-general-availability-of-consumption-and-charge-apis-for-enterprise-azure-customers/)。 您可以建立自己的自訂解決方案，來使用 ACI API 收集、報告和視覺化 Azure 使用資訊。

### <a name="mapping-names-and-usage-details-between-the-portal-the-connector-and-the-api"></a>在入口網站、連接器和 API 之間對應名稱和使用詳細資料
Azure 入口網站中的詳細資料資料行和名稱，在 API 和連接器中類似，但並非完全相同。 為了協助釐清，下表提供 API、連接器與您在 Azure 入口網站中看到的資料行之間的對應。 同時也指出資料行是否已經淘汰。 如需這些詞彙的詳細資訊和定義，請參閱 [Azure 帳單資料字典](https://docs.microsoft.com/azure/billing/billing-enterprise-api-usage-detail)。

| ACI 連接器 / ContentPack ColumnName | ACI API 資料行名稱 | EA 資料行名稱 | 已淘汰/為了回溯相容性而存在 |
| --- | --- | --- | --- |
| AccountName |accountName |帳戶名稱 |否 |
| AccountId |accountId | |是 |
| AcccountOwnerId |accountOwnerEmail |AccountOwnerId |否 |
| AdditionalInfo |additionalInfo |AdditionalInfo |否 |
| AdditionalInfold | | |是 |
| Consumed Quantity |consumedQuantity |Consumed Quantity |否 |
| Consumed Service |consumedService |Consumed Service |否 |
| ConsumedServiceId |consumedServiceId | |是 |
| 成本 |cost |ExtendedCost |否 |
| Cost Center |costCenter |Cost Center |否 |
| 日期 |日期 |日期 |否 |
| 日 | |日 |否 |
| DepartmentName |departmentName |部門名稱 |否 |
| DepartmentID |departmentId | |是 |
| Instance ID | | |是 |
| InstanceId |instanceId |Instance ID |否 |
| 位置 | | |是 |
| Meter Category |meterCategory |Meter Category |否 |
| Meter ID | | |是 |
| 計量名稱 |meterName |計量名稱 |否 |
| Meter Region |meterRegion |Meter Region |否 |
| Meter Sub-Category |meterSubCategory |Meter Sub-Category |否 |
| MeterId |meterId |Meter ID |否 |
| Month | |Month |否 |
| 產品 |product |產品 |否 |
| ProductId |productId | |是 |
| 資源群組 |resourceGroup |資源群組 |否 |
| Resource Location |resourceLocation |Resource Location |否 |
| ResourceGroupId | | |是 |
| ResourceLocationId |resourceLocationId | |是 |
| ResourceRate |resourceRate |ResourceRate |否 |
| ServiceAdministratorId |serviceAdministratorId |ServiceAdministratorId |否 |
| ServiceInfo1 |serviceInfo1 |ServiceInfo1 |否 |
| ServiceInfo1Id | | |是 |
| ServiceInfo2 |serviceInfo2 |ServiceInfo2 |否 |
| ServiceInfo2Id | | |是 |
| Store Service Identifier |storeServiceIdentifier |Store Service Identifier |否 |
| StoreServiceIdentifierId | | |是 |
| 訂用帳戶名稱 |subscriptionName |訂用帳戶名稱 |否 |
| 標籤 |標籤 |標籤 |否 |
| TagsId | | |是 |
| Unit Of Measure |unitOfMeasure |Unit Of Measure |否 |
| 年度 | |年度 |否 |
| SubscriptionId |subscriptionId |SubscriptionId |是 |
| SubscriptionGuid |subscriptionGuid |SubscriptionGuid |否 |

## <a name="connect-with-azure-cost-management"></a>與 Azure 成本管理進行連線

在本節中，您將了解如何連線至您的客戶合約帳單帳戶。

> [!NOTE]
> Azure 成本管理連接器目前支援**客戶合約**的客戶。  **Enterprise 合約**客戶應該使用 Microsoft Azure 使用量見解連接器。
>
>

若要使用 **Azure 成本管理**連接器進行連線，請從 **Power BI Desktop** 的 [首頁]  功能區中選取 [Get Data] \(取得資料\)  。  從左側的類別選取 [Azure]  ，您會看到 [Azure Cost Management (Beta)] \(Azure 成本管理 (搶鮮版 (Beta))\)  。 選取 [連接]  。

![](media/desktop-connect-azure-consumption-insights/azure-cost-management-00.png)

在出現的對話方塊中，輸入您的「帳單設定檔識別碼」  。

![](media/desktop-connect-azure-consumption-insights/azure-cost-management-01.png)

您可以從 [Azure 入口網站](https://portal.azure.com)取得帳單設定檔識別碼。  巡覽至 [Cost Management + Billing] \(成本管理 + 帳單\)  ，並選取您的帳單帳戶，然後選取側邊欄中的 [Biling profiles] \(帳單設定檔\)  。  選取您的帳單設定檔，然後選取側邊欄中的 [屬性]  。  複製您的帳單設定檔識別碼。

![](media/desktop-connect-azure-consumption-insights/azure-cost-management-02.png)

系統會提示您使用 Azure 電子郵件和密碼登入。  進行驗證之後，您會看到 [導覽器]  視窗，其中有 12 個資料表可供您使用：

* **帳單事件**：提供新發票、點數購買等事件記錄檔。
* **預算**：提供預算詳細資料，以檢視實際成本或現有預算目標的使用情況。
* **費用**：提供 Azure 使用量、市場費用和分別計費費用的月份層級摘要。
* **整批點數**：為所提供帳單設定檔提供 Azure 整批購買點數的詳細資料。
* **點數摘要**：為所提供帳單設定檔提供點數摘要。
* **Marketplace**：提供用量型 Azure Marketplace 費用。
* **價位表**：為所提供帳單設定檔提供依計量排列的適用費率。
* **RI 費用**：提供過去 24 個月與您的保留執行個體相關聯的費用。
* **RI 建議 (單一)** ：根據您單一訂用帳戶上，過去 7、30 或 60 天的使用量趨勢所提供的保留執行個體購買建議。
* **RI 建議 (共用)** ：根據您所有訂用帳戶上，過去 7、30 或 60 天的使用量趨勢所提供的保留執行個體購買建議。
* **RI 使用量**：提供您現有保留執行個體過去一個月的使用詳細資料。
* **使用量詳細資料**：為所指定帳單設定檔識別碼提供使用量的細目和估計費用。

您可以選取任何資料表旁邊的核取方塊，以便查看預覽。  您可以藉由核取名稱旁邊的方塊，然後選取 [載入]  ，以選取一或多個資料表。

![](media/desktop-connect-azure-consumption-insights/azure-cost-management-03.png)

當您選取 [載入]  時，資料會載入到 **Power BI Desktop**。

![](media/desktop-connect-azure-consumption-insights/azure-consumption-insights_05.png)

您選取的資料載入後，可以在 [欄位]  窗格看到您所選取的資料表和欄位。

![](media/desktop-connect-azure-consumption-insights/azure-cost-management-05.png)

請觀看 [How to analyze spending in Power BI with Azure Consumption Insights](https://www.youtube.com/watch?v=QKBMXXrlpEk) (如何使用 Azure 使用量見解分析 Power BI 的支出) 影片，以了解如何使用 Azure 使用量見解連接器檢閱 Power BI Desktop 中的成本資料。

## <a name="writing-custom-queries"></a>撰寫自訂查詢

如果您想要自訂月數、變更 API 版本，或對傳回的資料執行更進階的邏輯，您可以建立自訂 M 查詢。

請移至 **Power BI Desktop** 的 [首頁]  功能區，並選取 [Get Data] \(取得資料\)  的下拉式箭號，然後選取 [空白查詢]  。  您也可以在**查詢編輯器**中這麼做，方法是以滑鼠右鍵按一下左側的 [查詢]  窗格，然後從出現的功能表中選取 [新增查詢] > [Blank Menu] \(空白功能表\)  。

在 [公式列]  中鍵入下列內容，將 `billingProfileId` 取代為您的實際識別碼，並將 "charges" 取代為任何有效的資料表名稱 (如先前所列)。

```
let
    Source = AzureCostManagement.Tables(billingProfileId, [ numberOfMonths = 3 ]),
    charges = Source{[Key="charges"]}[Data]
in
    charges
```

除了將 `numberOfMonths` 修改為介於 1 到 36 之間的任何值，您還可以提供：

* `apiVersion`，用來自訂查詢將會呼叫的 API 版本。
* `lookbackWindow` 適用於 RI 建議 (單一或共用)，用來修改要從中產生建議的時間範圍 (有效的選項：7、30 或 60 天)


## <a name="next-steps"></a>後續步驟
您可以使用 Power BI Desktop 連接至各式各樣的資料。 如需有關資料來源的詳細資訊，請參閱下列資源︰

* [Power BI Desktop 是什麼？](desktop-what-is-desktop.md)
* [Power BI Desktop 中的資料來源](desktop-data-sources.md)
* [使用 Power BI Desktop 合併資料並使其成形](desktop-shape-and-combine-data.md)
* [在 Power BI Desktop 中連接至 Excel 活頁簿](desktop-connect-excel.md)   
* [直接將資料輸入 Power BI Desktop 中](desktop-enter-data-directly-into-desktop.md)   

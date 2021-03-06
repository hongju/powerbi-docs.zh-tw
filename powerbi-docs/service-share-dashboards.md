---
title: 與同事和其他人共用 Power BI 儀表板和報表
description: 如何與組織內外的同事共用 Power BI 儀表板與報表，以及需要了解的共用相關資訊。
author: maggiesMSFT
manager: kfile
ms.reviewer: lukaszp
featuredvideoid: 0tUwn8DHo3s
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/24/2019
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: cb4fdeeea228d388197c35c69d934c0bf04c8033
ms.sourcegitcommit: 8bf2419b7cb4bf95fc975d07a329b78db5b19f81
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "66374705"
---
# <a name="share-power-bi-dashboards-and-reports-with-coworkers-and-others"></a>與同事和其他人共用 Power BI 儀表板和報表
「共用」  是讓一些人存取您儀表板和報表的一種好方法。 Power BI 還提供[數種其他方式可進行共同作業及散發您的儀表板和報表](service-how-to-collaborate-distribute-dashboards-reports.md)。

![[我的最愛儀表板] 清單中的共用圖示](media/service-share-dashboards/power-bi-share-dash-report-favorites.png)

不論是與組織內部或外部共用內容，您都會需要 [Power BI Pro 授權](service-features-license-type.md)。 您的收件者也需要 Power BI Pro 授權，除非該內容中[Premium 容量](service-premium-what-is.md)。 

您可以共用儀表板和報表從 Power BI 服務中的大部分位置：我的最愛、 最近、 與我共用 （如果擁有者允許的話），我的工作區或其他工作區。 當您與他人共用儀表板或報表時，他們可以檢視該儀表板或報表並與之互動，但無法編輯它們。 除非套用[資料列層級安全性 (RLS)](service-admin-rls.md)，否則他們將能看到和您在儀表板或報表中可看見的相同資料。 如果您允許的話，您與其共用儀表板或報表的同事，也可以與他們的同事共用。 組織外部人員可以人也檢視和互動儀表板或報表，但不能共用它。 

您也可以[從任何 Power BI 行動裝置應用程式共用儀表板](consumer/mobile/mobile-share-dashboard-from-the-mobile-apps.md)。 不過，您無法共用儀表板從 Power BI Desktop。

## <a name="video-share-a-dashboard"></a>影片：共用儀表板
觀看 Amanda 與她公司內外的同事共用儀表板。 然後遵循影片下方的逐步指示親自試試看。

<iframe width="560" height="315" src="https://www.youtube.com/embed/0tUwn8DHo3s?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

## <a name="share-a-dashboard-or-report"></a>共用儀表板或報表

1. 在儀表板或報表清單中，或是在開放的儀表板或報表中，選取 [共用]  ![共用圖示](media/service-share-dashboards/power-bi-share-icon.png)。

2. 在頂端的方塊中，輸入個人、通訊群組或安全性群組的完整電子郵件地址。 您無法共用動態通訊清單。 
   
   您可以與其位址在您組織外的人員共用，但是您會看到一則警告。
   
   ![外部共用的相關警告](media/service-share-dashboards/power-bi-share-dialog-warning.png) 
 
   >[!NOTE]
   >輸入的方塊支援，最多 100 個使用者或群組。 如果您需要有大量的使用者共用，請考慮建立工作區中的儀表板並[散發為應用程式](service-create-distribute-apps.md)。
   > 
   > 


3. 您可以視需要新增訊息。 這是選擇性的。
4. 若要讓同事與他人共用您的內容，請檢查**允許收件者共用您的儀表板 （或報表）** 。
   
   允許其他人共用稱為「再次共用」  。 如果您允許的話，他們就可以從 Power BI 服務和行動裝置應用程式再次共用，或將電子郵件邀請轉寄給組織中的其他人。 邀請有效期一個月。 組織外部人員無法再次共用。 身為內容擁有者，您可以關閉再次共用，或是個別撤銷再次共用的權限。 請參閱[停止共用或停止其他人共用](#stop-sharing-or-stop-others-from-sharing)。

5. 選取 [共用]  。
   
   ![選取 [共用] 按鈕](media/service-share-dashboards/power-bi-share-dialog-share.png)  
   
   Power BI 會傳送電子郵件邀請給個人，而非群組，以共用內容的連結。 您會看到「成功」  通知。 
   
   當組織內的收件者按一下連結時，Power BI 會將儀表板或報表新增至其 [與我共用]  清單頁面。 他們可以選取您的名稱，就能查看您已與他們共用的所有內容。 
   
   ![[與我共用] 清單頁面](media/service-share-dashboards/power-bi-shared-with-me-dashboards-reports.png)
   
   當組織外的收件者按一下連結時，他們會看到儀表板或報表，但不是在平常的 Power BI 入口網站中。 如需詳細資訊，請參閱 <<c0> [ 與組織外部人員共用儀表板或報表](#share-a-dashboard-or-report-with-people-outside-your-organization)。

## <a name="who-has-access-to-a-dashboard-or-report-you-shared"></a>有哪些人員可以存取您共用的儀表板或報表？
有時您需要查看您已共用，並查看他們已共用的人員：

1. 在儀表板或報表清單中，或是儀表板或報表本身當中，選取 [共用]  ![共用圖示](media/service-share-dashboards/power-bi-share-icon.png)。 
2. 在 **共用儀表板**或是**共用報表**對話方塊中，選取**存取**。
   
    ![[共用儀表板] 對話方塊的 [存取] 索引標籤](media/service-share-dashboards/power-bi-share-dialog-access.png)

    組織外部人員列為 [Guest]  。

## <a name="stop-sharing-or-stop-others-from-sharing"></a>停止共用或停止其他人共用
只有儀表板或報表擁有者可以開啟和關閉再次共用。

### <a name="if-you-havent-sent-the-sharing-invitation-yet"></a>如果您尚未傳送共用邀請
* 清除**允許收件者共用您的儀表板 （或報表）** 再將其傳送的邀請底部的核取方塊。

### <a name="if-youve-already-shared-the-dashboard-or-report"></a>如果您已共用儀表板或報表
1. 在儀表板或報表清單中，或是儀表板或報表本身當中，選取 [共用]  ![共用圖示](media/service-share-dashboards/power-bi-share-icon.png)。 
2. 在 **共用儀表板**或是**共用報表**對話方塊中，選取**存取**。
   
    ![[共用儀表板] 對話方塊的 [存取] 索引標籤](media/service-share-dashboards/power-bi-share-dialog-access.png)
3. 選取 [讀取並再次共用]  旁的省略符號 ( **...** )，然後選取：
   
   ![[讀取並再次共用] 的省略符號](media/service-share-dashboards/power-bi-change-access.png)
   
   * [讀取]  ，阻止該員與其他人共用。
   * [移除存取權]  ，使該人員完全看不到共用的內容。

4. 在 **移除存取權**對話方塊方塊中，決定您是否也想要移除相關的內容，例如報表和資料集的存取權。 如果您移除警告圖示的項目![Power BI 警告圖示](media/service-share-dashboards/power-bi-warning-icon.png)，建議您最好也移除相關的內容，因為它將無法正確顯示。

    ![Power BI 共用警告對話方塊](media/service-share-dashboards/power-bi-sharing-warning-dialog.png)

## <a name="share-a-dashboard-or-report-with-people-outside-your-organization"></a>與組織外部人員共用儀表板或報表
當您與外部人員共用您的組織時，他們會收到附有共用儀表板或報表，他們必須登入 Power BI 以查看連結的電子郵件。 如果沒有 Power BI Pro 授權，他們可以按一下連結來註冊以取得授權。

登入後，他們會看到共用儀表板或報表的瀏覽器視窗中，不是在平常的 Power BI 入口網站。 若要稍後存取此儀表板或報表，它們必須加入書籤連結。

他們無法編輯這個儀表板或報表中的任何內容。 雖然它們可以與圖表互動，並變更篩選或交叉分析篩選器，但無法儲存變更。 

只有您的直接收件者才能看到共用儀表板或報表。 例如，如果您傳送電子郵件給 Vicki@contoso.com，只有 Vicki 看得到儀表板。 有其他任何人可以看到 儀表板，即使對方沒有連結。 Vicki 必須使用相同的電子郵件地址來存取它;如果她註冊時使用任何其他的電子郵件地址，她就沒有存取權儀表板。

如果內部部署的 Analysis Services 表格式模型實作角色或資料列層級安全性，則組織外部人員就看不到任何資料。

如果您傳送的連結從 Power BI 行動裝置應用程式的人員組織外部，按一下連結會開啟儀表板瀏覽器中，在 Power BI 行動裝置應用程式中。

如果您[允許外部來賓使用者編輯和管理組織中的內容](service-admin-portal.md#export-and-sharing-settings)，僅限耗用量的體驗預設不會套用到它們。 [深入了解](service-admin-azure-ad-b2b.md)。

## <a name="limitations-and-considerations"></a>限制與考量
共用儀表板和報表時的重要事項︰

* 一般來說，您和您的同事會在儀表板或報表中看到相同的資料。 因此，如果您具有可看到較多資料的權限，您的同事將能在您的儀表板或報表中看到您所有的資料。 不過，如果已將[資料列層級安全性 (RLS)](service-admin-rls.md) 套用至儀表板或報表的基礎資料集，則系統會依據每個人的認證來決定其可以存取的資料。
* 共用您儀表板的每個人都可以看到它並與其互動中相關的報告[閱讀檢視](consumer/end-user-reading-view.md#reading-view)。 他們無法建立報表，或在現有的報表中儲存變更。
* 雖然沒有人可以看到或下載的資料集，他們可以在使用中進行分析 功能來直接存取資料集。 系統管理員可以限制能夠使用 在 Excel 的 分析 群組中的每個人。 不過，對於該群組中每個人的限制適用於該群組所屬的每個工作區。
* 每個人都可以手動[重新整理資料](refresh-data.md)。
* 如果電子郵件使用 Office 365，您可以輸入與通訊群組相關聯的電子郵件地址來與通訊群組的成員共用。
* 共用電子郵件網域內外的同事和其網域是不同、 但登錄在相同的租用戶內的同事可以與其他人共用儀表板。 例如，如果網域 contoso.com 和 contoso2.com 都登錄在相同的租用戶與您的電子郵件地址是konrads@contoso.com，則ravali@contoso.com和gustav@contoso2.com可以共用，只要經過您共用的權限。
* 如果您的同事已能存取特定儀表板或報表，您可以藉由在儀表板或報表時，請將複製 URL 中傳送的直接連結。 例如：`https://powerbi.com/dashboards/g12466b5-a452-4e55-8634-xxxxxxxxxxxx`
* 同樣地，如果您的同事已能存取特定儀表板，您可以[傳送基礎報表的直接連結](service-share-reports.md)。 
* 您可以共用，至多 100 位使用者或群組中的單一共用動作。 不過，您可以讓超過 500 個使用者存取某個項目。 若要這樣做，共用多次，藉由指定使用者的個別或與使用者群組，其中包含所有使用者共用。

## <a name="troubleshoot-sharing"></a>針對共用問題進行疑難排解

### <a name="my-dashboard-recipients-see-a-lock-icon-in-a-tile-or-a-permission-required-message"></a>我的儀表板收件者看到磚中出現鎖定圖示或「需要權限」的訊息

與您共用的人員在嘗試檢視報告時，可以看到儀表板中鎖定的圖格或「需要權限」訊息。

![Power BI 鎖定的圖格](media/service-share-dashboards/power-bi-locked_tile_small.png)

如果是這樣，您需要授與他們基礎資料集的權限：

1. 前往內容清單中的 [資料集]  索引標籤。

1. 選取省略符號 ( **...** ) 旁的資料集，然後選取**管理權限**。

    ![管理權限](media/service-share-dashboards/power-bi-sharing-manage-permissions.png)

1. 選取 [新增使用者]  。

    ![選取 [新增使用者]](media/service-share-dashboards/power-bi-share-dataset-add-user.png)

1. 輸入個人、通訊群組或安全性群組的完整電子郵件地址。 您無法共用動態通訊清單。

    ![新增電子郵件地址](media/service-share-dashboards/power-bi-add-user-dataset.png)


1. 選取 [加入]  。

### <a name="i-cant-share-a-dashboard-or-report"></a>我無法共用儀表板或報表

若要共用的儀表板或報表，您需要再次共用基礎內容; 權限也就是說，任何相關報表和資料集。 如果您看到訊息指出您無法共用，請詢問報表作者提供您再次共用這些報表和資料集的權限。

![「無法共用」訊息](media/service-share-dashboards/power-bi-sharing-unable-to-share.png)


## <a name="next-steps"></a>後續步驟
* 有任何意見嗎？ 請移駕 [Power BI 社群網站](https://community.powerbi.com/)提供您的建議。
* [應該如何共同作業和共用儀表板和報表？](service-how-to-collaborate-distribute-dashboards-reports.md)
* [共用已篩選的 Power BI 報表](service-share-reports.md)。
* 有問題嗎？ [試試 Power BI 社群](http://community.powerbi.com/)。


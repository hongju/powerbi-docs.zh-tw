---
title: 修正「公司 SSL 憑證不受信任」
description: 登入 Power BI for Android 應用程式時，您可能會看到訊息：「無法驗證，因為您的公司 SSL 憑證不受信任」
.": ''
author: mshenhav
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 05/18/2018
ms.author: mshenhav
ms.openlocfilehash: de103412e21e0d26d20058e2d4e1fb9a8a5449bf
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "61341337"
---
# <a name="fixing-corporate-ssl-certificate-is-untrusted---power-bi"></a>修正「公司 SSL 憑證不受信任」- Power BI
登入 Microsoft Power BI for Android 行動裝置應用程式時，您可能會看到訊息：「無法驗證，因為您的公司 SSL 憑證不受此裝置信任。 請連絡您的公司 IT 管理員。」 

您要採取的動作通常取決於 Android 裝置上的作業系統，但有幾個其他問題，可能會造成這個錯誤。

## <a name="on-android-7-or-later"></a>在 Android 7 或更新版本上
尋找名為 **Chrome** 的應用程式更新，並安裝更新。

## <a name="on-android-6-and-earlier"></a>在 Android 6 或更早版本上
您的裝置可能需要 System Webview 的更新版本。 它可能已安裝在您的裝置上，您只需要按一下 [更新]  。

如果 System Webview 未安裝在裝置上︰

1. 在您的 Android 裝置上，關閉 Power BI。
2. 開啟 [Google Play 商店] 並搜尋 Google Inc. 的 **System Webview**。
3. 安裝它。
4. 重新啟動 Power BI 應用程式，然後登入。

## <a name="time-zone-settings"></a>時區設定
裝置上的時區設定可能有誤。 

移至 [設定]   > [系統]   > [日期和時間]  檢查它們。

## <a name="custom-authentication-server"></a>自訂驗證伺服器
如果您使用自訂驗證伺服器，公司驗證伺服器在的 SSL 憑證可能無效。 請與您組織的 IT 合作，依照[此文章](https://support.microsoft.com/en-us/help/3203929/using-adal-to-authenticate-from-android-devices-fails-if-additional-ce)中的指導方針測試公司驗證伺服器設定。

## <a name="next-steps"></a>後續步驟
* 從 Android App Store [下載 Android 應用程式](http://go.microsoft.com/fwlink/?LinkID=544867)。
* 有問題嗎？ [嘗試在 Power BI 社群提問](http://community.powerbi.com/) 


---
description: Adobe Experience Platform Auditor 常見問題與解答
seo-description: Adobe Experience Platform Auditor 常見問題與解答
seo-title: Adobe Experience Platform Auditor 常見問題集
title: Adobe Experience Platform Auditor 常見問題集
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 71%

---


# Adobe Experience Platform Auditor 常見問題集{#auditor-faq}

本文將為 Adobe Experience Platform Auditor 的相關常見問題提供答案。

* [什麼是Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [我的公司是否符合使用Platform Auditor的資格？](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Platform Auditor會評分哪些Adobe技術？](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [我可以執行多少次稽核？](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [稽核時會進行何種編目？](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [稽核需要多久的時間？](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [報表中提供哪些資訊？](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [這些資訊有何功用？](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Platform Auditor可以稽核非Adobe技術嗎？](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [我能否核准 IP 位址以允許掃描頁面…](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Platform Auditor是否使用與Observepoint相同的IP範圍？](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## 什麼是Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor是Adobe Experience Cloud的一項服務，與ObservePoint共同開發，後者是驗證數位實作的專家。

有了Platform Auditor，客戶一次最多可掃描500個網頁，並收到報告，說明如何改善其Adobe Experience Cloud實作，以獲得Adobe投資的全部價值。

## Am I eligible to use Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

所有Adobe Experience Cloud客戶組織都可免費存取Platform Auditor（自2018年5月1日起）。 每個使用者都必須先同意 Adobe Experience Cloud UI 中的 Adobe/ObservePoint 使用條款，才能存取其功能。若要選擇退出條款，請聯絡客戶經理。

## How do I access Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. 您也可以直接前往 [https://auditor.adobe.com](https://auditor.adobe.com)。

## Which Adobe technologies does Platform Auditor grade? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID 服務 (先前稱為 Marketing Cloud ID 服務)
* Target

下列 Adobe 解決方案目前未包含在測試規則中。這些解決方案的支援預計會在未來的更新提供。

* Advertising Cloud Creative
* Audience Manager
* 促銷活動
* Adobe Experience Platform Launch

## 我可以執行多少次稽核？{#section-caac1e50ce1249aeba76308f3ef03fa0}

您可執行的稽核並沒有數量上的限制。使用者一次只能執行一項稽核。如果您嘗試執行的稽核使用與執行中的稽核相同的設定，則會發生錯誤。

## 稽核時會進行何種編目？{#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint 技術目前會對在檔案連結中找到的 URL 進行編目。對於在按鈕、分頁 Widget 和其他這類頁面元素中找到的連結，並不會進行編目。

## How do I suggest new criteria for Platform Auditor tests? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 稽核需要多久的時間？{#section-5086ae27ef1f4671a9d951348654633a}

完成稽核的所需時間取決於許多因素，包括：

* 頁面載入時間

   ObservePoint 引擎會在瀏覽器中載入稽核的每個頁面。頁面載入的速度越快，稽核就能越快完成。
* 同時間的連線

   Platform Auditor使用單一連線來瀏覽每個頁面。 完整的 ObservePoint 帳戶一次最多可使用 10 個引擎。
* 網路靜默

   每個頁面載入後，稽核會先等待歷時 7 秒的網路靜默，再繼續前往下一頁。如果頁面傳送了會在頁面載入後執行的大量網路請求，則會在等待 60 秒後逾時。
* 頁面重試

   如果找不到某個頁面或標記，稽核會先儲存該 URL，稍後再回過頭加以稽核。稽核最多會瀏覽一個頁面三次，以確定錯誤並非由暫時性的問題造成。
* 正在處理

   稽核執行後，其收集到的所有資料會透過規則進行處理和篩選。這項處理頗耗時，但不像掃描本身需要那麼久的時間。

>[!NOTE]
>
>Platform Auditor一次運行一次掃描。 完整的 ObservePoint 帳戶可以連續執行許多稽核。

## 報表中提供哪些資訊？{#section-752d6b82f6744a3182c4ce16ea6b5d3f}

每次掃描都會產生一份報表，顯示已掃描的 URL、在這些網頁上發現的問題，以及如何更正這些問題的建議。

掃描的結果可細分為三種類別：

* 設定
* 標記一致性
* 標記是否存在

除了這三個類別以外，報表還提供警報，其中包含您應注意但不一定需要立即處理的資訊。

來自這些類別的建議，可再進一步細分為三種類別：

* 強烈建議
* 建議
* 略過

## 這些資訊有何功用？{#section-9308c1ea882048b781087ae6d2eee9f0}

透過Platform Auditor提供的所有建議皆旨在協助您採取行動，以解決您實作Adobe Experience Cloud解決方案時的問題，例如DTM或Target。 為了促進這一點，Platform Auditor團隊已廣泛工作，以提供非常詳細的說明，說明在何處需要做什麼。 您可以匯出所有已掃描的 URL 和所有測試結果的試算表，以便輕鬆找出問題的領域。下列範例說明 DTM 實施的一項建議：

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom 回呼置於最後</b> </p> <p>必須要有 _satellite.pageBottom() 函數才能正確實施 DTM。在結尾的 &lt;/body&gt; 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Can Platform Auditor audit non-Adobe technology? {#section-f6e73c56083b4815bbf901296038bcd4}

不會。不過，ObservePoint 的完整方案可讓客戶稽核並監視所有行銷標記和技術。身為 Adobe 客戶，您可以存取免費試用帳戶。To access your trial account visit [ObservePoint’s Platform Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## 我能否核准 IP 位址，以允許掃描受登入機制保護的頁面？{#section-011e4f54c58140ffb93bedeb0745b6cc}

目前，若無完整的 ObservePoint 方案，即不支援此功能。

## Does Platform Auditor use the same IP ranges as ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

編目由 ObservePoint 執行，因此會使用相同的 IP 位址。

如需詳細資訊，請參閱 [ObservePoint 文件](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list)。

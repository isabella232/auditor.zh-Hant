---
description: Adobe Experience Platform Auditor 常見問題與解答
seo-description: Adobe Experience Platform Auditor 常見問題與解答
seo-title: Adobe Experience Platform Auditor 常見問題集
title: Adobe Experience Platform Auditor 常見問題集
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: ht
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: ht
source-wordcount: '990'
ht-degree: 100%

---


# Adobe Experience Platform Auditor 常見問題集{#auditor-faq}

本文將針對 Adobe Experience Platform Auditor 的常見問題提供答案。

* [什麼是 Adobe Experience Platform Auditor？](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [我的公司是否符合使用 Platform Auditor 的資格？](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Platform Auditor 會對哪些 Adobe 技術評分？](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [我可以執行多少次稽核？](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [稽核時會進行何種編目？](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [稽核需要多久的時間？](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [報表中提供哪些資訊？](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [這些資訊有何功用？](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Platform Auditor 是否可稽核 Adobe 以外的技術？](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [我能否核准 IP 位址以允許掃描頁面...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Platform Auditor 使用的 IP 範圍是否與 ObservePoint 相同？](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## 什麼是 Adobe Experience Platform Auditor？{#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor 是 Adobe Experience Cloud 的一項服務，由 Adobe 與數位實作驗證的專家 ObservePoint 共同開發而成。

透過 Platform Auditor，客戶一次最多可掃描 500 個網頁，並取得報表，了解如何改善其 Adobe Experience Cloud 實作，使其 Adobe 投資充分發揮效益。

## 我是否符合使用 Platform Auditor 的資格？{#section-f90094050d1e44929066a942833435cf}

自 2018 年 5 月 1 日起，所有 Adobe Experience Cloud 客戶組織都可免費存取 Platform Auditor。使用者都必須先同意 Adobe Experience Cloud UI 中的 Adobe/ObservePoint 使用條款，才能存取其功能。若要選擇終止條款，請連絡客戶經理。

## 如何存取 Platform Auditor？{#section-531ff85f94384831a89cbb4109549daf}

登入 [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) 後，按一下頂端導覽區塊的&#x200B;**[!UICONTROL 「啟動」]**&#x200B;即可找到 Platform Auditor。您也可以直接前往 [https://auditor.adobe.com](https://auditor.adobe.com)。

## Platform Auditor 會對哪些 Adobe 技術評分？{#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID 服務 (先前稱為 Marketing Cloud ID 服務)
* Target

下列 Adobe 解決方案目前未包含在測試規則中。這些解決方案的支援預計會在未來的更新提供。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch

## 我可以執行多少次稽核？{#section-caac1e50ce1249aeba76308f3ef03fa0}

您可執行的稽核並沒有數量上的限制。使用者一次只能執行一項稽核。如果您嘗試執行的稽核使用與執行中的稽核相同的設定，則會發生錯誤。

## 稽核時會進行何種編目？{#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint 技術目前會對在檔案連結中找到的 URL 進行編目。對於在按鈕、分頁 Widget 和其他這類頁面元素中找到的連結，並不會進行編目。

## 如何為 Platform Auditor 測試提出建議的新標準？{#section-926e6ef9225b4f0bb19c2927d634cd77}

您可以按一下以下頁面中的&#x200B;**[!UICONTROL 「分享意見」]**，透過 Platform Auditor 社群提交測試建議：[https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 稽核需要多久的時間？{#section-5086ae27ef1f4671a9d951348654633a}

完成稽核的所需時間取決於許多因素，包括：

* 頁面載入時間

   ObservePoint 引擎會在瀏覽器中載入稽核的每個頁面。頁面載入的速度越快，稽核就能越快完成。
* 同時間的連線

   Platform Auditor 會使用單一連線來瀏覽每個頁面。完整的 ObservePoint 帳戶一次最多可使用 10 個引擎。
* 網路靜默

   每個頁面載入後，稽核會先等待歷時 7 秒的網路靜默，再繼續前往下一頁。如果頁面傳送了會在頁面載入後執行的大量網路請求，則會在等待 60 秒後逾時。
* 頁面重試

   如果找不到某個頁面或標記，稽核會先儲存該 URL，稍後再回過頭加以稽核。稽核最多會瀏覽一個頁面三次，以確定錯誤並非由暫時性的問題造成。
* 正在處理

   稽核執行後，其收集到的所有資料會透過規則進行處理和篩選。這項處理頗耗時，但不像掃描本身需要那麼久的時間。

>[!NOTE]
>
>Platform Auditor 每次只會執行一項掃描作業。完整的 ObservePoint 帳戶可以連續執行許多稽核。

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

Platform Auditor 提供的所有建議，都是為了協助您採取因應動作，以解決您在實作 Adobe Experience Cloud 解決方案 (例如 DTM 或 Target) 時所發生的問題。為此，Platform Auditor 團隊已就各方面提供詳盡的指示，說明相關情況下的必要措施。您可以匯出所有已掃描的 URL 和所有測試結果的試算表，以便輕鬆找出問題的領域。下列範例說明 DTM 實作的一項建議：

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom 回呼置於最後</b> </p> <p>必須要有 _satellite.pageBottom() 函數才能正確實作 DTM。在結尾的 &lt;/body&gt; 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Platform Auditor 是否可稽核 Adobe 以外的技術？{#section-f6e73c56083b4815bbf901296038bcd4}

否。不過，ObservePoint 的完整方案可讓客戶稽核並監視所有行銷標記和技術。身為 Adobe 客戶，您可以存取免費試用帳戶。若要存取試用帳戶，請造訪 [ObservePoint 的 Platform Auditor 頁面](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium)。

## 我能否核准 IP 位址，以允許掃描受登入機制保護的頁面？{#section-011e4f54c58140ffb93bedeb0745b6cc}

目前，若未使用完整的 ObservePoint 方案，即不支援此功能。

## Platform Auditor 使用的 IP 範圍是否與 ObservePoint 相同？{#section-39512b156e194787981bdd572ff5b5a9}

編目由 ObservePoint 執行，因此會使用相同的 IP 位址。

如需詳細資訊，請參閱 [ObservePoint 文件](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list)。

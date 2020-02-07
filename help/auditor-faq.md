---
description: 'null'
seo-description: 'null'
seo-title: Auditor 常見問題集
title: Auditor常見問答集
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Auditor常見問答集{#auditor-faq}

本文包含有關Adobe Experience Platform Auditor的常見問題解答。

* [什麼是Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [我的公司是否符合使用Auditor的資格？](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Auditor會評分哪些Adobe技術？](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [我可以執行多少次審計？](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [審計需要編寫什麼？](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [審計需要多久？](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [報表中提供哪些資訊？](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [這些資訊有何可行性？](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Auditor可以稽核非Adobe技術嗎？](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [我是否可將我的IP位址列入白名單，以允許掃描頁面……](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Auditor是否使用與Observepoint相同的IP範圍？](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## 什麼是Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor是Adobe Experience cloud的一項服務，與ObservePoint共同開發，後者是驗證數位實作的專家。

使用Auditor，客戶一次最多可掃描500個網頁，並收到報告，說明如何改善其Adobe Experience cloud實作，以獲得Adobe投資的全部價值。

## 我是否符合使用Auditor的資格？ {#section-f90094050d1e44929066a942833435cf}

所有Adobe Experience cloud客戶組織都可免費存取Auditor（自2018年5月1日起）。 每位使用者必須先同意Adobe Experience Cloud UI中的Adobe/ObservePoint使用條款，才能存取該功能。 若要選擇退出條款，請連絡您的客戶經理。

## 我要如何存取Auditor? {#section-531ff85f94384831a89cbb4109549daf}

登入 [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) 後，按一下頂端導覽的&#x200B;**[!UICONTROL 「啟動」]**&#x200B;即可找到 Auditor。您也可以直接前往 [https://auditor.adobe.com](https://auditor.adobe.com)。

## Auditor會評分哪些Adobe技術？ {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising cloud搜尋
* Analytics
* DTM
* Experience Cloud ID服務（先前稱為Marketing Cloud ID服務）
* Target

下列Adobe解決方案目前不包含在測試規則中。 預計未來將會針對這些解決方案提供支援。

* Advertising Cloud Creative
* Audience Manager
* 促銷活動
* Launch

## 我可以執行多少次審計？ {#section-caac1e50ce1249aeba76308f3ef03fa0}

您可以執行的稽核數目沒有限制。 使用者只能一次執行一次審核。 如果您嘗試使用與正在運行的審計相同的設定啟動審計時，將發生錯誤。

## 審計需要編寫什麼？ {#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint技術目前會編目檔案連結中的URL。 按鈕、分頁介面工具集和其他這類頁面元素中的連結不會編目。

## 我要如何為Auditor測試提出新標準？ {#section-926e6ef9225b4f0bb19c2927d634cd77}

您可以按一下本頁面中的&#x200B;**[!UICONTROL 「分享意見」]**，透過 Auditor 社群提交測試建議：[https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 審計需要多久？ {#section-5086ae27ef1f4671a9d951348654633a}

導致審計完成所需時間的因素有很多，包括：

* 頁面載入時間

   ObservePoint引擎會在瀏覽器中載入稽核的每個頁面。 頁面載入的速度越快，稽核完成的速度就越快。
* 同時連接

   Adobe Auditor使用單一連線來瀏覽每個頁面。 完整的ObservePoint帳戶一次最多使用10個引擎。
* 網路靜默

   每個頁面載入後，稽核會等待7秒的網路靜默，再繼續前往下一頁。 如果頁面傳送大量在頁面載入後發生的網路要求，等待會在60秒後逾時。
* 頁面重試次數

   如果找不到頁面或標籤，稽核會儲存該URL，並在稍後的稽核中傳回該URL。 稽核最多會瀏覽一個頁面三次，以確定錯誤不是由暫時性問題造成。
* 正在處理

   執行審核後，系統會處理並篩選其收集到的所有資料。 此處理時間很長，但不像掃描本身那麼花費時間。

>[!NOTE]
>
>Adobe Auditor一次執行單一掃描。 完整的ObservePoint帳戶可以連續執行許多稽核。

## 報表中提供哪些資訊？ {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

每次掃描都會產生一份報表，顯示已掃描的URL、這些網頁上發現的問題，以及如何修正發現的問題的建議。

掃描結果分為三類：

* 設定
* 標籤一致性
* 標籤存在

除了這三個類別外，報表還提供警報，其中包含您應該知道但不一定需要立即行動的資訊。

然後，這些類別中的建議又分為三個類別：

* 強烈建議
* 建議
* 通過

## 這些資訊有何可行性？ {#section-9308c1ea882048b781087ae6d2eee9f0}

透過Auditor提供的所有建議皆可協助您採取行動，以解決您實作Adobe Experience cloud解決方案時的問題，例如DTM或Target。 為了促進這一點，審計員團隊已廣泛開展工作，就需要在何處做什麼提供非常詳細的說明。 您可以匯出已掃描的所有URL和所有測試結果的試算表，以便輕鬆找出問題區域。 以下是DTM實作的一個建議範例：

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom回呼最後一次</b> </p> <p>正確的DTM實作需要_satellite.pageBottom()函式。 在結束&lt;/body&gt;標籤前立即新增內嵌指令碼，以確保正確的DTM功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auditor可以稽核非Adobe技術嗎？ {#section-f6e73c56083b4815bbf901296038bcd4}

不會。不過，ObservePoint的完整方案可讓客戶審核並監控所有行銷標籤和技術。 身為Adobe客戶，您可以存取免費試用帳戶。 若要存取您的試用帳戶，請 [造訪ObservePoint的Auditor頁面](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)。

## 我是否可將我的IP位址列入白名單，以允許掃描受登入保護的頁面？ {#section-011e4f54c58140ffb93bedeb0745b6cc}

目前不支援此功能，但未提供完整的ObservePoint產品。

## Auditor是否使用與ObservePoint相同的IP範圍？ {#section-39512b156e194787981bdd572ff5b5a9}

搜索由ObservePoint執行，因此使用相同的IP地址。

如需詳細 [資訊，請參閱](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ObservePoint檔案。

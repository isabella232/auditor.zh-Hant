---
description: 包含篩選器可限制審核可從「開始URL」編目的連結。 排除篩選器可防止審計搜索連結。
seo-description: 包含篩選器可限制審核可從「開始URL」編目的連結。 排除篩選器可防止審計搜索連結。
seo-title: 包含和排除篩選
title: 包含和排除篩選
uuid: 477fc38c-7351-42dd-8209-2fb7549ee34c
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 包含和排除篩選{#include-and-exclude-filters}

包含篩選器可限制審核可從「開始URL」編目的連結。 排除篩選器可防止審計搜索連結。

<!--
Content from ObservePoint (https://help.observepoint.com/articles/2872121-include-and-exclude-filters) with their permission. Modified slightly for style and Auditor emphasis.
-->

「包含篩選」和「排除篩選」提供稽核准則。 將「包含」和「排除」篩選保留為空，審核可以從「開始URL」的連結開始，編目它所遇到的任何連結。

![](assets/filter.png)

透過套用「包含」篩選器、「排除」篩選器或兩者的組合，可提供稽核可編目之連結的相關指示。

「包含篩選器」欄位中的任何項目都會限制掃描僅顯示符合該項目的頁面。 「排除篩選」欄位中的任何項目都會防止掃描任何符合該項目的頁面。

「包含」和「排除」篩選器可以是完整URL、部分URL或符合有效頁面的規則運算式。

## 優先順序 {#section-e9d42419dd3f459bb20e7a33c6104f12}

1. **開始URL** 優先於其他所有項目，而且在稽核期間一律會進行瀏覽，即使URL符合「排除」篩選器中的項目亦然。 「開始URL」一律會先於其他URL進行瀏覽。

   ![](assets/startingpage.png)

   在上述影像中，稽核會從起始頁面的屬性中搜尋 `document.links` 連結。 這些連結可由稽核掃描。

1. **包含URL** 必須從起始頁面連結，否則將無法搜尋，也不會瀏覽。

   ![](assets/includefilter.png)

   在上述影像中，新增「包含」篩選器會限制符合篩選條件的URL。 現在只有5個連結符合審核掃描的資格。

1. **排除URL** ，會排除符合資格的連結。

   ![](assets/excludefilter.png)

   在上述影像中，新增「排除」篩選會防止合格連結的URL。 現在，審核只有三個連結符合掃描的資格。

## 啟動URL {#section-ccb46abcd96f4a8ab171245015d2b724}

Auditor需要單一頁面才能使用「開始URL」。 「開始URL」一律會先於其他URL進行瀏覽。 從開始頁面搜尋的任何連結都符合瀏覽的資格，但須受「包含」和「排除」篩選條件所限。 如果「排除」項目與「開始URL」相符，則會忽略該項目。

## 包含篩選 {#section-7626060a56a24b658f8c05f031ac3f5f}

「包含」篩選器可限制哪些連結符合在審核期間進行掃描的資格。 包含篩選器可以：

* 完全限定的URL
* 部分URL
* 符合完整或部分URL的規則運算式
* 上述任何組合

將URL或規則運算式新增至「包含」篩選器並不保證稽核中會掃描這些特定URL。 稽核會檢查「開始URL」上的連結，然後導覽至符合資格的連結。 稽核會持續進行此檢查和導覽程式，直到達到500個掃描URL的限制，或直到找不到更符合資格的連結為止。

>[!NOTE]
>
>在某些情況下，完成500頁掃描可能需要48小時。

依預設，稽核會掃描起始URL的所有子網域。 除非透過提供包含篩選器明確覆寫，否則掃描將使用下列regex include篩選器：

`^https?://([^/:\?]*\.)?mysite.com`

這樣，「開始URL」頁面上找到的任何連結都符合瀏覽的資格。 它與「開始URL」中任何子網域上的任何頁面相符。

使用預設的「包含」篩選器可提供廣泛範圍，供稽核進行編目。 若要在特定區段或頁面上返回首頁，請在此方塊中新增篩選器，以提供您審核的特定指示。 在這種情況下，請將預設值替換為希望審計掃描的目錄。 您也可以使用包含篩選器來執行跨網域稽核，您需要在一個網域上開始稽核，並在另一個網域上結束。 若要這麼做，請輸入您要遍歷的網域。 無論如何，若要找到任何「包含篩選器URL」，必須在已稽核的頁面上進行搜尋。

「包含篩選器」可包含精確的URL、部分URL或規則運算式。 例如，如果「開始URL」為 [!DNL http://mysite.com]預設值，則下列頁面符合掃描的資格（請注意粗體字元）:

```
http://mysite.com
http
<b>s</b>://mysite.com
http://
<b>www</b>.mysite.com/home
http://
<b>dev</b>.mysite.com/home
http://
<b>my</b>.mysite.com/products/products_and_services.html
```

對於複雜的URL模式，請使 [用ObservePoint的規則運算式測試程式](http://regex.observepoint.com/)。

有關常見模式匹 [配使用案例，請參閱ObservePoint文檔的通用規則運算式](https://help.observepoint.com/articles/2872116-common-regular-expressions-for-observepoint) 。

## 排除篩選器 {#section-00aa5e10c878473b91ba0844bebe7ca9}

「排除」篩選器會防止URL被稽核。 您可以使用精確的URL、部分URL或規則運算式。 不會造訪任何符合「排除」篩選條件中項目的URL。 如果您的「開始URL」已包含在「排除」篩選器中，則不會排除它。 「開始URL」一律會由稽核掃描。

## 測試篩選器和URL {#section-3cfa125b1756411395a64701e128efa0}

您可以在Auditor中測試您的篩選器和URL。

在建立稽核時，按一下「測 **[!UICONTROL 試進階篩選」]**。 輸入您的篩選器和URL，然後按一下「 **[!UICONTROL 套用]**」。

![](assets/test-advanced-filters.png)

## ObservePoint檔案 {#section-79cdc8e850d047969b6d2badf6bbd6f9}

本文是與ObservePoint合作開發的。 有關最新資訊，請參閱 [ObservePoint文檔](https://help.observepoint.com/articles/2872121-include-and-exclude-filters)。

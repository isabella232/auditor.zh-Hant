---
description: 此參考提供Adobe Experience Platform Auditor針對標籤存在所執行測試的詳細資訊。
seo-description: 此參考提供Adobe Experience Platform Auditor針對標籤存在所執行測試的詳細資訊。
seo-title: 標記是否存在
title: 標記是否存在
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 79%

---


# 標記是否存在

此參考提供Adobe Experience Platform Auditor針對標籤存在所執行測試的詳細資訊。

Platform Auditor會評估標籤是否存在，以及它是否在您的頁面程式碼中位於正確的位置。

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 測試 </th> 
   <th colname="col2" class="entry"> 標準 </th> 
   <th colname="col3" class="entry"> 建議 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - 程式碼是否存在</b> </p> <p>權重：5 </p> </td> 
   <td colname="col2"> <p> Advertising Cloud 標記無法在 DOM 中使用。 </p> </td> 
   <td colname="col3"> <p>使用Adobe Experience Platform Launch的Advertising Cloud擴充功能實作Advertising Cloud標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - 實施區段像素</b> </p> <p>權重：5 </p> </td> 
   <td colname="col2"> <p> 將您的 Advertising Cloud 區段像素升級為新的 Advertising Cloud 僅限影像標記。使用過時的 AMO 區段標記可能會導致資料遺失。 </p> </td> 
   <td colname="col3"> <p>使用Advertising Cloud的Platform Launch擴充功能實作Advertising Cloud細分像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - 在 DOM 中載入</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 未偵測到 Adobe Analytics 標記。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Analytics。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - 載入程式庫</b> </p> <p>權重：5 </p> <p>其他資訊: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/admin/c-troubleshooting.html" format="html" scope="external">DTM 疑難排解</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 新增頁首與頁尾程式碼</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> 在 DOM 中找不到全域_satellite 物件。Dynamic Tag Management 未安裝或無法執行。 </p> </td> 
   <td colname="col3"> <p>確認已在頁面上實施 DTM 程式庫，且後續指令碼活動不會加以封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - 單一內嵌程式碼</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 生產網站應載入一個 DTM 程式庫即可。 </p> </td> 
   <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom 回呼存在於 &lt;body&gt; 中</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面的 <span class="codeph">&lt;body&gt;</span> 內找不到 Dynamic Tag Management 所需的 <span class="codeph">_satellite.pageBottom()</span> 回呼。 </p> <p>如果在頁面上完全找不到 <span class="codeph">pageBottom</span> 呼叫，或該呼叫位於 <span class="codeph">&lt;head&gt;</span> 標記中 (或其他非預期的位置)，則此測試不會通過。只有在 <span class="codeph">pageBottom</span> 位於 <span class="codeph">&lt;body&gt;</span> 標記內的某處時，測試才會通過。如果完全不在頁面上，則無法運作，且其他兩個 <span class="codeph">pageBottom</span> 測試也不會通過。 </p> </td> 
   <td colname="col3"> <p>在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - 引發 pageBottom 標記</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 未偵測到 DTM <code> pageBottom</code> 標記。 </p> <p>如果呼叫位於 <code> if</code> 陳述式內而產生類似於 <code> if (false) {_satellite.pageBottom()}</code> 的行為，就會發生此狀況。因此，儘管標記可能存在且已正確放置，仍可能無法引發。 </p> </td> 
   <td colname="col3"> <p>在每個頁面上安裝 DTM <code> pageBottom</code> 呼叫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - 程式碼是否存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/id-service/using/intro/overview.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>找不到 Experience Cloud ID 服務程式碼。強烈建議使用 Experience Cloud ID (MCID) 以確保能夠充分發揮 Experience Cloud 解決方案的效益，且其對於 Experience Cloud 解決方案的 ID 管理而言十分重要。 </p> </td> 
   <td colname="col3"> <p> 安裝最新版的 MCID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - Cookie 是否存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/tools/macid.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 找不到 <span class="codeph">AMCV_</span> Cookie。您必須從 <span class="codeph">VisitorAPI.js</span> 程式碼將訪客物件具現化。 </p> </td> 
   <td colname="col3"> <p> 如果這是 DTM 實施，請確認已在 MCID 工具中正確輸入 AdobeOrg ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - 有 MID 值存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/id-service/using/intro/cookies.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在 <span class="codeph">AMCV_</span> Cookie 中找不到 MID 值。 </p> </td> 
   <td colname="col3"> <p>再次測試以確認是否有任何 MCID API 延遲。若持續發生此狀況，請聯絡 Adobe 客戶服務。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 載入程式庫</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在 DOM 中找不到全域_satellite 物件。平台啟動未安裝或無法執行。 </p> </td> 
   <td colname="col3"> <p>確認平台啟動程式庫已建置在頁面上，且未遭後續指令碼活動封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 沒有多個內嵌指令碼</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>頁面上不應載入多個內嵌指令碼。生產網站只應載入一個平台啟動程式庫。 </p> </td> 
   <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom 回呼存在於 &lt;body&gt; 中</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellite.pageBottom()</span> callback was not found within the <span class="codeph"> &lt;body&gt;</span> of the page, which is required by Platform Launch. </p> <p>如果在頁面上完全找不到 <span class="codeph">pageBottom</span> 呼叫，或該呼叫位於 <span class="codeph">&lt;head&gt;</span> 標記中 (或其他非預期的位置)，則此測試不會通過。只有在 <span class="codeph">pageBottom</span> 位於 <span class="codeph">&lt;body&gt;</span> 標記內的某處時，測試才會通過。如果完全不在頁面上，則無法運作，且其他兩個 <span class="codeph">pageBottom</span> 測試也不會通過。 </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper Platform Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 進行非同步部署時，pageBottom 回呼不應存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>The <span class="codeph"> _satellite.pageBottom()</span> callback was found on the page, which should not be the case when Platform Launch is asynchronously deployed. </p> </td> 
   <td colname="col3"> <p>Remove the<span class="codeph"> _satellite.pageBottom()</span> script to enable proper Platform Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 程式碼是否存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>Target 應定義於 DOM 中。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Target (at.js)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Target - 在 &lt;head&gt; 中載入程式庫</b> </p> <p>權重：4 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> Target 程式庫應載入 <span class="codeph">&lt;head&gt;</span> 標記中。 </p> </td> 
   <td colname="col3"> <p> 確認 Target 程式庫已載入 <span class="codeph">&lt;head&gt;</span> 標記中。 </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: 此參考提供Adobe Experience Platform Auditor針對測試所顯示警報的詳細資訊。
seo-description: 此參考提供Adobe Experience Platform Auditor針對測試所顯示警報的詳細資訊。
seo-title: 警報
title: 警報
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 70%

---


# 警報{#alerts}

此參考提供Adobe Experience Platform Auditor針對測試所顯示警報的詳細資訊。

警報會顯示您應留意但不影響分數的問題。這些最佳實務建議在某些情況下可能不適用於您的實施。

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 測試 </th> 
   <th colname="col2" class="entry"> 標準 </th> 
   <th colname="col3" class="entry"> 建議 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 實施正確的轉換標記</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>檢查是否使用正確的轉換標記。 </p> <p> <p>警告：使用過時的 TubeMogul 轉換標記，可能導致資料遺失。 </p> </p> </td> 
   <td colname="col3"> <p>將您的轉換像素升級為新的 Advertising Cloud 僅限影像轉換標記。 </p> <p>透過適用於Adobe Experience Platform Launch的Advertising Cloud擴充功能，您最容易完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 使用正確的 JS 標記</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 應使用最新的 JavaScript 標記。 </p> </td> 
   <td colname="col3"> <p>將您的 Advertising Cloud JavaScript 升級至最新版本。使用過時的 JavaScript 版本可能會導致功能失效。 </p> <p>透過使用Advertising Cloud擴充功能的Platform Launch，您可更輕鬆地完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 僅限影像標記</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 影像像素格式應符合下列其中一個建議格式： </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>將您的 Advertising Cloud 像素升級至新的 Advertising Cloud 僅限影像標記，以確保您使用的是完整的 Advertising Cloud 功能。 </p> <p>透過適用於Platform Launch的Advertising Cloud擴充功能，最輕鬆地完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 啟用區段像素 DSP 同步</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>檢查 TubeMogul 區段像素是否包含「DSP 同步」設定，並建議您將該設定新增至像素。 </p> <p>「DSP 同步」設定取決於查詢字串參數的使用，因此 </p> <p>如果對 <span class="codeph">("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph">"http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph">"http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>引發標記，且該標記包含 URL 參數 <span class="codeph">"sid=")</span>， </p> <p>則應確認 URL 參數 <span class="codeph">"cs=0"</span> 或 <span class="codeph">"cs=1"</span> 是否存在；若不存在，則建議將 <span class="codeph">"cs=1"</span> 新增至這些像素，以提高投放對象準確率。 </p> </td> 
   <td colname="col3"> <p> 將 URL 參數 <span class="codeph">"cs=1"</span> 新增至 Advertising Cloud 像素，以便進行 DSP 同步，進而提高投放對象準確率。 </p> <p>Advertising Cloud的Launch擴充功能可讓您輕鬆完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - pageBottom 回呼位置</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management 需要 <span class="codeph">_satellite.pageBottom()</span> 函數。在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> <p> <p>注意：最佳實務是讓該標記成為 <span class="codeph">&lt;body&gt;</span> 中的<i>最後一個</i>標記。若將其置於 <span class="codeph">&lt;body&gt;</span> 標記內，雖然或許能運作，但由於這並非最佳實務，因此其運作可能會不正確，或產生非預期或不適當的結果。 </p> </p> </td> 
   <td colname="col3"> <p>在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 自行託管</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/client-side-information.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> DTM 程式庫在 Adobe 的 Akamai 執行個體上受到託管 (網址是 <span class="filepath">assets.adobedtm.com</span>)。 </p> <p> 自行託管是載入 DTM 的建議方法，因為此方法可讓您透過快取控制進一步掌控網站效能、減少對第三方指令碼的依賴，且更能掌握發佈程序。您可以透過自己的網站託管或 CDN 來託管及管理 DTM 程式庫。 </p> </td> 
   <td colname="col3"> <p>自行託管是在頁面上載入 DTM 的建議方法。雖然透過 Akamai CDN 進行 DTM 託管在多數情況下都是可行的，但自行託管可以改善頁面效能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - 僅使用一個 AdobeOrg</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/id-service/using/intro/id-request.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>在一般 MCID 實施中，應使用單一 AdobeOrg。 </p> </td> 
   <td colname="col3"> <p>驗證此實施有多個 AdobeOrg ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom 回呼位置</b> </p> <p>權重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> 其他資訊</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Platform Launch should have a <span class="codeph"> pageBottom </span>callback function defined last in the body of the page if synchronously deployed. </p> <p> <p>注意：最佳實務是讓該標記成為 <span class="codeph">&lt;body&gt;</span> 中的<i>最後一個</i>標記。若將其置於 <span class="codeph">&lt;body&gt;</span> 標記內，雖然或許能運作，但由於這並非最佳實務，因此其運作可能會不正確，或產生非預期或不適當的結果。 </p> </p> </td> 
   <td colname="col3"> <p>Platform Launch requires the <span class="codeph"> _satellite.pageBottom()</span> function for synchronous deployments. Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper Platform Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 自行託管</b> </p> <p>權重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Adobe Experience Platform Launch快速入門</a> </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> 平台啟動非同步部署</a> </p> </td> 
   <td colname="col2"> <p>The Platform Launch library is being hosted on Adobe's Akamai instance at <span class="filepath"> assets.adobedtm.com</span>. </p> <p>自我托管是載入Platform Launch的建議方法，因為它可透過快取控制、降低協力廠商指令碼相依性，以及更完善的發佈程式控制，提供對網站效能的更大控制。 Platform Launch程式庫可透過您自己的Web代管或CDN來代管和管理。 </p> </td> 
   <td colname="col3"> <p>雖然透過Akamai CDN進行Platform Launch代管在大多數情況下都能運作，但建議將自行托管作為改善頁面效能的第一步。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 應以非同步方式部署</b> </p> <p>權重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>平台啟動應非同步部署，以獲得最佳效能。 </p> </td> 
   <td colname="col3"> <p>在內嵌指令碼中加入async參數，以確保正確的非同步平台啟動功能 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault 中的內容</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 使用 at.js 時，mboxDefault 中應有內容存在。 </p> </td> 
   <td colname="col3"> <p>確認有可用的內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>


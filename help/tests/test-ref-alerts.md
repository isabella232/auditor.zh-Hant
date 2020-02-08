---
description: 此參考提供了有關Auditor為測試顯示警報的詳細資訊。
seo-description: 此參考提供了有關Auditor為測試顯示警報的詳細資訊。
seo-title: 警報
title: 警報
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# 警報{#alerts}

此參考提供了有關Auditor為測試顯示警報的詳細資訊。

警報顯示您應該注意的問題，但不會影響分數。 這些建議是最佳實務，在某些情況下可能不適用於您的實作。

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 正確實作轉換標籤</b> </p> <p>重量：0 </p> </td> 
   <td colname="col2"> <p>檢查是否使用了正確的轉換標籤。 </p> <p> <p>警告： 使用過時的TubeMogul轉換標籤可能會造成資料遺失。 </p> </p> </td> 
   <td colname="col3"> <p>將您的轉換像素升級為全新的Advertising cloud僅限影像的轉換標籤。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 使用的JS標籤正確</b> </p> <p>重量：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloud應使用最新的JavaScript標籤。 </p> </td> 
   <td colname="col3"> <p>將您的Advertising Cloud javaScript升級至最新版本。 使用過時的JavaScript版本可能會導致功能遺失。 </p> <p>使用Advertising Cloud Launch Extension可更輕鬆地完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 僅限影像的標籤</b> </p> <p>重量：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloud影像像素格式應符合下列其中一種建議格式： </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>將您的Advertising cloud像素升級至新的Advertising cloud僅限影像標籤，以確保您正在運用完整的Advertising cloud功能。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 啟用細分像素DSP同步</b> </p> <p>重量：0 </p> </td> 
   <td colname="col2"> <p>檢查TubeMogul區段像素是否包含DSP同步設定，並建議將該設定新增至像素。 </p> <p>「DSP同步」設定是使用查詢字串參數來決定，因此 </p> <p>如果標籤引發至<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>此標籤包含URL參 <span class="codeph"> 數"sid=")</span> </p> <p>然後檢查URL參數 <span class="codeph"> "cs=0"</span> 或<span class="codeph"> "cs=1"是否存在，若不建議將</span><span class="codeph"></span> "cs=1"新增至這些像素，以提高觀眾比對率。 </p> </td> 
   <td colname="col3"> <p> 將URL參數 <span class="codeph"> "cs=1"新增至Advertising cloud像素</span> ，以便進行DSP同步化，進而提高受眾比對率。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - pageBottom回呼位置</b> </p> <p>重量：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 其他資訊</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>「動態標籤管理」 <span class="codeph"> 需要_satellite.pageBottom()函式</span> 。 在結束&lt;/body&gt;標籤前加入內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的DTM功能。 </p> <p> <p>注意：最佳實務是，標籤是 <i>&lt;body&gt;中</i> 的 <span class="codeph"></span>最後一個標籤。 如果在 <span class="codeph"> &lt;body&gt;</span> tag（內文）中找到它，它有可能運作，但由於它並非最佳實務，因此可能會運作不正確，或產生非預期或不想要的結果。 </p> </p> </td> 
   <td colname="col3"> <p>在結束&lt;/body&gt;標籤前加入內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的DTM功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM —— 自行托管</b> </p> <p>重量：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> DTM程式庫是在Adobe的Akamai執行個體上代管，位於 <span class="filepath"> assets.adobedtm.com</span>。 </p> <p> 自行代管是載入DTM的建議方法，因為它可透過快取控制、減少協力廠商指令碼相依性，並更能控制發佈程式，提供對網站效能的更大控制。 DTM程式庫可透過您自己的網頁代管或CDN來代管和管理。 </p> </td> 
   <td colname="col3"> <p>自行代管是在頁面上載入DTM的建議方法。 雖然透過Akamai CDN進行DTM代管在大多數情況下都能運作，但自行托管可改善頁面效能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID服務——僅使用一個AdobeOrg</b> </p> <p>重量：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>在一般的MCID實作中，應使用單一AdobeOrg。 </p> </td> 
   <td colname="col3"> <p>驗證此實作有多個AdobeOrg ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>啟動- pageBottom回呼位置</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他資訊</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>如果同步部 <span class="codeph"> 署， </span>啟動應在頁面內文中最後定義pageBottom回呼函式。 </p> <p> <p>注意：最佳實務是，標籤是 <i>&lt;body&gt;中</i> 的 <span class="codeph"></span>最後一個標籤。 如果在 <span class="codeph"> &lt;body&gt;</span> tag（內文）中找到它，它有可能運作，但由於它並非最佳實務，因此可能會運作不正確，或產生非預期或不想要的結果。 </p> </p> </td> 
   <td colname="col3"> <p>Launch需要 <span class="codeph"> _satellite.pageBottom()函式</span> ，才能進行同步部署。 在結束&lt;/body&gt;標籤前立即新增內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的啟動功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>啟動——自行托管</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Launch快速入門</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> 啟動非同步部署</a> </p> </td> 
   <td colname="col2"> <p>Launch程式庫是由Adobe的Akamai執行個體代管，位於 <span class="filepath"> assets.adobedtm.com</span>。 </p> <p>自我托管是載入Launch的建議方法，因為它可透過快取控制、減少協力廠商指令碼相依性，以及更完善的發佈程式控制，提供網站效能的更佳控制。 Launch程式庫可透過您自己的Web代管或CDN來代管和管理。 </p> </td> 
   <td colname="col3"> <p>雖然透過Akamai CDN啟動代管在大多數情況下都能運作，但建議將自行代管建置為改善頁面效能的第一步。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>啟動——應非同步部署</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>啟動應以非同步方式部署，以獲得最佳效能。 </p> </td> 
   <td colname="col3"> <p>在內嵌指令碼中加入async參數，以確保正確的非同步啟動功能 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - mboxDefault中的內容</b> </p> <p>重量：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 使用at.js時，mboxDefault中應存在內容。 </p> </td> 
   <td colname="col3"> <p>驗證內容是否可用。 </p> </td> 
  </tr> 
 </tbody> 
</table>


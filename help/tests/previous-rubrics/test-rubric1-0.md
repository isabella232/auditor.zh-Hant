---
description: 'null'
seo-description: 'null'
seo-title: 測試規則0.0.8
title: 測試規則0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
translation-type: tm+mt
source-git-commit: b56d3d2bd79c812fda6a75827d14044d9a8a3b4c

---


# 測試規則0.0.8{#test-rubric}

## 測試規則0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## 警報 {#alerts}

此參考提供了有關Auditor為測試顯示警報的詳細資訊。

警報顯示您應該注意的問題，但不會影響分數。

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
    <td colname="col1"> <p><b>Advertising Cloud —— 正確實作轉換標籤</b> </p> <p>重量：0 </p> </td> 
    <td colname="col2"> <p>檢查是否使用了正確的轉換標籤。 </p> <p> <p>警告： 使用過時的TubeMogul轉換標籤可能會造成資料遺失。 </p> </p> </td> 
    <td colname="col3"> <p>將您的轉換像素升級為全新的Advertising cloud僅限影像的轉換標籤。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 僅限影像的標籤</b> </p> <p>重量：0 </p> </td> 
    <td colname="col2"> <p>Advertising cloud影像像素格式應符合下列其中一種建議格式： </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>將您的Advertising cloud像素升級至新的Advertising cloud僅限影像標籤，以確保您正在運用完整的Advertising cloud功能。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 啟用細分像素DSP同步</b> </p> <p>重量：0 </p> </td> 
    <td colname="col2"> <p>檢查TubeMogul區段像素是否包含DSP同步設定，並建議將該設定新增至像素。 </p> <p>「DSP同步」設定是使用查詢字串參數來決定，因此 </p> <p>如果標籤引發至<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>此標籤包含URL參 <span class="codeph"> 數"sid=")</span> </p> <p>然後檢查URL參數 <span class="codeph"> "cs=0"</span> 或<span class="codeph"> "cs=1"是否存在，若不建議將</span><span class="codeph"></span> "cs=1"新增至這些像素，以提高觀眾比對率。 </p> </td> 
    <td colname="col3"> <p> 將URL參數 <span class="codeph"> "cs=1"新增至Advertising cloud像素</span> ，以便進行DSP同步化，進而提高受眾比對率。 </p> <p>Advertising Cloud Launch Extension最容易完成這項工作。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom回呼位置</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> 
     <draft-comment>
       TEa9df69942f404055a64262889c8b21d3 
     </draft-comment> </td> 
    <td colname="col2"> <p> 動態標籤管理需要<span class="codeph"> _satellite.pageBottom()函式</span> 。 </p> <p>最佳實務是，標籤是 <i>&lt;body&gt;</i> 中 <span class="codeph"></span>的最後一個標籤。 如果在 <span class="codeph"> &lt;body&gt;</span> tag（內文）中找到它，它有可能運作，但由於它並非最佳實務，因此可能會運作不正確，或產生非預期或不想要的結果。 </p> </td> 
    <td colname="col3"> <p>在結束&lt;/body&gt;標籤前加入內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的DTM功能。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID服務——僅使用一個AdobeOrg</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p>在一般的MCID實作中，應使用單一AdobeOrg。 </p> </td> 
    <td colname="col3"> <p>驗證此實作有多個AdobeOrg ID。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target - mboxDefault中的內容</b> </p> <p>重量：0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 使用at.js時，mboxDefault中應存在內容。 </p> </td> 
    <td colname="col3"> <p>驗證內容是否可用。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 設定 {#configuration}

此參考提供了有關Auditor為配置執行的測試的詳細資訊。

Auditor會根據其他規則和建議的最佳實務來評估標籤。

<table id="table_A8A1FC360482447185C8460A18426638"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 測試 </th> 
    <th colname="col2" class="entry"> 標準 </th> 
    <th colname="col3" class="entry"> 建議 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 轉換名稱僅使用英數字元</b> </p> <p>重量：3 </p> </td> 
    <td colname="col2"> <p>ev_conversion_ <span class="codeph"> property_name</span> 參數應僅包含數值和小數值，「<span class="codeph"> ev_transid」參數除外(</span><span class="codeph"></span> ev_transid值可包含文字或數值) </p> <p>尋找 <span class="codeph"> 包含URL參數(以</span> ev_開頭)的everesttech.net像素 <span class="codeph"></span>。 </p> <p>範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> 請確定您的交易屬性參數只包含數值和小數值。 </p> <p> <p>警告： 任何其他值類型都可能導致資料遺失。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 轉換名稱使用URL安全字元</b> </p> <p>重量：3 </p> </td> 
    <td colname="col2"> <p> 轉換屬性名稱不應包含&amp;符號或問號。 </p> <p> 範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>請確定transaction屬性參數不包含非編碼的&amp;符號或問號。 這些會中斷URL格式。 </p> <p> <p>警告：包含非編碼&amp;符號或問號的屬性參數(例如：ev_ <span class="codeph"> formComplete?=1</span> 或 <span class="codeph"> ev_formComplete&amp;Submit=1</span>)，可能會造成資料遺失。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 交易ID已正確實作</b> </p> <p>重量：1 </p> </td> 
    <td colname="col2"> <p> 屬性名 <span class="codeph"> 稱ev_transid=</span> ，不應為空。 </p> <p>範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>屬性名 <span class="codeph"> 稱ev_transid=</span> ，不應留在沒有值(<span class="codeph"> ev_transid=</span>)的情況下。 如果保留此值而沒有值，則可能會丟失事務資料。 為ev_transid=指 <span class="codeph"> 定值</span> ，或從像素中移除參數。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics —— 在DOM中執行個體化</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/testing-and-validation-process/impl-validation.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analytics代碼未安裝或無法執行。 找不到分析程式碼時傳回0。 </p> </td> 
    <td colname="col3"> <p>確認Analytics標籤已實作在頁面上，且未被後續指令碼活動封鎖。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics —— 執行個體化一次</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 在頁面上偵測到Adobe Analytics代碼多次。. 找不到分析程式碼時傳回0。 </p> </td> 
    <td colname="col3"> <p>請確定頁面上只有一個Analytics標籤。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics —— 最新版本</b> </p> <p>重量：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 您的頁面未執行最新版Analytics程式碼庫。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 找不到分析程式碼時傳回0。 </p> </td>       
    <td colname="col3"> <p>安裝最新版的Analytics程式庫。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM —— 自行托管</b> </p> <p>重量：4 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> DTM程式庫是在Adobe的Akamai執行個體上代管，位於 <span class="filepath"> assets.adobedtm.com</span>。 </p> <p> 自行代管是載入DTM的建議方法，因為它可透過快取控制、減少協力廠商指令碼相依性，並更能控制發佈程式，提供對網站效能的更大控制。 DTM程式庫可透過您自己的網頁代管或CDN來代管和管理。 </p> </td> 
    <td colname="col3"> <p>自行代管是在頁面上載入DTM的建議方法。 雖然透過Akamai CDN進行DTM代管在大多數情況下都能運作，但自行托管可改善頁面效能。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM —— 協力廠商標籤在DOM就緒後以非同步方式載入</b> </p> <p>重量：3 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/resources/load-order.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p>為在良好的使用者體驗與收集正確資料之間取得平衡，第三方標籤應在DOM就緒時觸發。 這將確保這些追蹤指令碼的執行，而不會影響網站功能。 </p> </td> 
    <td colname="col3"> <p>調整執行第三方像素的所有規則，以在DOM就緒時觸發，以解決此問題。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID服務——最新版本</b> </p> <p>重量：2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 您的頁面未執行最新版的訪客ID服務程式碼庫 <span class="codeph"> visitorAPI.js</span>。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 </p> </td> 
    <td colname="col3"> <p>安裝最新版的訪客ID服務程式庫。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target —— 最新版本</b> </p> <p>重量：2 </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/dtm/target/" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 您的頁面未執行最新版的Target程式碼庫。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 </p> </td> 
    <td colname="col3"> <p>安裝最新版的Target程式庫。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - mboxDefault在mboxCreate之前 </b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p>正確使用 <span class="codeph"> mboxCreate</span> ，看起來類似： </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>請務必在叫 <span class="codeph"> 用mboxCreate()前加入&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span><span class="codeph"> 標籤</span>。 at.js不會為您新增一個。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target —— 有效的DOCTYPE</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 檢測到無效的DOCTYPE。 此藍本中不會引發mbox。 </p> <p>對於at.js,DOCTYPE必須處於「標準」模式，否則Target將無法運作。 </p> </td> 
    <td colname="col3"> <p>更新頁面上的DOCTYPE。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 標籤一致性 {#tag-consistency}

此參考提供了有關Auditor為標籤一致性而執行的測試的詳細資訊。

Auditor會評估各URL的標籤是否一致。

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 測試 </th> 
    <th colname="col2" class="entry"> 標準 </th> 
    <th colname="col3" class="entry"> 建議 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analytics —— 一致的程式碼版本 </b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/choose-implementation-method.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 找到多個Analytics程式碼版本。 </p> </td> 
    <td colname="col3"> <p>將所有Analytics例項取代為目前版本。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 標籤存在 {#tag-presence}

此參考提供了有關Auditor為標籤存在而執行的測試的詳細資訊。

Auditor會評估標籤是否存在，以及標籤是否在您的頁面程式碼中位於正確位置，依此類推。

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
    <td colname="col1"> <p><b>Advertising Cloud —— 程式碼呈現</b> </p> <p>重量：5 </p> </td> 
    <td colname="col2"> <p> DOM中不提供Advertising cloud標籤。 </p> </td> 
    <td colname="col3"> <p>使用Advertising Cloud Launch Extension實作Advertising cloud標籤。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud —— 實作區段像素</b> </p> <p>重量：5 </p> </td> 
    <td colname="col2"> <p> 將您的Advertising cloud細分像素升級至新的Advertising cloud僅限影像標籤。 使用過時的AMO區段標籤可能會造成資料遺失。 </p> </td> 
    <td colname="col3"> <p>使用Advertising Cloud Launch Extension實作Advertising cloud區段像素。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics —— 在DOM中載入</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 未偵測到Adobe Analytics標籤。 </p> </td> 
    <td colname="col3"> <p>安裝最新版Analytics。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM —— 已載入資料庫</b> </p> <p>重量：5 </p> <p>其他資訊: </p> <p> 
      <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
       <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM疑難排解</a> </li> 
       <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 新增頁首與頁尾程式碼</a> </li> 
      </ul> </p> </td> 
    <td colname="col2"> <p> 在DOM中找不到全域_satellite物件。 動態標籤管理未安裝或無法執行。 </p> </td> 
    <td colname="col3"> <p>確認DTM程式庫已建置在頁面上，且未遭後續指令碼活動封鎖。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM —— 單一內嵌代碼</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 生產網站只應載入一個DTM程式庫。 </p> </td> 
    <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom回呼存在於&lt;body&gt;</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 在頁 <span class="codeph"> 面的&lt;body&gt;</span><span class="codeph"></span> （動態標籤管理需要）中找不到_satellite.pageBottom()回呼。 </p> <p>如果頁面上完 <span class="codeph"> 全 </span>找不到pageBottom呼叫，或者它位於 <span class="codeph"> &lt;head&gt;</span> 標籤（或其他非預期位置），則此測試會失敗。 只有在&lt;body&gt;標 <span class="codeph"> 簽內找到pageBottom</span> 時 <span class="codeph"> ，才會傳遞</span> 。 如果它完全不在頁面上，它將無法運作，其他兩個pageBottom測 <span class="codeph"> 試也會失敗</span> 。 </p> </td> 
    <td colname="col3"> <p>在結束&lt;/body&gt;標籤前加入內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的DTM功能。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom標籤引發</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 未偵 <span class="codeph"> 測到DTM pageBottom</span> 標籤。 </p> <p>如果呼叫位於 <span class="codeph"> if</span> 陳述式中，並產生類似 <span class="codeph"> if(false){_satellite.pageBottom()}的情形，就會發生這種情況</span>。 因此，雖然標籤可能存在且已正確放置，但標籤仍可能無法觸發。 </p> </td> 
    <td colname="col3"> <p>安裝DTM頁面 <span class="codeph"> 每頁</span> 「底部呼叫」。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID服務- cookie存在</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 找 <span class="codeph"> 不到AMCV_</span> Cookie。 您必須從VisitorAPI.js程式碼實例 <span class="codeph"> 化訪客物件</span> 。 </p> </td> 
    <td colname="col3"> <p> 如果這是DTM實作，請確認AdobeOrg ID已正確輸入至MCID工具。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID服務- MID值呈現</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 在 <span class="codeph"> AMCV_</span> cookie中找不到mid值。 </p> </td> 
    <td colname="col3"> <p>請再次測試，以檢查是否有任何MCID API延遲。 如果情況持續，請聯絡Adobe客戶服務。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID服務——應安裝</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
    <td colname="col2"> <p> 找不到Experience Cloud ID服務程式碼。 強烈建議使用ECID，以確保您從Experience cloud解決方案中獲得最大價值，並且對於跨EC解決方案的ID管理至關重要。 </p> </td> 
    <td colname="col3"> <p>請安裝MCID的最新版本。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target —— 在&lt;head&gt;中載入的程式庫</b> </p> <p>重量：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> 
     <draft-comment>
       TE61c380082a4b4706b28a84aa047599a7 
     </draft-comment> </td> 
    <td colname="col2"> <p> Target程式庫應載入至 <span class="codeph"> &lt;head&gt;標籤</span> 。 </p> </td> 
    <td colname="col3"> <p> 檢查以確定Target程式庫已載入至 <span class="codeph"> &lt;head&gt;標籤</span> 。 </p> </td> 
   </tr> 
  </tbody> 
</table>

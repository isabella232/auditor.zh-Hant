---
description: 此參考提供了有關Auditor為標籤存在而執行的測試的詳細資訊。
seo-description: 此參考提供了有關Auditor為標籤存在而執行的測試的詳細資訊。
seo-title: 標籤存在
title: 標籤存在
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 標籤存在

此參考提供了有關Auditor為標籤存在而執行的測試的詳細資訊。

Auditor會評估標籤是否存在，以及標籤是否在您的頁面代碼中位於正確位置。

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
   <td colname="col1"> <p><b>Analytics —— 在DOM中載入</b> </p> <p>重量：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 其他資訊</a> </p> </td> 
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
   <td colname="col2"> <p> 未偵 <code> pageBottom</code> 測到DTM標籤。 </p> <p>如果呼叫位於導致類似 <code> if</code> 的陳述式中，則可能發生此情況 <code> if (false) {_satellite.pageBottom()}</code>。 因此，雖然標籤可能存在且已正確放置，但標籤仍可能無法觸發。 </p> </td> 
   <td colname="col3"> <p>在每個頁面上 <code> pageBottom</code> 安裝DTM呼叫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服務——程式碼存在</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>找不到Experience Cloud ID服務程式碼。 強烈建議使用Experience Cloud ID(MCID)，以確保您從Experience cloud解決方案中獲得最大價值，對於跨Experience cloud解決方案的ID管理至關重要。 </p> </td> 
   <td colname="col3"> <p> 安裝最新版的MCID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服務- cookie存在</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 找 <span class="codeph"> 不到AMCV_</span> Cookie。 您必須從VisitorAPI.js程式碼實例 <span class="codeph"> 化訪客物件</span> 。 </p> </td> 
   <td colname="col3"> <p> 如果這是DTM實作，請確認AdobeOrg ID已正確輸入至MCID工具。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服務- MID值呈現</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在AMCV_ <span class="codeph"> Cookie中找不到MID值</span> 。 </p> </td> 
   <td colname="col3"> <p>請再次測試，以檢查是否有任何MCID API延遲。 如果情況持續，請聯絡Adobe客戶服務。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> 啟動——已載入資料庫</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在DOM中找不到全域_satellite物件。 Launch未安裝或無法執行。 </p> </td> 
   <td colname="col3"> <p>確認啟動程式庫已實作在頁面上，且未遭後續指令碼活動封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>啟動——沒有多個內嵌指令碼</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>頁面上不應載入多個內嵌指令碼。 生產網站只應載入一個Launch程式庫。 </p> </td> 
   <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom回呼存在於&lt;body&gt;中</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁 <span class="codeph"> 面的&lt;body&gt;中找不到</span> _satellite.pageBottom() <span class="codeph"></span> ，這是Launch所需的。 </p> <p>如果頁面上完 <span class="codeph"> 全 </span>找不到pageBottom呼叫，或者它位於 <span class="codeph"> &lt;head&gt;</span> 標籤（或其他非預期位置），則此測試會失敗。 只有在&lt;body&gt;標 <span class="codeph"> 簽內找到pageBottom</span> 時 <span class="codeph"> ，才會傳遞</span> 。 如果它完全不在頁面上，它將無法運作，其他兩個pageBottom測 <span class="codeph"> 試也會失敗</span> 。 </p> </td> 
   <td colname="col3"> <p>在結束&lt;/body&gt;標籤前立即新增內嵌 <span class="codeph"> 指令碼</span> ，以確保正確的啟動功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom回呼在非同步部署時不應存在</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>在頁 <span class="codeph"> 面上找到_satellite.pageBottom()</span> ，當Launch非同步部署時，不應該是這樣。 </p> </td> 
   <td colname="col3"> <p>移除<span class="codeph"> _satellite.pageBottom()指令碼</span> ，以啟用正確的啟動功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target —— 程式碼存在</b> </p> <p>重量：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>Target應在DOM中定義。 </p> </td> 
   <td colname="col3"> <p>安裝最新版Target(at.js)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target —— 在&lt;head&gt;中載入的程式庫</b> </p> <p>重量：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> Target程式庫應載入至 <span class="codeph"> &lt;head&gt;標籤</span> 。 </p> </td> 
   <td colname="col3"> <p> 檢查以確定Target程式庫已載入至 <span class="codeph"> &lt;head&gt;標籤</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

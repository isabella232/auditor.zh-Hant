---
description: 此參考提供與 Auditor 針對設定而執行的測試有關的詳細資訊。
seo-description: 此參考提供與 Auditor 針對設定而執行的測試有關的詳細資訊。
seo-title: 設定
title: 設定
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 78105ff6766f48f3aaccfeda281e5b4883be856a

---


# 設定

此參考提供與 Auditor 針對設定而執行的測試有關的詳細資訊。

設定測試會掃描您實施中的特定設定、值或潛在衝突。Auditor 會根據其他規則和建議的最佳實務來評估標記。

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 轉換名稱僅使用英數字元</b> </p> <p>權重：3 </p> </td> 
   <td colname="col2"> <p><span class="codeph">ev_conversion_property_name</span> 參數應僅包含數值和小數值，但 "<span class="codeph">ev_transid</span>" 參數除外 (<span class="codeph">ev_transid</span> 值可包含文字值或數值) </p> <p>尋找包含 URL 參數 (以 <span class="codeph">ev_</span> 開頭) 的 <span class="codeph">everesttech.net</span> 像素。 </p> <p>範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> 確定您的交易屬性參數只包含數值和小數值。 </p> <p> <p>警告：任何其他值類型都可能導致資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 轉換名稱使用 URL 可用的字元</b> </p> <p>權重：3 </p> </td> 
   <td colname="col2"> <p> 轉換屬性名稱不應包含 &amp; 符號或問號。 </p> <p> 範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>確定交易屬性參數未包含非編碼的 &amp; 符號或問號。這些符號會中斷 URL 格式。 </p> <p> <p>警告：包含非編碼 &amp; 符號或問號的屬性參數 (例如：<span class="codeph">ev_formComplete?=1</span> 或 <span class="codeph">ev_formComplete&amp;Submit=1</span>) 可能會導致資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 正確實施交易 ID</b> </p> <p>權重：1 </p> </td> 
   <td colname="col2"> <p> 屬性名稱 <span class="codeph">ev_transid=</span> 不應空白。 </p> <p>範例: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>屬性名稱 <span class="codeph">ev_transid=</span> 不應保留為空白 (<span class="codeph">ev_transid=</span>)。若將其保留為空白，交易資料可能會遺失。將值指派給 <span class="codeph">ev_transid=</span>，或從像素中移除參數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 在 DOM 中具現化</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics 程式碼未安裝或無法執行。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>確認已在頁面上實施 Analytics 標記，且後續指令碼活動不會加以封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 具現化一次</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面上偵測到 Adobe Analytics 程式碼多次。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>確定頁面上只有一個 Analytics 標記。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 最新版本</b> </p> <p>權重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版 Analytics 程式碼庫。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Analytics 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - 在 DOM 準備就緒後，以非同步方式載入第三方標記</b> </p> <p>權重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/resources/load-order.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>為了在良好的使用者體驗與收集正確資料之間取得平衡，應在 DOM 準備就緒時觸發第三方標記。這樣可以確保這些追蹤指令碼能夠在不影響網站功能的情況下執行。 </p> </td> 
   <td colname="col3"> <p>調整所有執行第三方像素的規則，使其在 DOM 就緒時引發，以解決此問題。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID 服務 - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/tools/macid.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版的訪客 ID 服務程式碼庫 <span class="codeph">visitorAPI.js</span>。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的訪客 ID 服務程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>這些頁面未執行最新版的 Launch 程式碼庫 (Turbine)。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p> 重建 Launch 程式庫並加以發佈，以更新 Launch 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版 Target 程式碼庫。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Target 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - 在 mboxCreate 前面加上 mboxDefault</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p><span class="codeph">mboxCreate</span> 的正確用法如下所示： </p> <p> <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;! -Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>在叫用 <span class="codeph">mboxCreate()</span> 之前，請務必先加上 <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> 標記。at.js 不會為您加上此標記。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - 有效的 DOCTYPE</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/help/en/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 偵測到無效的 DOCTYPE。在此情況下不會引發 mbox。 </p> <p>對 at.js 而言，DOCTYPE 必須處於「標準」模式，否則 Target 將無法運作。 </p> </td> 
   <td colname="col3"> <p>更新頁面上的 DOCTYPE。 </p> </td> 
  </tr> 
 </tbody> 
</table>


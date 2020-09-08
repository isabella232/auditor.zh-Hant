---
description: Adobe Auditor 測試相關資訊
seo-description: Adobe Auditor 測試相關資訊
seo-title: 測試規則 1.0.1
title: 測試規則 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: ht
source-git-commit: 77ced60ff8e05515521d89d16c32cbad42d1e8d0
workflow-type: ht
source-wordcount: '2684'
ht-degree: 100%

---


# 測試規則 1.0.1{#test-rubric}

## 測試規則 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## 警報 {#alerts}

此參考提供與 Auditor 針對測試而顯示之警報有關的詳細資訊。

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
   <td colname="col3"> <p>將您的轉換像素升級為新的 Advertising Cloud 僅限影像轉換標記。 </p> <p>這項工作用 Advertising Cloud Launch Extension 來執行最為容易。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 使用正確的 JS 標記</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 應使用最新的 JavaScript 標記。 </p> </td> 
   <td colname="col3"> <p>將您的 Advertising Cloud JavaScript 升級至最新版本。使用過時的 JavaScript 版本可能會導致功能失效。 </p> <p>使用 Advertising Cloud Launch Extension 可輕鬆完成這項工作。 </p> </td> 
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
   <td colname="col3"> <p>將您的 Advertising Cloud 像素升級至新的 Advertising Cloud 僅限影像標記，以確保您使用的是完整的 Advertising Cloud 功能。 </p> <p>這項工作用 Advertising Cloud Launch Extension 來執行最為容易。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 啟用區段像素 DSP 同步</b> </p> <p>權重：0 </p> </td> 
   <td colname="col2"> <p>檢查 TubeMogul 區段像素是否包含「DSP 同步」設定，並建議您將該設定新增至像素。 </p> <p>「DSP 同步」設定取決於查詢字串參數的使用，因此 </p> <p>如果對 <span class="codeph">("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph">"http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或 <span class="codeph">"http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>引發標記，且該標記包含 URL 參數 <span class="codeph">"sid=")</span>， </p> <p>則應確認 URL 參數 <span class="codeph">"cs=0"</span> 或 <span class="codeph">"cs=1"</span> 是否存在；若不存在，則建議將 <span class="codeph">"cs=1"</span> 新增至這些像素，以提高投放對象準確率。 </p> </td> 
   <td colname="col3"> <p> 將 URL 參數 <span class="codeph">"cs=1"</span> 新增至 Advertising Cloud 像素，以便進行 DSP 同步，進而提高投放對象準確率。 </p> <p>這項工作用 Advertising Cloud Launch Extension 來執行最為容易。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - pageBottom 回呼位置</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management 需要 <span class="codeph">_satellite.pageBottom()</span> 函數。在結尾的內文標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> <p> <p>注意：最佳實務是讓該標記成為 <span class="codeph">&lt;body&gt;</span> 中的<i>最後一個</i>標記。若將其置於 <span class="codeph">&lt;body&gt;</span> 標記內，雖然或許能運作，但由於這並非最佳實務，因此其運作可能會不正確，或產生非預期或不適當的結果。 </p> </p> </td> 
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
      1.0.1 
    --> <p><b>Launch - pageBottom 回呼位置</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>如果進行同步部署，Launch 應在頁面內文中的結尾處定義 <span class="codeph">pageBottom</span> 回呼函數 </p> <p> <p>注意：最佳實務是讓該標記成為 <span class="codeph">&lt;body&gt;</span> 中的<i>最後一個</i>標記。若將其置於 <span class="codeph">&lt;body&gt;</span> 標記內，雖然或許能運作，但由於這並非最佳實務，因此其運作可能會不正確，或產生非預期或不適當的結果。 </p> </p> </td> 
   <td colname="col3"> <p>在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 自行託管</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>Launch 程式庫在 Adobe 的 Akamai 執行個體上受到託管 (網址是 <span class="filepath">assets.adobedtm.com</span>)。 </p> <p>自行託管是載入 Launch 的建議方法，因為此方法可讓您透過快取控制進一步掌控網站效能、減少對第三方指令碼的依賴，且更能掌握發佈程序。您可以透過自己的網站託管或 CDN 來託管及管理 Launch 程式庫。 </p> </td> 
   <td colname="col3"> <p>雖然透過 Akamai CDN 進行 Launch 託管在多數情況下都是可行的，但建議您實施自行託管，作為改善頁面效能的首要步驟。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 應以非同步方式部署</b> </p> <p>權重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>Launch 應以非同步方式部署，以獲得最佳效能。 </p> </td> 
   <td colname="col3"> <p>在內嵌指令碼中加入 async 參數，以確保非同步 Launch 功能可正確運作 </p> </td> 
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

## 設定 {#configuration}

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
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 轉換名稱僅使用英數字元</b> </p> <p>權重：3 </p> </td> 
   <td colname="col2"> <p><span class="codeph">ev_conversion_property_name</span> 參數應僅包含數值和小數值，但 "<span class="codeph">ev_transid</span>" 參數除外 (<span class="codeph">ev_transid</span> 值可包含文字值或數值) </p> <p>尋找包含 URL 參數 (以 <span class="codeph">ev_</span> 開頭) 的 <span class="codeph">everesttech.net</span> 像素。 </p> <p>範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> 確定您的交易屬性參數只包含數值和小數值。 </p> <p> <p>警告：任何其他值類型都可能導致資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 轉換名稱使用 URL 可用的字元</b> </p> <p>權重：3 </p> </td> 
   <td colname="col2"> <p> 轉換屬性名稱不應包含 &amp; 符號或問號。 </p> <p> 範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>確定交易屬性參數未包含非編碼的 &amp; 符號或問號。這些符號會中斷 URL 格式。 </p> <p> <p>警告：包含非編碼 &amp; 符號或問號的屬性參數 (例如：<span class="codeph">ev_formComplete?=1</span> 或 <span class="codeph">ev_formComplete&amp;Submit=1</span>) 可能會導致資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 正確實施交易 ID</b> </p> <p>權重：1 </p> </td> 
   <td colname="col2"> <p> 屬性名稱 <span class="codeph">ev_transid=</span> 不應空白。 </p> <p>範例: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>屬性名稱 <span class="codeph">ev_transid=</span> 不應保留為空白 (<span class="codeph">ev_transid=</span>)。若將其保留為空白，交易資料可能會遺失。將值指派給 <span class="codeph">ev_transid=</span>，或從像素中移除參數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 在 DOM 中具現化</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics 程式碼未安裝或無法執行。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>確認已在頁面上實施 Analytics 標記，且後續指令碼活動不會加以封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 具現化一次</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面上偵測到 Adobe Analytics 程式碼多次。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>確定頁面上只有一個 Analytics 標記。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 最新版本</b> </p> <p>權重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版 Analytics 程式碼庫。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。在網頁上找不到 Analytics 程式碼時，會傳回 0。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Analytics 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 在 DOM 準備就緒後，以非同步方式載入第三方標記</b> </p> <p>權重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/resources/load-order.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>為了在良好的使用者體驗與收集正確資料之間取得平衡，應在 DOM 準備就緒時觸發第三方標記。這樣可以確保這些追蹤指令碼能夠在不影響網站功能的情況下執行。 </p> </td> 
   <td colname="col3"> <p>調整所有執行第三方像素的規則，使其在 DOM 就緒時引發，以解決此問題。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/tools/macid.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版的訪客 ID 服務程式碼庫 <span class="codeph">visitorAPI.js</span>。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的訪客 ID 服務程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>這些頁面未執行最新版的 Launch 程式碼庫 (Turbine)。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p> 重建 Launch 程式庫並加以發佈，以更新 Launch 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 最新版本</b> </p> <p>權重：2 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/tools/target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版 Target 程式碼庫。支援 Experience Cloud 技術的程式碼庫會持續更新並調整，以保有強化的效能並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Target 程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 在 mboxCreate 前面加上 mboxDefault</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p><span class="codeph">mboxCreate</span> 的正確用法如下所示： </p> <p> <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;! -Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>在叫用 <span class="codeph">mboxCreate()</span> 之前，請務必先加上 <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> 標記。at.js 不會為您加上此標記。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 有效的 DOCTYPE</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 偵測到無效的 DOCTYPE。在此情況下不會引發 mbox。 </p> <p>對 at.js 而言，DOCTYPE 必須處於「標準」模式，否則 Target 將無法運作。 </p> </td> 
   <td colname="col3"> <p>更新頁面上的 DOCTYPE。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標記一致性{#tag-consistency}

此參考提供與 Auditor 針對標記一致性而執行的測試有關的詳細資訊。

Auditor 的一致性測試會在所有掃描的頁面上尋找不一致之處。這些值或設定在網站的所有頁面上均應相同，以確保資料收集的正確性。

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 一致的程式碼版本</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 找到多個 Analytics 程式碼版本。 </p> </td> 
   <td colname="col3"> <p>將所有 Analytics 執行個體取代為目前版本。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標記是否存在{#tag-presence}

此參考提供與 Auditor 針對標記是否存在而執行的測試有關的詳細資訊。

Auditor 會評估標記是否存在，及其是否位於頁面程式碼中的正確位置。

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 程式碼是否存在</b> </p> <p>權重：5 </p> </td> 
   <td colname="col2"> <p> Advertising Cloud 標記無法在 DOM 中使用。 </p> </td> 
   <td colname="col3"> <p>使用 Advertising Cloud Launch Extension 來實施 Advertising Cloud 標記。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 實施區段像素</b> </p> <p>權重：5 </p> </td> 
   <td colname="col2"> <p> 將您的 Advertising Cloud 區段像素升級為新的 Advertising Cloud 僅限影像標記。使用過時的 AMO 區段標記可能會導致資料遺失。 </p> </td> 
   <td colname="col3"> <p>使用 Advertising Cloud Launch Extension 來實施 Advertising Cloud 區段像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 在 DOM 中載入</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/analytics/implementation/home.html" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 未偵測到 Adobe Analytics 標記。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的 Analytics。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 載入程式庫</b> </p> <p>權重：5 </p> <p>其他資訊: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/admin/c-troubleshooting.html" format="html" scope="external">DTM 疑難排解</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 新增頁首與頁尾程式碼</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> 在 DOM 中找不到全域_satellite 物件。Dynamic Tag Management 未安裝或無法執行。 </p> </td> 
   <td colname="col3"> <p>確認已在頁面上實施 DTM 程式庫，且後續指令碼活動不會加以封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 單一內嵌程式碼</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 生產網站應載入一個 DTM 程式庫即可。 </p> </td> 
   <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - pageBottom 回呼存在於 &lt;body&gt; 中</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面的 <span class="codeph">&lt;body&gt;</span> 內找不到 Dynamic Tag Management 所需的 <span class="codeph">_satellite.pageBottom()</span> 回呼。 </p> <p>如果在頁面上完全找不到 <span class="codeph">pageBottom</span> 呼叫，或該呼叫位於 <span class="codeph">&lt;head&gt;</span> 標記中 (或其他非預期的位置)，則此測試不會通過。只有在 <span class="codeph">pageBottom</span> 位於 <span class="codeph">&lt;body&gt;</span> 標記內的某處時，測試才會通過。如果完全不在頁面上，則無法運作，且其他兩個 <span class="codeph">pageBottom</span> 測試也不會通過。 </p> </td> 
   <td colname="col3"> <p>在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 DTM 可正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 引發 pageBottom 標記</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 未偵測到 DTM <span class="codeph">pageBottom</span> 標記。 </p> <p>如果呼叫位於 <span class="codeph">if</span> 陳述式內而產生類似於 <span class="codeph">if (false) {_satellite.pageBottom()}</span> 的行為，就會發生此狀況。因此，儘管標記可能存在且已正確放置，仍可能無法引發。 </p> </td> 
   <td colname="col3"> <p>在每個頁面上安裝 DTM <span class="codeph">pageBottom</span> 呼叫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - 程式碼是否存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/id-service/using/implementation/implementation-methods.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>找不到 Experience Cloud ID 服務程式碼。強烈建議使用 Experience Cloud ID (MCID) 以確保能夠充分發揮 Experience Cloud 解決方案的效益，且其對於 Experience Cloud 解決方案的 ID 管理而言十分重要。 </p> </td> 
   <td colname="col3"> <p> 安裝最新版的 MCID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID 服務 - Cookie 是否存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/id-service/using/implementation/implementation-guides.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
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
      1.0.1 
    --> <p><b>Launch - 載入程式庫</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在 DOM 中找不到全域_satellite 物件。Launch 未安裝或無法執行。 </p> </td> 
   <td colname="col3"> <p>確認已在頁面上實施 Launch 程式庫，且後續指令碼活動不會加以封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 沒有多個內嵌指令碼</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>頁面上不應載入多個內嵌指令碼。生產網站應載入一個 Launch 程式庫即可。 </p> </td> 
   <td colname="col3"> <p>確認頁面上僅載入生產程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - pageBottom 回呼存在於 &lt;body&gt; 中</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面的 <span class="codeph">&lt;body&gt;</span> 內找不到 Launch 所需的 <span class="codeph">_satellite.pageBottom()</span> 回呼。 </p> <p>如果在頁面上完全找不到 <span class="codeph">pageBottom</span> 呼叫，或該呼叫位於 <span class="codeph">&lt;head&gt;</span> 標記中 (或其他非預期的位置)，則此測試不會通過。只有在 <span class="codeph">pageBottom</span> 位於 <span class="codeph">&lt;body&gt;</span> 標記內的某處時，測試才會通過。如果完全不在頁面上，則無法運作，且其他兩個 <span class="codeph">pageBottom</span> 測試也不會通過。 </p> </td> 
   <td colname="col3"> <p>請在結尾的 <span class="codeph">&lt;/body&gt;</span> 標記前面加上緊鄰的內嵌指令碼，以確保 Launch 可正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 進行非同步部署時，pageBottom 回呼不應存在</b> </p> <p>權重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>在頁面上找到 <span class="codeph">_satellite.pageBottom()</span> 回呼，但以非同步方式部署 Launch 時不應有此回呼。 </p> </td> 
   <td colname="col3"> <p>移除 <span class="codeph">_satellite.pageBottom()</span> 指令碼，以啟用正確的 Launch 功能。 </p> </td> 
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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 在 &lt;head&gt; 中載入程式庫</b> </p> <p>權重：4 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他資訊</a> </p> 
    <!--
      TE61c380082a4b4706b28a84aa047599a7 
    --> </td> 
   <td colname="col2"> <p> Target 程式庫應載入 <span class="codeph">&lt;head&gt;</span> 標記中。 </p> </td> 
   <td colname="col3"> <p> 確認 Target 程式庫已載入 <span class="codeph">&lt;head&gt;</span> 標記中。 </p> </td> 
  </tr> 
 </tbody> 
</table>


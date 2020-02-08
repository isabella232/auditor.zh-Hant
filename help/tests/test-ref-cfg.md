---
description: 此參考提供了有關Auditor為配置執行的測試的詳細資訊。
seo-description: 此參考提供了有關Auditor為配置執行的測試的詳細資訊。
seo-title: 設定
title: 設定
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 設定

此參考提供了有關Auditor為配置執行的測試的詳細資訊。

設定測試會掃描您實作中的特定設定、值或潛在衝突。 Auditor會根據其他規則和建議的最佳實務來評估標籤。

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
    </draft-comment> <p><b>Advertising Cloud —— 轉換名稱僅使用英數字元</b> </p> <p>重量：3 </p> </td> 
   <td colname="col2"> <p>ev_conversion_ <span class="codeph"> property_name</span> 參數應僅包含數值和小數值，「<span class="codeph"> ev_transid」參數除外(</span><span class="codeph"></span> ev_transid值可包含文字或數值) </p> <p>尋找 <span class="codeph"> 包含URL參數(以</span> ev_開頭)的everesttech.net像素 <span class="codeph"></span>。 </p> <p>範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> 請確定您的交易屬性參數只包含數值和小數值。 </p> <p> <p>警告： 任何其他值類型都可能導致資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 轉換名稱使用URL安全字元</b> </p> <p>重量：3 </p> </td> 
   <td colname="col2"> <p> 轉換屬性名稱不應包含&amp;符號或問號。 </p> <p> 範例: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>請確定transaction屬性參數不包含非編碼的&amp;符號或問號。 這些會中斷URL格式。 </p> <p> <p>警告：包含非編碼&amp;符號或問號的屬性參數(例如：ev_ <span class="codeph"> formComplete?=1</span> 或 <span class="codeph"> ev_formComplete&amp;Submit=1</span>)，可能會造成資料遺失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 交易ID已正確實作</b> </p> <p>重量：1 </p> </td> 
   <td colname="col2"> <p> 屬性名 <span class="codeph"> 稱ev_transid=</span> ，不應為空。 </p> <p>範例: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>屬性名 <span class="codeph"> 稱ev_transid=</span> ，不應留在沒有值(<span class="codeph"> ev_transid=</span>)的情況下。 如果保留此值而沒有值，則可能會丟失事務資料。 為ev_transid=指 <span class="codeph"> 定值</span> ，或從像素中移除參數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics —— 在DOM中執行個體化</b> </p> <p>重量：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics代碼未安裝或無法執行。 找不到分析程式碼時傳回0。 </p> </td> 
   <td colname="col3"> <p>確認Analytics標籤已實作在頁面上，且未被後續指令碼活動封鎖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics —— 執行個體化一次</b> </p> <p>重量：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 在頁面上偵測到Adobe Analytics代碼多次。. 找不到分析程式碼時傳回0。 </p> </td> 
   <td colname="col3"> <p>請確定頁面上只有一個Analytics標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics —— 最新版本</b> </p> <p>重量：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版Analytics程式碼庫。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 找不到分析程式碼時傳回0。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的Analytics程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM —— 協力廠商標籤在DOM就緒後以非同步方式載入</b> </p> <p>重量：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>為在良好的使用者體驗與收集正確資料之間取得平衡，第三方標籤應在DOM就緒時觸發。 這將確保這些追蹤指令碼的執行，而不會影響網站功能。 </p> </td> 
   <td colname="col3"> <p>調整執行第三方像素的所有規則，以在DOM就緒時觸發，以解決此問題。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服務——最新版本</b> </p> <p>重量：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版的訪客ID服務程式碼庫 <span class="codeph"> visitorAPI.js</span>。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的訪客ID服務程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>啟動——最新版本</b> </p> <p>重量：2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>這些頁面未執行最新版的啟動程式碼程式庫(Turbine)。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 </p> </td> 
   <td colname="col3"> <p> 重建並發佈啟動程式庫，以更新啟動程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target —— 最新版本</b> </p> <p>重量：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 您的頁面未執行最新版的Target程式碼庫。 支援Experience cloud技術的程式碼庫會不斷更新和調整，以利用效能改善並提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安裝最新版的Target程式庫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault在mboxCreate之前 </b> </p> <p>重量：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p>正確使用 <span class="codeph"> mboxCreate</span> ，看起來類似： </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>請務必在叫 <span class="codeph"> 用mboxCreate()前加入&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span><span class="codeph"> 標籤</span>。 at.js不會為您新增一個。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target —— 有效的DOCTYPE</b> </p> <p>重量：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他資訊</a> </p> </td> 
   <td colname="col2"> <p> 檢測到無效的DOCTYPE。 此藍本中不會引發mbox。 </p> <p>對於at.js,DOCTYPE必須處於「標準」模式，否則Target將無法運作。 </p> </td> 
   <td colname="col3"> <p>更新頁面上的DOCTYPE。 </p> </td> 
  </tr> 
 </tbody> 
</table>


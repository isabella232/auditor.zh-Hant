---
description: 此參考提供了有關Auditor執行的測試的詳細資訊。
seo-description: 此參考提供了有關Auditor執行的測試的詳細資訊。
seo-title: 測試參考
title: 測試參考
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# 測試參考{#test-reference}

此參考提供了有關Auditor執行的測試的詳細資訊。

**目前的測試規則版本：** 1.0.5

每個測試都會加權。 您的測試分數等於指定的權重。 如果您以5的重量通過測驗，就會得到5分。

* 0:提醒您應該注意的問題，但這不會影響您的分數。
* 1:建議最佳化。 不影響資料的準確性。
* 2:未通過此測試表示您將無法存取Experience cloud中的最新功能和修正。
* 3:測試效率，以及實作是否遵循最佳實務。
* 4:失敗表示您可能正在收集不可靠的資料。
* 5:失敗表示您可能會看到資料遺失。

測試通過／失敗。 他們會測試是否符合測試條件，因此不會對部分符合進行部分分數。 例如，如果測試檢查Adobe解決方案的最新版本，而您只落後於一個版本，則獲得的分數會與您先前的五個版本相同。 最新版本包含效能改進和錯誤修正，因此建議使用最新版本。

**強烈建議**&#x200B;您修正層級 4 或層級 5 的結果。

**建議**&#x200B;您修正層級 1 到層級 3 的結果。

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

## 測試類別 {#section-630181db21ef4eec9ce6a13a0482bb55}

此測試參考將測試分為下列類別：

---
description: 此參考提供與 Auditor 執行的測試有關的詳細資訊。
seo-description: 此參考提供與 Auditor 執行的測試有關的詳細資訊。
seo-title: 測試參考
title: 測試參考
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: ht
source-git-commit: 78105ff6766f48f3aaccfeda281e5b4883be856a

---


# 測試參考{#test-reference}

此參考提供與 Auditor 執行的測試有關的詳細資訊。

**目前的測試規則版本：** 1.0.5

每項測試都會加權。您的測試分數會等於指定的權重。如果您通過權重為 5 的測試，就會得到 5 分。

* 0：對您應留意、但不影響分數的問題提出警報。
* 1：建議最佳化。不影響資料正確性。
* 2：若未通過此測試，表示您將無法存取 Experience Cloud 中的最新功能和修正。
* 3：測試效率，以及實施是否遵循最佳實務準則。
* 4：若未通過，表示您所收集的資料可能不可靠。
* 5：若未通過，表示可能會發生資料遺失。

測試結果分成通過和未通過。測試目的在於確認是否符合測試條件，因此並不會因為部分符合而獲得部分分數。例如，如果測試檢查您是否有最新版的 Adobe 解決方案，而您只比最新版本舊一個版本，您得到的分數仍會與舊五個版本相同。最新版本包含效能改進和錯誤修正，因此建議您使用最新版本。

**強烈建議**&#x200B;您修正層級 4 或層級 5 的結果。

**建議**&#x200B;您修正層級 1 到層級 3 的結果。

## Auditor 會對哪些 Adobe 技術評分？{#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID 服務 (先前稱為 Marketing Cloud ID 服務)
* Target

下列 Adobe 解決方案目前未包含在測試規則中。這些解決方案的支援預計會在未來的更新提供。

* Advertising Cloud Creative
* Audience Manager
* 促銷活動
* Launch

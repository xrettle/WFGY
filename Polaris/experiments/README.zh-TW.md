# Polaris 實驗證據包繁體中文版 🌌

> English version: [`README.md`](./README.md)  
> 說明：目前不是每一個 WFGY 頁面都有繁體中文版本。若繁體中文頁面和英文頁面有差異，請以英文頁面作為主要參考版本。

這裡是 **WFGY 5.0 Polaris Protocol** 的公開實驗證據頁。

這一頁的目的很簡單：

讓你不用先下載 ZIP，也能先看懂這批實驗在驗證什麼、為什麼跟 AI 成本有關、公開證據包各自代表什麼，以及目前結果能說什麼、不能說什麼。

ZIP 檔主要是給想重現、研究、審核、檢查公開證據紀錄的人使用。

官方 repository：

https://github.com/onestardao/WFGY

授權：

除非特定檔案另有說明，否則採用 MIT License。

<a id="top"></a>

---

## 快速導覽 🧭

| 你想看什麼 | 跳到哪裡 |
| --- | --- |
| 先看懂這批實驗 | [3 分鐘快速看懂](#quick-start) |
| 各包分別是什麼 | [七個公開證據包](#evidence-packs) |
| 為什麼新增 PP02D | [社群建議補充實驗](#community-follow-up) |
| 核心數據是多少 | [核心結果總覽](#results) |
| 題目有沒有偷懶 | [題目設計與嚴謹性](#rigor) |
| 黑粉質疑怎麼回答 | [FAQ 與黑粉攻擊](#faq) |
| 想下載或重現 | [下載與檔案驗證](#downloads) |
| 哪些不能宣稱 | [宣稱邊界](#claim-ceiling) |

---

<a id="quick-start"></a>

## 3 分鐘快速看懂 ⚡

現在 AI 成本越來越高，不只是因為模型變大，也因為很多任務會把大量背景、規則、限制、範例和上下文反覆塞進模型。

模型每次讀越多 token，推理成本就越高。

Polaris 實驗問的是：

> 如果我們不要每次都把整本說明書丟給模型，而是先把任務整理成更穩定的結構，再交給模型輸出，能不能在少很多 token 的情況下，仍然保留可檢查的輸出品質？

這不是單純把 prompt 剪短。

單純剪短 prompt，可能會把重要限制、邊界、評分條件和錯誤檢查一起剪掉。Polaris 的重點不是粗暴刪字，而是把任務裡真正重要的關係整理出來。

它要保留的是：

| 要保留的東西 | 為什麼重要 |
| --- | --- |
| 任務目標 | 確認模型知道要完成什麼 |
| 限制條件 | 防止模型亂走 |
| 順序關係 | 防止步驟跳掉 |
| 邊界規則 | 防止過度延伸 |
| 錯誤風險 | 防止常見假成功 |
| 審核條件 | 讓結果可以被檢查 |

白話說：

傳統長上下文做法，像是每次都把整本城市百科全書交給模型。

Polaris 的做法，像是先畫出城市地圖、道路關係、危險區域、目的地和檢查點。

重點不是把資訊變少。

重點是把資訊變清楚。

一句話說：

> Polaris 不是把任務變小，而是把任務變清楚。🧠

<details>
<summary>展開：這跟 GPU 成本有什麼關係？</summary>

很多人談 AI 成本時，會先想到 GPU。

這沒有錯。GPU 是模型推理成本的重要底層。

但真正進到使用場景時，成本不只來自 GPU 本身，也來自每一次模型要讀多少 token、生成多少 token、跑多少輪、被多少長上下文拖住。

如果每次任務都要塞一大包背景文字，模型就要反覆讀很多內容。

這會變成成本。

Polaris 的思路是：

除了追求更大的模型、更強的 GPU、更長的上下文，我們也可以反過來問：

任務本身能不能先被整理得更聰明？

如果任務可以被整理成更穩定的結構，模型可能不需要每次重讀一整座圖書館，而是讀一張更清楚的任務地圖。

所以 Polaris 不是說 GPU 不重要。

它是在說：

AI 成本不只可以從硬體端解，也可以從任務結構端解。

</details>

<details>
<summary>展開：這不是單純把提示詞變短</summary>

如果只是把提示詞剪短，通常會丟失資訊，品質也可能下降。

Polaris 的實驗重點不是粗暴刪字，而是把任務內容重新整理成更穩定的結構。

可以想像成：

| 原本長文字 | 轉換後 |
| --- | --- |
| 一大段任務說明 | 任務節點 |
| 很多規則 | 規則關係 |
| 多個目標 | 目標順序 |
| 多種限制 | 邊界條件 |
| 可能錯誤 | 審核點 |
| 最後輸出 | 結果格式 |

這樣模型收到的不是一團很長的文字，而是一個比較清楚的任務結構。

模型接下來要做的事，比較像是：

讀懂這張任務地圖。  
把地圖翻譯回正確輸出。  
完成題目要求。

所以你可以把它理解成：

先把任務變成結構，再讓模型把結構翻譯成答案。

</details>

[回到快速導覽](#top)

---

<a id="evidence-packs"></a>

## 七個公開證據包 📦

目前本頁正式公開七個主要證據包。

它們不是七份重複資料，而是不同角度的證據。

前四包 PP01 到 PP02C，是原本的公開證據層。後三包 PP02D_A、PP02D_B、PP02D_C，是在社群回饋後補上的補充證據層，其中包含來自 [Zaious (@ChronicleCore)](https://github.com/Zaious) 的建議方向。

PP02D 不是取代前面的證據包，而是補上更多檢查：API 穩定性、hardcase final-run gates，以及公開 QA noninferiority。

| 證據包 | 它回答的問題 | 一句話看懂 |
| --- | --- | --- |
| PP01 / 主證據整合包 | 任務結構化後，能不能降低 token 成本，同時保留品質 | 成本主戰場 |
| PP02A | T4 分支是否能從較弱版本走到最後通過 | 版本演化證據 |
| PP02B | 偏數學任務是否能形成可檢查的結構化證據鏈 | 數學壓力測試 |
| PP02C | 程式修復是否能守住來源、沙盒與硬性紅線 | 黑粉紅線測試 |
| PP02D_A | sharded API fixtures 是否能在穩定性檢查下保留結構化輸出 | API 穩定性補充 |
| PP02D_B | hardcase final-run gates 是否能在沒有 parser rescue 或 semantic fallback 的情況下通過 | hardcase final-run 補充 |
| PP02D_C | 公開 QA compact context 是否能降低成本，同時維持可檢查 QA 指標的 noninferiority | 公開 QA noninferiority 補充 |

### PP01 / 主證據整合包

這是最適合第一次接觸者先看的主包。

它回答的是：

結構化任務表示，能不能在少很多 token 的情況下，仍然保留可檢查的輸出品質？

本頁把 `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` 視為 **PP01 / 主證據整合包** 與目前公開證據總入口。

### PP02A

這包看的是 T4 證據分支。

它的重點不是只放最後漂亮結果，而是保留版本演化痕跡，讓讀者知道這不是只挑一張勝利截圖。

### PP02B

這包看的是偏數學任務。

它不宣稱所有數學問題都已經解決，而是展示在這組任務裡，模型輸出、整理結果、家族判定、合約檢查與證書結果如何形成可檢查的證據鏈。

### PP02C

這包看的是程式修復、沙盒檢查、來源邊界與硬性紅線。

程式修復最容易出現假成功，例如亂猜 repo、誤用 metadata、跟隨干擾來源、沒有證據卻宣稱精準修補。PP02C 就是專門檢查這些問題。

### PP02D_A

這包看的是 sharded API stability 與 output preservation checks。

它補上 216 個 fixture 的證據，檢查 structured outputs、support checks、aggregate support checks、counterfactual checks 與 poison-rejection checks 是否能在 API-style sharding 下穩定通過。

### PP02D_B

這包看的是 hardcase final-run API evidence。

它檢查 216 次 API calls 中的 transport success、parse success、certificate exactness、arena valid-set matching、valid recall 與 invalid rejection。

### PP02D_C

這包看的是 public QA noninferiority under compact context。

它使用 100 題公開 QA cases，比較 baseline raw context 與 Polaris compact context 在兩個模型層級下的表現。它不是要宣稱全域 QA 優越，而是公開一組可檢查證據：在這個公開測試範圍內，compact context 能降低 token 成本，同時維持可比較的 QA 訊號。

[回到快速導覽](#top)

---

<a id="community-follow-up"></a>

## 社群建議補充實驗 🤝

PP02D_A、PP02D_B、PP02D_C 是在社群回饋後補上的補充實驗。

第一層公開證據準備完成後，社群回饋指出，如果能把幾個容易被質疑的壓力點補上，整體公開證據會更完整。

特別感謝 [Zaious (@ChronicleCore)](https://github.com/Zaious) 建議把這些補充檢查做得更明確。

這三包 PP02D 補充實驗由 WFGY / OneStarDAO 這邊實作與發布。它們應被理解為額外公開實驗證據，不是第三方驗證、不是官方 benchmark 認證，也不是核心數學公開。

PP02D 補上的內容：

| 補充包 | 補了什麼 | 為什麼重要 |
| --- | --- | --- |
| PP02D_A | 216-fixture sharded API stability 與 preservation checks | 補上 structured outputs、support checks、counterfactual checks、poison-rejection checks 在 API-style sharding 下能否穩定保留 |
| PP02D_B | 216-call hardcase final-run evidence | 補上 hardcase gates 是否能在沒有 parser rescue、semantic fallback、certificate mismatch、valid-set mismatch 的情況下通過 |
| PP02D_C | 100-case public QA noninferiority pilot | 補上 baseline raw context 與 Polaris compact context 的公開 QA 比較，並包含 token 與成本下降紀錄 |

白話說：

PP01 到 PP02C 建立了第一層公開證據。

PP02D_A 到 PP02D_C 則是在容易被懷疑的地方多補幾道壓力檢查，讓整體實驗更完整、更難被一句話打掉。

這不改變宣稱邊界。

PP02D 讓公開證據層更寬、更可檢查，但它不宣稱所有 AI 任務都已解決、不宣稱小模型全面打敗大模型，也不代表完整核心數學已經公開。

[回到快速導覽](#top)

---

<a id="results"></a>

## 核心結果總覽 📊

目前公開的是 WFGY 5.0 Polaris Protocol 預發布階段的第一層實驗證據。

這一層重點是公開結果、證據鏈與可審核材料，不是完整開源執行包。

| 項目 | 數量或狀態 |
| --- | ---: |
| 主要公開證據包 | 7 |
| 原始 PP01–PP02C 主要測試案例 | 680 |
| 原始 PP01–PP02C 主要模型輸出 | 3600 |
| PP02D_A fixtures | 216 |
| PP02D_B final-run API calls / raw outputs | 216 |
| PP02D_C 公開 QA cases | 100 |
| PP02D_C model-arm output records | 400 |
| 內含完整核心數學 | 0 |
| 內含完整 Colab 執行 notebook | 0 |

目前公開版本可以支持的是：

> 在目前公開的任務範圍內，Polaris 顯示出一個值得重視的訊號：任務如果先被整理成更穩定的結構，就有機會降低 token 成本，同時保留可檢查的輸出品質。

目前公開版本不應被解讀為：

| 不應解讀為 | 說明 |
| --- | --- |
| 所有 AI 任務都已經解決 | 目前只覆蓋指定公開任務範圍 |
| 小模型全面打敗大模型 | 目前證明的是指定任務中的結構化效果 |
| GPU scaling 已經不重要 | GPU 仍然重要，Polaris 是任務結構端的成本路線 |
| 第三方官方 benchmark | 這是自建公開實驗證據鏈 |
| 完整核心數學已公開 | 目前公開的是證據包，不是完整核心 |
| 完整 Colab 重現流程已公開 | 完整重現材料會在正式開源發布後補上 |

完整核心數學、正式重現材料與更多發布內容，預計在正式開源發布後逐步補上。

<details>
<summary>展開：七包詳細結果快照</summary>

### PP01 / 主證據整合包

| 指標 | 數值 |
| --- | ---: |
| 測試案例 | 320 |
| 測試組別 | 6 |
| 預期輸出 | 1920 |
| 實際輸出 | 1920 |
| 解析通過率 | 1.0 |
| 洩漏數 | 0 |
| C 組平均分數 | 0.988465 |
| B 組平均分數 | 0.967265 |
| C 組相對 B 組保留率 | 1.0219 |
| C 組相對 A 組總 token 比例 | 0.1656 |
| C 組相對 A 組輸入 token 比例 | 0.1242 |
| 失敗特徵吻合率 | 1.0 |
| 過度宣稱數 | 0 |
| 關鍵錯誤來源數 | 0 |
| 類別崩潰數 | 0 |
| 硬性檢查通過 | true |
| 最終通過 | true |
| 全域狀態 | `OSK_MVP_FINAL_PASS` |

### PP02A

| 指標 | 最終數值 |
| --- | ---: |
| 測試案例 | 120 |
| 最終 run 原始輸出 | 240 |
| 領域數 | 6 |
| API 錯誤數 | 0 |
| 解析失敗數 | 0 |
| 解析成功率 | 1.0 |
| 弱列數 | 0 |
| 達到 seal 的領域數 | 6 |
| 達到 dominant 或更好層級的領域數 | 6 |
| 達到 release 或更好層級的領域數 | 6 |
| T4 系統分數 | 100.0 |
| 內部加權分數 | 125.0 |
| 最終結果 | `SEAL_PASS` |

PP02A 也保留前一版較弱參考紀錄：解析成功率 0.9958、弱列數 1、達到 seal 的領域數 5、最終結果 `INVALID`。

### PP02B

| 指標 | 數值 |
| --- | ---: |
| 測試案例 | 120 |
| 預期編譯輸出 | 120 |
| 實際編譯輸出 | 120 |
| 預期總輸出 | 720 |
| 實際總輸出 | 720 |
| 預期模型壓力輸出 | 600 |
| 實際模型壓力輸出 | 600 |
| 模型 API 呼叫 | 600 |
| C 組解析通過率 | 1.0 |
| C 組合約通過率 | 1.0 |
| 家族紅燈數 | 0 |
| 編譯驗證紅燈數 | 0 |
| 模型壓力警告數 | 0 |
| 模型壓力結果 | `MODEL_STRESS_PASS` |
| 主證書結果 | `T4_MAIN_CERTIFICATE_PASS` |
| 最終結果 | `T4_MAIN_CERTIFICATE_PASS` |

### PP02C

| 指標 | 數值 |
| --- | ---: |
| 主要測試案例 | 120 |
| 每題測試組別 | 6 |
| 預期主要輸出 | 720 |
| 實際主要輸出 | 720 |
| 解析通過率 | 1.0 |
| 硬性紅線數 | 0 |
| 警告數 | 0 |
| 程式庫幻覺數 | 0 |
| 把 metadata 當證據的次數 | 0 |
| 把干擾來源當正式來源的次數 | 0 |
| 忽略來源優先順序的次數 | 0 |
| 沒有來源卻宣稱精準修補的次數 | 0 |
| 合約缺欄位數 | 0 |
| 合約列舉值錯誤數 | 0 |
| 合約值不一致數 | 0 |
| 宣稱邊界通過率 | 1.0 |
| 超額通過分數 | 120 |
| 最終分支結果 | `FULL_SANDBOX_STRONG_PASS` |

PP02C 也包含沙盒 run、全域硬性紅線矩陣、迷你預檢與干擾來源矩陣等支援檢查。

### PP02D_A

| 指標 | 數值 |
| --- | ---: |
| Fixture count | 216 |
| Shard count | 6 |
| API exception count | 0 |
| Shard parse fail count | 0 |
| Parse fail count | 0 |
| Fixture pass count | 216/216 |
| Semantic support checks | 1944/1944 |
| Aggregate support union checks | 216/216 |
| Total support closure checks | 2160/2160 |
| Forbidden-use count | 0 |
| Hard-zero count | 0 |
| Counterfactual pairs pass | 180/180 |
| DeltaHitScore | 1.0 |
| StabilityScore | 1.0 |
| CounterfactualScore | 1.0 |
| Poison reject count | 12/12 |
| Schema budget pass | true |
| 最終結果 | `GREEN` |

### PP02D_B

| 指標 | 數值 |
| --- | ---: |
| API calls | 216/216 |
| Transport pass | 216/216 |
| Transport fail | 0 |
| Parse pass | 216/216 |
| Parse fail | 0 |
| Parser rescue count | 0 |
| Semantic fallback count | 0 |
| Certificate exact | 216/216 |
| Arena valid-set match | 54/54 |
| Valid recall | 108/108 |
| Invalid rejection | 108/108 |
| 最終結果 | `GREEN` |
| Claim ceiling | `API_216_EVIDENCE_ONLY_NOT_GLOBAL_PROOF` |

### PP02D_C

| 指標 | 數值 |
| --- | ---: |
| 公開 QA cases | 100 |
| Models | `gpt-4.1-mini`, `gpt-4.1` |
| Arms | baseline raw context, Polaris compact context |
| Model-arm output records | 400 |
| Parse pass records | 400/400 |
| Metadata leakage fail count | 0 |
| Self-grading fail count | 0 |
| API key pattern in prompts count | 0 |
| Baseline answer F1 mean, both models | 0.7884761905 |
| Compact-context answer F1 mean, both models | 0.7941428571 |
| Baseline support-title F1 mean, both models | 0.8966666667 |
| Compact-context support-title F1 mean, both models | 0.8453333333 |
| Token reduction, compact vs baseline | 0.3704355582 |
| Estimated cost reduction, compact vs baseline | 0.3124261543 |
| Baseline wrong-source total, both models | 2 |
| Compact-context wrong-source total, both models | 5 |
| Baseline hallucinated-detail total, both models | 0 |
| Compact-context hallucinated-detail total, both models | 1 |
| 最終結果 | `GREEN` |
| Claim ceiling | `100_CASE_PUBLIC_HOTPOTQA_MODEL_LADDER_EVIDENCE_ONLY` |

Model-ladder detail：

| Model | Arm | Answer F1 mean | Support-title F1 mean | Wrong-source total | Hallucinated-detail total | Estimated cost USD |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `gpt-4.1` | `A_BASELINE_RAW_CONTEXT` | 0.7791428571 | 0.9026666667 | 1 | 0 | 0.498238 |
| `gpt-4.1` | `B_POLARIS_COMPACT_CONTEXT` | 0.7819761905 | 0.8403333333 | 3 | 1 | 0.342512 |
| `gpt-4.1-mini` | `A_BASELINE_RAW_CONTEXT` | 0.7978095238 | 0.8906666667 | 1 | 0 | 0.099630 |
| `gpt-4.1-mini` | `B_POLARIS_COMPACT_CONTEXT` | 0.8063095238 | 0.8503333333 | 2 | 0 | 0.068566 |

</details>

[回到快速導覽](#top)

---

<a id="rigor"></a>

## 題目設計與嚴謹性 🧪

這批實驗不是用幾題展示題來炫技。

如果只拿幾個模型剛好會回答的題目，確實可以做出很好看的頁面，但那種結果沒有太大研究價值。

Polaris 這批實驗採用的是家族化設計。

意思是：

不是只問「模型有沒有答對」，而是把不同失敗型態拆開，分別檢查模型在不同壓力下能不能守住任務結構、來源邊界、錯誤檢查與宣稱範圍。

簡單說：

> 不是挑幾條好走的路給模型散步，而是先把容易跌倒的坑標出來，再看它能不能穩定走過去。🕳️

### 為什麼不用單題展示？

單題展示很容易有三個問題：

| 問題 | 風險 |
| --- | --- |
| 題目太少 | 可能只是模型剛好會 |
| 題目太順 | 看不出邊界與失敗風險 |
| 只看最後答案 | 看不到模型是否偷跳步驟、亂猜來源或過度宣稱 |

所以這批實驗不是只看最後輸出漂不漂亮。

它同時檢查：

| 檢查方向 | 為什麼重要 |
| --- | --- |
| 任務是否保持原意 | 防止模型把問題改成比較容易回答的版本 |
| 條件是否被保留 | 防止模型忽略限制 |
| 來源是否可靠 | 防止模型亂猜或用錯資料 |
| 是否過度宣稱 | 防止模型把局部結果吹成通用結論 |
| 是否有洩漏 | 防止題目或答案污染結果 |
| 是否踩到硬性紅線 | 防止漂亮答案掩蓋不可接受錯誤 |
| 是否能回查原始輸出 | 防止只看整理後結果而無法驗證 |

### 各分支測什麼風險？

| 分支 | 主要測試方向 | 它防的是什麼 |
| --- | --- | --- |
| PP01 / 主證據整合包 | token 成本下降與品質保留 | 只省 token 但品質崩壞，或靠洩漏與過度宣稱撐結果 |
| PP02A | T4 證據分支與版本演化 | 只放最後漂亮結果，不保留過程脈絡 |
| PP02B | 偏數學任務結構化測試 | 符號漂移、條件遺失、錯誤等價、反例忽略 |
| PP02C | 程式修復、來源邊界、沙盒檢查與硬性紅線 | repo 幻覺、metadata 誤用、干擾來源誤用、沒有證據卻宣稱精準修補 |
| PP02D_A | Sharded API stability 與 output preservation | 摘要看起來通過，但 parse、support 或 counterfactual checks 失敗 |
| PP02D_B | Hardcase final API evidence | transport failure、parser rescue dependency、certificate mismatch、valid-set mismatch |
| PP02D_C | Public QA noninferiority pilot | token 下降但 QA 品質悄悄掉落、leakage 增加或宣稱膨脹 |

這些分支不是重複測同一件事。

它們分別對應不同風險面。

PP01 看成本主訊號。

PP02A 看證據路徑。

PP02B 看偏數學推理壓力。

PP02C 看程式修復與黑粉紅線。

PP02D_A 看 sharded API stability 與 preservation。

PP02D_B 看 hardcase final-run gates。

PP02D_C 看 compact context 下的公開 QA noninferiority。

<details>
<summary>展開：題目是不是故意設計得很鬆？</summary>

不是。

更精準的說法是：

題目不是為了讓模型看起來很厲害而設計，而是為了讓常見錯誤有機會暴露出來。

PP01 不只看 token 變少，也看品質、洩漏、錯誤來源與過度宣稱。

PP02A 不只看最後通過，也保留前一版較弱參考紀錄。

PP02B 不只看數學答案漂不漂亮，也看符號、條件、假設、反例與推理結構。

PP02C 不只看程式回答像不像，也看來源使用、沙盒檢查、干擾來源與硬性紅線。

PP02D_A 不只看 summary 是否綠燈，也看 fixtures、support closure、counterfactual pairs、poison rejection 與 parse stability。

PP02D_B 不只看 API run 是否完成，也看 transport、parsing、certificate exactness、valid-set match、valid recall 與 invalid rejection。

PP02D_C 不只看 compact context 是否比較省 token，也看 answer F1、support-title F1、leakage、wrong-source totals、hallucinated-detail totals 與 cost records。

所以這批題目的設計不是放水。

它更接近：

> 把模型常見失敗路徑整理成測試場，再檢查 Polaris 是否能降低這些失敗。

</details>

<details>
<summary>展開：自建實驗為什麼仍然有價值？</summary>

這是自建公開實驗，不是第三方官方 benchmark。

所以它不能被包裝成外部權威排名。

但自建實驗仍然可以有價值，前提是它不能只放最後分數。

它必須讓讀者可以往回檢查：

| 如果只放結果 | 可信度問題 |
| --- | --- |
| 只放總分 | 不知道每題怎麼判 |
| 只放截圖 | 不知道模型原始輸出 |
| 只放漂亮案例 | 不知道是否挑結果 |
| 只放結論 | 不知道是否過度宣稱 |
| 不放檔案指紋 | 不知道檔案是否一致 |

這次公開的做法是把證據鏈放出來：

模型原始輸出。  
整理後結果。  
每題判定。  
token 成本。  
審核紀錄。  
警告紀錄。  
硬性紅線。  
檔案指紋。

所以這批資料的定位不是：

> 請相信我們很強。

而是：

> 這是目前公開的實驗軌跡，你可以從結果往回檢查。

</details>

[回到快速導覽](#top)

---

<a id="faq"></a>

## FAQ 與黑粉攻擊 🛡️

這一區專門回答第一次接觸者和懷疑者最常問的問題。

<details>
<summary>Q1. 這是不是只是把 prompt 寫短？</summary>

不是。

短 prompt 是減字。

Polaris 是整理任務結構。

如果只是剪短文字，很容易把限制、邊界、評分條件和錯誤檢查一起剪掉。Polaris 要做的是保留這些關鍵資訊，只是把它們整理成模型更容易使用的任務地圖。

白話說：

傳統做法像是每次都搬一整本百科全書給模型看。

Polaris 的方向比較像是先畫好地圖，再讓模型照著地圖完成任務。

</details>

<details>
<summary>Q2. 這是不是自己做實驗自己爽？</summary>

這是自建公開實驗，不是第三方官方 benchmark。

但它仍然有價值，因為它不是只放最後分數。

這批資料公開的是一條證據鏈，包含模型原始輸出、整理後結果、每題判定、token 成本、審核紀錄、警告紀錄、硬性紅線與檔案指紋。

所以它的定位不是外部排名，而是可回查的公開實驗證據。

更精準地說：

這不是要你先相信我們很強。

這是先把實驗軌跡放出來，讓你可以從結果往回檢查。

</details>

<details>
<summary>Q3. 題目是不是故意設計得很簡單？</summary>

不是用單題展示，而是用家族化壓力設計。

這些分支不是只測舒服場景，而是分別檢查不同類型的失敗風險。

所以這批題目的設計不是放水。

它更接近：

把模型常見失敗路徑整理成測試場，再檢查 Polaris 是否能降低這些失敗。

</details>

<details>
<summary>Q4. 有沒有偷放答案或污染題目？</summary>

公開包不是只放總分，也包含洩漏檢查、原始輸出、整理後結果與審核紀錄。

這不代表未來所有實驗都永遠不會出錯。

它代表這次公開資料不是只給一張漂亮截圖，而是留下可以回查的檢查材料。

例如：

PP01 會看洩漏、錯誤來源、過度宣稱與類別崩潰。

PP02C 會看來源行為、干擾來源、metadata as evidence、沙盒檢查與硬性紅線。

PP02D_C 會看 metadata leakage、self-grading risk、API key pattern risk、wrong-source totals 與 hallucinated-detail totals。

這些檢查的目的，就是避免模型靠偷吃答案、亂引用來源，或把不該當證據的東西當證據。

</details>

<details>
<summary>Q5. 這是否代表小模型全面打敗大模型？</summary>

不代表。

比較精準的說法是：

在目前公開的指定任務範圍內，Polaris 顯示出任務結構化後降低 token 成本並保留可檢查輸出品質的訊號。

這不能被解讀成所有小模型都全面勝過所有大模型。

也不能被解讀成所有 AI 任務都已經解決。

目前可以說的是：

在這些公開測試分支裡，結構化任務表示出現了值得重視的成本與品質訊號。

</details>

<details>
<summary>Q6. 這是否代表 GPU scaling 不重要？</summary>

不代表。

GPU 仍然重要。

Polaris 的重點是從另一個方向降低成本，也就是先改善任務本身的表示方式，減少模型每次需要重讀的大量上下文。

換句話說：

硬體 scaling 是一條路。

任務結構優化是另一條路。

這批實驗不是在說 GPU 不重要，而是在展示：

AI 成本也可以從任務結構端被重新思考。

</details>

<details>
<summary>Q7. 為什麼 ZIP 裡沒有完整核心數學與完整 Colab？</summary>

因為這一版公開的是預發布階段的證據包，不是完整執行包。

目前目的，是先讓讀者看到模型原始輸出、判定、成本、審核、警告、紅線與檔案指紋。

完整核心數學、正式重現材料與更多發布內容，會在正式開源發布後逐步補上。

簡單說：

這一版先公開證據。

後續再公開更深層的數學邏輯與重現材料。

</details>

<details>
<summary>Q8. 這次公開最重要的意義是什麼？</summary>

最重要的不是放了很多 ZIP。

最重要的是：

先公開證據，再公開更深層的數學與執行材料。

這代表讀者不必只看截圖或相信口號，而是可以先看到模型原始輸出、整理後結果、判定表、token 成本、審核紀錄與檔案指紋。

換句話說：

這批資料不是要求你先相信。

它是先把公開證據鏈放出來，讓你可以看懂，也可以往回檢查。✨

</details>

<details>
<summary>Q9. 為什麼新增 PP02D_A、PP02D_B、PP02D_C？</summary>

這三包是社群建議後補上的補充實驗。

PP01 到 PP02C 已經覆蓋第一層公開證據：成本訊號、版本演化、偏數學任務與程式修復紅線。

PP02D 則補上讀者可能合理要求的更多壓力檢查：

API 穩定性。

Hardcase final-run gates。

Compact context 下的公開 QA noninferiority。

特別感謝 [Zaious (@ChronicleCore)](https://github.com/Zaious) 建議把這些補充檢查做得更明確。

這不改變宣稱邊界。PP02D 讓公開證據層更完整、更可檢查，但它仍然不是完整核心數學公開，也不是第三方官方 benchmark。

</details>

<details>
<summary>Q10. 為什麼 PP02D_C 移除了 public prompt bodies？</summary>

PP02D_C 是公開證據包，不是核心方法公開包。

公開 ZIP 保留的是結果證據：case manifest、raw outputs、parser records、scorer traces、leakage audits 與 verdicts。

Prompt bodies 與 compact-selection trace internals 先排除，避免在正式開源前暴露尚未公開的方法細節。

公開版 PP02D_C 也把上傳來源裡的 `DD02C` 標籤正規化為 `PP02D_C`，並把殘留的 `full_30` artifact 檔名改為 `full100`。但 raw model JSON bodies 會保留原樣，以維持 hash integrity。

</details>

[回到快速導覽](#top)

---

<a id="downloads"></a>

## 下載與檔案驗證 🧾

如果你只是想快速理解，看完這個 README 就夠。

ZIP 主要是給想重現、研究、審核或檢查原始輸出的人使用。

目前正式公開證據包以這七個檔案為準：

| 正式名稱 | 檔案 | 用途 |
| --- | --- | --- |
| PP01 / 主證據整合包 | `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | 成本主證據與公開證據總入口 |
| PP02A | `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | T4 證據分支與版本演化 |
| PP02B | `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | 偏數學任務結構化測試 |
| PP02C | `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | 程式修復、沙盒檢查與硬性紅線 |
| PP02D_A | `wfgy5_polaris_protocol_pp02d_a_public_evidence_20260504.zip` | 216-fixture sharded API stability 與 preservation checks |
| PP02D_B | `wfgy5_polaris_protocol_pp02d_b_public_evidence_20260504.zip` | 216-call API hardcase final-run evidence |
| PP02D_C | `wfgy5_polaris_protocol_pp02d_c_public_evidence_20260504.zip` | Public QA noninferiority pilot evidence |

下載連結：

| 檔案 | 下載 |
| --- | --- |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip) |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02d_a_public_evidence_20260504.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02d_a_public_evidence_20260504.zip) |
| `wfgy5_polaris_protocol_pp02d_b_public_evidence_20260504.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02d_b_public_evidence_20260504.zip) |
| `wfgy5_polaris_protocol_pp02d_c_public_evidence_20260504.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02d_c_public_evidence_20260504.zip) |

目前 downloads 資料夾中可能保留部分早期過程檔案。

第一次閱讀請以上面七個正式公開證據包為準。

<details>
<summary>展開：工程師建議檢查順序</summary>

| 順序 | 建議檢查 | 為什麼重要 |
| --- | --- | --- |
| 1 | 模型原始回答 | 確認這次 run 真的產生了模型回應 |
| 2 | 整理後輸出 | 檢查輸出如何轉成結構化紀錄 |
| 3 | 每題或每個 fixture 的判定 | 檢查每個 case 如何對應到結果 |
| 4 | 分組或階段判定 | 檢查更高層級的結果模式 |
| 5 | token 成本紀錄 | 檢查成本與 token efficiency behavior |
| 6 | 審核紀錄 | 檢查 leakage、warning、hard veto 或 source quality checks |
| 7 | SHA256 紀錄 | 檢查檔案完整性 |

</details>

<details>
<summary>展開：SHA256 檔案指紋</summary>

SHA256 可以理解成檔案指紋。

它不是用來證明實驗結論一定正確，而是用來確認你下載到的 ZIP 是否和公開紀錄一致。

| 檔案 | SHA256 |
| --- | --- |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | `50ed006c83f25d69b3080da044882e21663ada2cecb432622b843411d078657e` |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | `28f2ca19a0a6bac27967bedbc07b4c2f9b44f1c212687ae74512967d42a2e7ad` |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | `10c5d39a15d74afb29d89386147ba60e830fc624b050d53f0e4187c97fe3df65` |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | `a85b7919da2fae8c543189fbaf586e3573af73642a1e410e49e5df6a5e6bb9f8` |
| `wfgy5_polaris_protocol_pp02d_a_public_evidence_20260504.zip` | `3915a336566074344314ced1c9c332640f659019d6278e434e18e987118af299` |
| `wfgy5_polaris_protocol_pp02d_b_public_evidence_20260504.zip` | `0fcd4529f531b5a0c8724183c7034f36b083995509fb977ddaa81a34f14a76a5` |
| `wfgy5_polaris_protocol_pp02d_c_public_evidence_20260504.zip` | `2a372b926f2aeb7fa8043018dedb45087d8a5ab45be24c035bdd24d06bb85d8b` |

</details>

[回到快速導覽](#top)

---

<a id="claim-ceiling"></a>

## 宣稱邊界 🚧

這批資料目前可以說：

| 可以說 | 說明 |
| --- | --- |
| Polaris 在公開任務範圍內顯示出降低 token 成本的訊號 | 尤其是 PP01 主成本實驗與 PP02D_C 公開 QA pilot |
| 結構化任務表示有機會保留可檢查輸出品質 | 不是只看答案好不好看，也看證據鏈 |
| 公開包覆蓋不同風險面 | 成本、版本演化、偏數學、程式修復、API 穩定性、hardcase gates 與公開 QA |
| ZIP 可供研究者與懷疑者往回檢查 | 包含原始輸出、判定、成本、審核與檔案指紋 |

這批資料目前不能說：

| 不能說 | 原因 |
| --- | --- |
| 所有 AI 任務都已經解決 | 目前只覆蓋指定公開任務範圍 |
| 小模型全面打敗大模型 | 目前證明的是指定任務中的結構化效果 |
| GPU scaling 已經不重要 | GPU 仍然重要，Polaris 是任務結構端的成本路線 |
| 這是第三方官方 benchmark | 這是自建公開實驗證據鏈 |
| ZIP 已包含完整核心數學 | 目前公開的是證據包，不是完整核心 |
| 目前已提供完整 Colab 重現流程 | 完整重現材料會在正式開源發布後補上 |

一句話收斂：

> 這批資料不是要求你先相信，而是先把公開證據鏈放出來，讓你可以看懂，也可以往回檢查。✨

[回到快速導覽](#top)

---

## 建議短描述 ✍️

WFGY 5.0 Polaris Protocol 的公開證據層，包含模型原始輸出、整理後輸出、判定表、token 成本紀錄、審核紀錄、SHA256 檔案指紋、原始 PP01–PP02C 證據層，以及社群建議後補上的 PP02D_A–PP02D_C 補充證據層。

---

## 目前狀態 📌

| 欄位 | 內容 |
| --- | --- |
| 專案 | WFGY 5.0 Polaris Protocol |
| 資料夾角色 | 公開實驗證據層 |
| 發布類型 | 第一層公開證據 |
| 公開分支 | PP01、PP02A、PP02B、PP02C、PP02D_A、PP02D_B、PP02D_C |
| 主要證據包 | 7 |
| 原始 PP01–PP02C 測試案例 | 680 |
| 原始 PP01–PP02C 模型輸出 | 3600 |
| 追加 PP02D_A fixtures | 216 |
| 追加 PP02D_B API calls / raw outputs | 216 |
| 追加 PP02D_C 公開 QA cases | 100 |
| 追加 PP02D_C model-arm output records | 400 |
| 模型原始輸出 | 公開安全範圍內已包含 |
| 整理後輸出 | 公開安全範圍內已包含 |
| 判定檔 | 已包含 |
| 審核檔 | 已包含 |
| token 成本紀錄 | 有資料處已包含 |
| SHA256 紀錄 | 已包含 |
| 執行 notebook | 未包含 |
| 核心數學 | 第一層公開證據尚未包含 |
| 完整實作發布 | 預計在正式開源發布開始後提供 |
| 授權 | 除非特定檔案另有說明，否則採用 MIT License |
| Repository | https://github.com/onestardao/WFGY |

---

## 最後說明 🌱

這個資料夾存在的目的，是在完整開源發布前先讓證據可見。

目前 packages 展示的是實驗軌跡：

測試設計、模型原始輸出、解析、評分、token 成本、審核、結果判定與檔案完整性紀錄。

PP02D 補充包加入了社群建議後補上的壓力檢查，同時維持相同的公開證據邊界。

完整數學邏輯與重現材料，預計會在正式開源發布開始後跟上。

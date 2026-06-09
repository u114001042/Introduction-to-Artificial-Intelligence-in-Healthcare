好的，這是一份根據您提供的演講逐字稿整理而成的重點摘要 `.md` 檔案。聽眾可以在聆聽演講時，快速瀏覽這份文件，以掌握演講的核心架構與關鍵資訊。

---

# 開源 AI 與智慧數位工作者新紀元：演講重點摘要

**演講者：** Kerri Briske & Adil
**主題：** Open Source AI: Shaping the Next Era of Intelligent Digital Workers

---

## 第一部分：關鍵時刻與趨勢

### 三大標誌性時刻
1.  **ChatGPT 時刻 (2022年底)**：生成式 AI 的爆發。
2.  **DeepSeek 時刻 (2025年1月)**：標誌著同步 tokens 與推理模型的重要性。
3.  **OpenClaw 時刻 (現在)**：不僅是推理，更是 **智慧體 (Agents) 與智慧體協同工作** 的時代。

### 關鍵趨勢：Token 消耗與算力需求爆炸性增長
- **Token 用量暴增**：過去回答一個問題約需 10,000 tokens。現在多個智慧體協作，可產生數萬至數十萬 tokens。
- **算力需求提升 15 倍**：Anthropic 報告指出，智慧體相互協作使算力需求提升 15 倍。
- **核心定律：算力 = 智慧 (Compute = Intelligence)**。

### OpenClaw 的歷史意義
- **小社區，大影響**：OpenClaw 是一個小型開源社區專案，但其影響力已超越 Linux。
- **對比 Linux**：Linux 用 30 年成為數位經濟的基石。OpenClaw 的崛起速度更快，預示著一個更重要的時代來臨。

---

## 第二部分：AI 智慧體 (AI Agents) 的演進

### 智慧體的定義與能力
一個完整的 AI 智慧體應具備：
1.  **思考與推理**：分析問題。
2.  **制定計劃**：規劃行動步驟。
3.  **採取行動**：執行任務並使用工具。

### 從單一智慧體到多智慧體協同
- **過去**：描述一個智慧體就已讓人感到複雜。
- **現在**：**多智慧體系統 (Multi-Agent Systems)** 成為現實。智慧體之間透過協定 (如 Agent-to-Agent Protocol) 溝通、分工、完成複雜目標。
- **未來**：智慧體不僅能「思考」和「對話」，更能 **「自主行動」** (Autonomously Doing)。

### 第四 Scaling Law (規模法則)
- **前三法則**：預訓練、後訓練、長思考 (推理)。
- **第四法則 (新增)**：**愈多智慧體協同工作，為達成共同目標而行動，其產出的目的性、智慧性和實用性就愈高。** 這將進一步驅動算力需求的成長。

---

## 第三部分：開源模型的崛起與 NVIDIA Nemotron

### 開源模型的使用量爆炸性成長
- **成長 35 倍**：根據 OpenRouter 的數據，開源模型在生產環境中的 token 生成量成長了 35 倍。
- **市佔率近半**：僅 2025 年 2 月，開源模型就佔了總生成 tokens 的 **48%**。企業為了降低成本，正大量將應用程式部分轉向開源模型。

### NVIDIA Nemotron 3 系列模型
- **命名由來**：Nemo (神經模組) + Megatron (強大變換器)。
- **三種尺寸**：Nano (小), Super (中), Ultra (大)。
- **核心架構：混合專家模型 (Mixture of Experts, MoE)** + **混合架構 (狀態空間模型 + Transformer)**。
    - **優點**：不僅智慧高，且 **極度高效**，能在相同硬體上運行更多 tokens。

### 最新發佈與成績
- **Nemotron 3 Super (GA)**：
    - 在 PinchBench 基準測試中獲得 **開源模型第一名**，總排名世界第四。
    - 評測重點：**現實世界任務** (如 coding、工具呼叫、OpenClaw 整合)。
- **Nemotron 3 Ultra (基礎模型)**：
    - 剛完成基礎訓練，已是 **世界最佳的基礎模型**。
    - **效率翻倍**：比市面上最佳開源模型還快兩倍。
    - 適合客戶進行後訓練 (Post-training) 或全微調 (Full Fine-tuning)。

### 其他重要模型
- **Parse & RAG**：
    - **Parse**：小型但強大的文件智慧模型，擅長理解 PDF 等非結構化資料 (如醫療、科學研究)。
    - **RAG**：多語言、多模態的嵌入模型，用於資訊檢索，性能表現優異。
- **Nemotron VoiceChat (Early Access)**：
    - 基於 NVIDIA 研究模型 PersonaPlex 開發。
    - 具備高度自然的 **對話動態 (Conversational Dynamics)**：如輪流發言、停頓處理、插話、來回確認等。
    - 可自由替換 ASR 和 LLM 元件。

---

## 第四部分：後訓練 (Post-Training) 與強化學習 (RL)

### 什麼是後訓練？
- **預訓練**：賦予模型「知識」。
- **後訓練**：教導模型如何「運用知識」與「行為表現」。

### 後訓練的關鍵：強化學習 (Reinforcement Learning)
- **機制**：建立各種「環境」(Gym Environments) 讓模型「練習」，並透過驗證者 (Verifier) 給予評分。
- **回饋循環**：即使答錯，也是學習機會。將結果回傳，持續訓練，並生成更多高品質的合成資料。
- **需要大量算力**：同時進行推理和訓練。

### RL 的應用與成效
- **殺手級應用：程式碼生成 (Code Generation)**。因為驗證很簡單：程式碼能否編譯？是否通過單元測試？
- **領域專業化**：RL 可應用於晶片設計 (EDA)、科學發現等特定領域。
- **成功案例**：
    - **Atlassian、SAP、Siemens EDA**：整合自身工具環境，讓模型學會使用這些工具。
    - **Edison Scientific**：用於加速阿茲海默症等科學研究。

---

## 第五部分：NVIDIA Agent Toolkit 與生態系

### AIQ：企業級深度研究智慧體藍圖
- **定義**：一個開源的參考藍圖，相當於觸手可及的研究實驗室。
- **運作流程**：
    1.  **意圖路由器**：判斷查詢是否需要深度研究 (內部統計超過70%為淺層研究)。
    2.  **協調器與規劃器**：維護待辦清單、管理記憶體、協調子智慧體。
    3.  **子智慧體團隊**：
        - 證據收集者 (Stats & Facts)
        - 比較者 (Benchmarks)
        - 視野前瞻者 (Event Horizon)
        - 框架分析者
        - **合成者**：整合所有成果為最終報告。
- **卓越的準確性與成本效益**：
    - 在 **Deep Research Bench 1 & 2** 雙雙拿下世界第一。
    - **成本降低 50%**：相較於純使用前沿專有模型。
    - **秘訣**：協調器/規劃器使用 GPT-5.2/Opus，**研究員子智慧體則使用經過微調的 Nemotron 3 Super**。

### OpenShell：安全為核心的智慧體運行環境
- **解決的痛點：Agent Paradox**
    - 智慧體要有用就需「自主性」，有自主性就需「權限」，有權限就更難「確保安全」。
- **解決方案：安全的沙盒 (Secure Sandbox)**
    - **預設拒絕 (Default Deny)**：所有權限需由管理員定義策略。
    - **策略強制執行引擎**：在沙盒內運行，不受智慧體控制。
    - **隱私路由器 (Privacy Router)**：
        - 敏感資訊 -> 路由至本地 LLM。
        - 可動態重寫查詢以移除 PII (個人識別資訊)，再發送給前沿模型。

### 生態系整合與合作案例
- **LangChain 整合**：將 NVIDIA Agent Toolkit 全面整合至 LangChain 生態系。
- **ServiceNow 案例**：
    - 使用多層級智慧體 (受理、分類、解決) 處理服務工單。
    - **成果：90% 的 L1 工單由 AI 智慧體自主解決。**
- **Edison Scientific 案例**：
    - 目標：將 6 個月的研究週期縮短為 1 天。
    - 運用 Parse、Nemotron RL、CUDA 等技術，加速阿茲海默症藥物發現。

### 推論架構：Dynamo 與 NIM 2.0
- **Dynamo**：分散式推論服務。
    - 功能：智慧調度 Pre-fill/Decode、KV Cache-aware routing、管理 K8s、模型熱替換。
    - **與 Agent Toolkit 整合**：透過 Profiler 分析智慧體工作負載，優化 AI 工廠 (AI Factory) 的路由。
- **NIM 2.0 (Early Access)**：
    - 基於 VLM 專案重構，並將優化貢獻回開源社群。
    - Day Zero 支援，開發者可無痛取得企業級支援。
    - **NIMD (內部專案名稱)**：將 Dynamo 的最佳功能帶入 NIM 容器。

---

## 總結：本次大會發佈重點

- **模型發佈**
    - Nemotron 3 Super (GA)
    - Nemotron 3 Ultra (最佳基礎模型)
    - VoiceChat (Early Access)
    - Parse 1.2
- **平台與工具**
    - Dynamo 1.0
    - NIM 2.0
    - AIQ 2.0
    - OpenShell
- **目標**：在 PinchBench、DeepBench、OCRBench 等各大評測基準中取得領先。這不僅是門檻，更是證明模型具備「上工」的能力。

### 行動呼籲
- **加入 Claw Mania**！
- 使用 **DGX Spark** 或 **DGX Station** (終極 Claw 平台)，立即動手 **Build Your First Claw**！
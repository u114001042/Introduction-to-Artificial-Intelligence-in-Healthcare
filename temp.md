## 2. GTC 2026 心得

在 2026 GTC 開始前，AI Agent 已是一個熱門概念。我曾在李弘毅老師的頻道學習 Agentic AI，但出於安全性考量並未實作。主要擔憂是代理可能會擅自更動硬碟中的資料，而為其配置獨立電腦與帳號的硬體與 token 成本過高。

本次 GTC 更新了我的看法：

- **OpenShell 的安全設計**：採用預設拒絕、策略引擎與隱私路由器機制，可漸進式賦予代理權限，讓個人助理的部署更為可行。
- **開源模型的成長**：市佔率已達 48%。Nemotron 3 Super 在 PinchBench 上緊追 GPT 與 Claude，且成本更低。這代表未來有機會本地端部署高品質 LLM，實現 24/7 個人 AI 助理（行程管理、郵件過濾、家庭安全監控、健康建議），同時降低 token 費用與隱私外洩風險。
- **硬體支援**：NVIDIA 推出 DGX Spark（原價屋售價 NT$135,000），可本地運行 120B 參數模型。雖然個人難以負擔，但對實驗室經費而言並非難事，可大幅提升隱私資料研究效率。

### 一個問題與解答

> **我問 AI：** 我只會寫簡單的 Python，不懂 RL，真的能建一個有用的代理嗎？
>
> **AI 答：** 完全可以。你可以從 Build-A-Claw 這類視覺化工具開始（如同演講中展示的積木組裝），用拖拉方式選擇 LLM 腦、工具（如 Telegram、網頁搜尋）。或是直接安裝 OpenClaw，以自然語言描述需求，它會自動產生設定檔。

**References:**
- [Open Source AI Shaping the Next Era of Intelligent Digital Workers](https://www.nvidia.com/zh-tw/on-demand/session/gtc26-s81789/)
- [Agentic AI 101](https://www.nvidia.com/zh-tw/on-demand/session/gtc26-s82432/)
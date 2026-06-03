# 🤖 設計實驗室 ｜ AI 設計部門 Skill
A multi-role AI design team skill for research, planning, scripting, design, and content production.
> 由設計實驗室 @pb_design_lab 專為內容創作者打造的 Claude AI 虛擬團隊，10 個專業角色分工協作，涵蓋從業配分析、內容企劃、腳本撰寫到社群發布的完整製作流程。

---

## 📖 這是什麼？

這套 Skill Pack 把 Claude 變成一個完整的**內容製作團隊**。每個 Skill 就是一個有專業角色定位、工作流程和輸出格式的 AI 成員。你可以根據任務需要，呼叫對應的角色來處理：

- 收到業配邀請？→ **Brief 解析師** 幫你拆解需求與風險
- 要研究一個 AI 工具？→ **AI 研究員** 幫你做功課
- 想發想影片切角？→ **內容企劃** 給你 3-5 個方向
- 腳本寫不出來？→ **腳本文案** 直接寫出可以唸的逐字稿
- 不知道要做什麼？→ **創意總監** 幫你判斷任務並分派工作

---

## 👥 團隊成員

| 角色 | Skill 名稱 | 核心職責 | 何時呼叫 |
|------|-----------|---------|---------|
| 🎬 創意總監 | `creative-director` | 任務分派、創意審核、流程統籌 | 不知道從哪開始、需要審核企劃方向 |
| 🔍 AI 研究員 | `ai-researcher` | AI 工具功能研究、競品比較、亮點整理 | 任何涉及 AI 工具的任務前期 |
| 📋 內容企劃 | `content-planner` | 主題發想、內容切角、影片架構規劃 | 確認研究資料後，進入企劃階段 |
| ✍️ 腳本文案 | `script-writer` | 逐字腳本、口播稿、業配融入語句 | 企劃確定後，進入撰稿階段 |
| 🎥 影音導演 | `video-director` | 分鏡表、錄屏清單、剪輯節奏規劃 | 腳本確定後，準備拍攝與剪輯 |
| 📨 Brief 解析 | `brief-analyst` | 業配需求解析、必講事項整理、風險提醒 | 收到業配邀請或合作 Brief 時 |
| 📱 社群經營 | `social-media` | 跨平台文案、內容日曆、發文策略 | 影片完成後的社群延伸 |
| 🎨 品牌視覺 | `brand-design` | 品牌識別系統、色彩字型、視覺規範 | 品牌層面的設計問題 |
| 🖼️ 行銷素材 | `marketing-materials` | 海報、Banner、社群圖文設計（整合 Canva） | 需要製作視覺素材 |
| 📅 專案經理 | `project-manager` | 任務拆解、時程規劃、交付清單管理 | 需要管理進度或整理任務 |

---

## 🔄 常見工作流程

### AI 工具業配影片（完整流程）

```
① brief-analyst    → 解析合作需求、整理必講事項、提醒風險
② ai-researcher    → 研究工具功能、獨特賣點、競品差異
③ content-planner  → 設計影片企劃、3-5 個主題切角方案
④ script-writer    → 撰寫逐字腳本（含業配段）、提供 2-3 個版本
⑤ video-director   → 規劃分鏡表、B-roll 清單、錄屏清單
⑥ social-media     → 撰寫各平台配套貼文、限動導流策略
⑦ project-manager  → 整理交付清單、建立拍攝時程
```

### 個人品牌短影音（輕量流程）

```
① content-planner  → 主題發想
② script-writer    → 撰寫腳本
③ video-director   → 分鏡規劃
④ social-media     → 跨平台發文套組
```

### 品牌視覺建立

```
① brand-design         → 建立識別系統（色彩、字型、Logo 概念）
② marketing-materials  → 設計行銷素材（整合 Canva MCP）
③ social-media         → 套用到各社群平台版型
```

---

## 🛠️ 環境需求

### 必要條件
- [Claude.ai](https://claude.ai) 帳號（建議 Pro 方案，取得更長上下文與更多功能）

### 建議整合（可選）
以下 MCP 連結可以讓對應 Skill 直接操作外部工具，讓工作流程更順暢：

| MCP 服務 | 連結後可做什麼 | 相關 Skill |
|---------|-------------|-----------|
| Gmail | 直接讀取業配邀請信件 | `brief-analyst` |
| Google Calendar | 自動建立拍攝日程與交件提醒 | `project-manager` |
| Notion | 建立任務資料庫、追蹤案件進度 | `project-manager` |
| Canva | 直接生成設計稿並匯出 | `marketing-materials`, `brand-design` |
| Figma | 讀取設計系統、取得設計 Token | `brand-design` |

> **沒有 MCP 也完全可以使用** — MCP 整合是加分項目，所有 Skill 在純文字輸出模式下同樣能完整運作。

---

## 📁 檔案結構

```
ai-design-team-skills/
├── README.md
├── SETUP.md
└── skills/
    ├── creative-director/
    │   └── SKILL.md
    ├── ai-researcher/
    │   └── SKILL.md
    ├── content-planner/
    │   └── SKILL.md
    ├── script-writer/
    │   └── SKILL.md
    ├── video-director/
    │   └── SKILL.md
    ├── brief-analyst/
    │   └── SKILL.md
    ├── social-media/
    │   └── SKILL.md
    ├── brand-design/
    │   └── SKILL.md
    ├── marketing-materials/
    │   └── SKILL.md
    └── project-manager/
        └── SKILL.md
```

---

## ⚙️ 如何使用

詳細安裝與設定步驟請見 **[SETUP.md](./SETUP.md)**。

快速入門：
1. Clone 這個 repo
2. 將 `skills/` 資料夾的內容上傳至你的 Claude.ai 自訂 Skill 設定
3. 開啟新對話，Claude 就會自動根據任務觸發對應角色
4. 若想指定角色，直接在對話中說明即可（例：「用 content-planner 幫我發想主題」）

---

## 🎯 設計原則

這套 Skill Pack 在設計時遵循以下原則：

- **角色分工明確**：每個 Skill 只做自己負責的事，不越界
- **上下游銜接**：每個角色的輸出格式，都是下一個角色需要的輸入格式
- **可直接執行**：所有輸出都是「可以直接用」的格式，不是模糊建議
- **台灣語境優先**：口語、文案、平台建議都針對台灣市場優化

---

## 🗒️ 客製化說明

以下內容是針對原始作者的個人情境所設定，若你 Fork 這個 Repo，建議根據自己的情況修改：

- **內容主軸**：`creative-director` 和 `content-planner` 中提到的「AI工具介紹」「業配合作影片」是原始作者的主要創作類型，可以修改為你的內容方向
- **語言風格**：`script-writer` 中的台灣口語風格與說話方式可根據個人特色調整
- **平台優先順序**：`social-media` 中的平台策略可根據你主要經營的平台調整

---

## 📄 授權

MIT License — 歡迎自由使用、修改與分享，請保留原始來源說明。

---

## 🙌 貢獻與回饋

如果你有改進建議，或者做了有用的客製化版本，歡迎開 Issue 或 PR。


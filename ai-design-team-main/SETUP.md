# ⚙️ SETUP.md — 安裝與設定指南

> 本文件說明如何將 AI 設計部門 Skill Pack 安裝到你的 Claude.ai，以及如何設定 MCP 整合來解鎖完整功能。

---

## 📋 安裝前確認

在開始之前，請確認你有：

- [ ] Claude.ai 帳號（免費方案可用，Pro 方案建議，功能更完整）
- [ ] 已 Clone 或下載這個 Repo
- [ ] （可選）準備好要連結的 MCP 服務帳號

---

## 🚀 Step 1：取得 Skill 檔案

### 方法 A：Clone Repo

```bash
git clone https://github.com/你的帳號/ai-design-team-skills.git
cd ai-design-team-skills
```

### 方法 B：直接下載 ZIP

在 GitHub 頁面點選 `Code → Download ZIP`，解壓縮後進入資料夾。

---

## 📤 Step 2：上傳 Skill 到 Claude.ai

目前 Claude.ai 透過 **Projects（專案）** 功能來管理自訂 Skill 和系統指令。

### 2-1 建立一個新專案

1. 前往 [claude.ai](https://claude.ai)
2. 在左側側欄點選 **「Projects」（專案）**
3. 點選 **「New Project」（建立新專案）**
4. 命名為：`AI 設計部門` 或你喜歡的名稱

### 2-2 上傳 Skill 檔案

1. 進入你剛建立的專案
2. 點選 **「Project Instructions」（專案指令）** 或 **「Add Content」**
3. 將 `skills/` 資料夾內所有的 `SKILL.md` 檔案內容加入專案
4. 建議一個 Skill 對應一個上傳區塊，方便後續管理

> **提示**：你可以把所有 10 個 SKILL.md 的內容合併成一個大型 System Prompt，或分開上傳。分開上傳的好處是可以單獨更新某個 Skill。

### 2-3 驗證安裝

在專案內開啟新對話，輸入：

```
我有一個業配邀請，幫我分析一下
```

如果 Claude 自動以 Brief 解析師的角色回應並要求提供 Brief 內容，代表安裝成功。

---

## 🔌 Step 3：設定 MCP 整合（可選但建議）

MCP（Model Context Protocol）讓 Claude 可以直接操作外部工具。以下是各 Skill 對應的 MCP 設定方式。

### 3-1 Gmail MCP（`brief-analyst` 使用）

**功能**：讓 Brief 解析師直接讀取你 Gmail 中的業配合作信件，不需要手動複製貼上。

**設定步驟**：
1. 前往 Claude.ai **Settings（設定）→ Integrations（整合）**
2. 找到 **Gmail** 並點選連結
3. 使用你的 Google 帳號授權
4. 授權完成後，在對話中說「幫我讀一下最近的業配邀請信」即可直接使用

**使用方式**：
```
幫我看一下 Gmail 裡最近的合作邀請信，有沒有業配案需要分析
```

---

### 3-2 Google Calendar MCP（`project-manager` 使用）

**功能**：讓專案經理直接在你的 Google 行事曆建立拍攝日程、交件提醒、上線日期。

**設定步驟**：
1. 前往 Claude.ai **Settings → Integrations**
2. 找到 **Google Calendar** 並點選連結
3. 使用你的 Google 帳號授權
4. 確認有賦予「建立活動」的權限

**使用方式**：
```
幫我排一下這個業配案的時程，上線日是 5/15，幫我在 Google Calendar 建立相關提醒
```

---

### 3-3 Notion MCP（`project-manager` 使用）

**功能**：讓專案經理在 Notion 建立案件追蹤資料庫，自動整理每個案件的狀態。

**設定步驟**：
1. 前往 Claude.ai **Settings → Integrations**
2. 找到 **Notion** 並點選連結
3. 選擇你想讓 Claude 存取的 Notion 工作區
4. 建議給予「讀取」和「建立頁面」的最低必要權限

**建議的 Notion 資料庫結構**（可直接複製）：

| 欄位名稱 | 類型 | 說明 |
|---------|------|------|
| 影片名稱 | 標題 | 案件名稱 |
| 類型 | 選項 | 業配 / 個人品牌 / 系列 |
| 狀態 | 選項 | 企劃中 / 製作中 / 送審中 / 上線 |
| 上線日期 | 日期 | 預定上線日 |
| 品牌名稱 | 文字 | 業配填入 |
| 合作費用 | 數字 | 業配填入 |
| 相關連結 | 連結 | Brief / 腳本 / 影片 |

**使用方式**：
```
幫我在 Notion 建立一個新的案件頁面，這是一個跟 OO 品牌的業配合作
```

---

### 3-4 Canva MCP（`marketing-materials`、`brand-design` 使用）

**功能**：讓行銷素材設計師直接在你的 Canva 帳號生成設計稿、調整尺寸、匯出圖片，省去描述後再手動製作的步驟。

**設定步驟**：
1. 前往 Claude.ai **Settings → Integrations**
2. 找到 **Canva** 並點選連結
3. 使用你的 Canva 帳號授權
4. 建議先在 Canva 設定好品牌色彩和 Logo（Brand Kit），讓設計稿自動套用品牌風格

**使用方式**：
```
幫我做一張 IG 貼文圖，主題是「5 個讓你省時的 AI 工具」，套用我的品牌色
```

---

### 3-5 Figma MCP（`brand-design` 使用）

**功能**：讓品牌視覺設計師讀取你現有的 Figma 設計系統，確保新設計符合既有規範。

**設定步驟**：
1. 前往 Claude.ai **Settings → Integrations**
2. 找到 **Figma** 並點選連結
3. 使用你的 Figma 帳號授權
4. 建議給予「讀取」權限即可

**使用方式**：
```
幫我讀取 Figma 裡的品牌設計系統，整理出目前的色彩和字型規範
```

---

## ✅ Step 4：驗證完整功能

安裝完成後，用以下測試指令確認各功能正常運作：

### 基本功能測試
```
我有一個任務不知道從哪裡開始，幫我規劃一下：
我想拍一支 AI 工具介紹影片，介紹 Notion AI，但也有業配需求。
```
> ✅ 預期：創意總監角色啟動，分析任務並給出角色分派建議

### MCP 功能測試（若已設定）
```
幫我搜尋一下 Gmail 裡最近有沒有業配合作信件
```
> ✅ 預期：Brief 解析師角色啟動，直接呼叫 Gmail 工具搜尋信件

---

## 🔧 常見問題

**Q：為什麼 Claude 沒有自動切換到對應的角色？**

A：確認你已在 Claude.ai 的**專案（Project）**中上傳了 Skill 檔案。在一般對話（非專案內）中，Skill 不會自動生效。也可以在對話中明確指定角色，例如：「請用 script-writer 的角色幫我寫腳本」。

---

**Q：可以只安裝部分 Skill 嗎？**

A：可以。10 個 Skill 各自獨立，你可以只上傳你需要的角色。不過建議至少安裝 `creative-director`，因為它是任務分派的入口，可以引導你找到需要的角色。

---

**Q：沒有 MCP 整合還能用嗎？**

A：完全可以。MCP 只是讓工作流程更自動化，所有 Skill 在純文字模式下都能完整運作。沒有 Gmail MCP 時，手動把業配信件貼上去給 `brief-analyst` 分析即可；沒有 Canva MCP 時，`marketing-materials` 會輸出詳細的設計描述，你再手動在 Canva 製作。

---

**Q：如何更新 Skill？**

A：直接在 Claude.ai 專案中替換對應的 Skill 內容即可。也可以持續關注這個 Repo 的更新，有新版本時 Pull 並重新上傳。

---

**Q：可以同時使用多個角色嗎？**

A：可以在同一個對話中切換角色。建議的做法是：先讓創意總監分析任務，再依序呼叫各個角色。也可以明確告訴 Claude「現在切換到 content-planner」來指定角色。

---

**Q：這套 Skill 的語言設定是？**

A：所有 Skill 預設使用繁體中文，針對台灣市場語境設計（口語、節慶、平台習慣等）。如果你需要英文或其他語言版本，可以 Fork 後自行修改 Skill 內容。

---

## 📬 需要協助？

如果在安裝過程中遇到問題，歡迎在 GitHub 開 Issue，說明你的操作步驟和遇到的狀況。

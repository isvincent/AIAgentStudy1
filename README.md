# 從 AI 對話到 AI 做事｜高中教師 AI Agent 互動研習

這是一套可直接上課、投影展示，並可部署到 **GitHub Pages** 的單頁式繁體中文教材網站。適用於高中教師、圖書館與學校行政職員的 AI Agent 研習。

## 功能

- 30 個 AI Agent 校園應用案例：六大類別、即時搜尋、難度篩選、詳細任務視窗。
- 8 個大型進階實作專題。
- 6 階段 AI Agent 工作流程與 Codex、Antigravity、Claude Code 教學比較。
- 2、3、6 小時研習課程規劃器，並可下載文字版課表。
- 三種可直接複製的 Agent 提示詞範本。
- 5 項校園 Agent Skills 建議。
- 學員學習檢核表、即時進度及文字紀錄下載。
- RWD 響應式版面、字體調整、深色模式及投影模式。
- 不需後端、不需 API Key、不使用外部 CDN，離線開啟也能運作。

## 專案結構

```text
ai-agent-teacher-workshop/
├── index.html      # 完整首頁：HTML + CSS + JavaScript
└── README.md       # 安裝、部署、修改與教學指引
```

## 本機開啟

直接雙擊 `index.html`，用 Chrome、Edge、Firefox 等現代瀏覽器開啟即可。搜尋、篩選、互動視窗、課表下載等不需連網。剪貼簿功能在某些瀏覽器的 `file://` 環境可能受限制，推薦在 GitHub Pages 的 HTTPS 網站操作。

也可以在此專案資料夾中執行：

```bash
python -m http.server 8000
```

然後瀏覽 `http://localhost:8000`。

## 上傳 GitHub 與啟用 GitHub Pages

### 方法一：直接使用 GitHub 網站

1. 登入 GitHub，建立一個公開儲存庫，例如 `ai-agent-teacher-workshop`。
2. 選取 **Add file → Upload files**，將 `index.html` 與 `README.md` 放到儲存庫根目錄並提交。
3. 進入儲存庫的 **Settings → Pages**。
4. 在 **Build and deployment** 的來源選擇 **Deploy from a branch**。
5. 選擇 `main` 分支與 `/ (root)`，按下 **Save**。
6. 部署完成後，網址通常是 `https://<你的GitHub帳號>.github.io/ai-agent-teacher-workshop/`。

> GitHub Pages 的設定位置與介面可能因帳號或儲存庫選項有所差異。實際網址以 Pages 顯示結果為準。

### 方法二：使用 Git 指令

```bash
git init
git add index.html README.md
git commit -m "Initial AI Agent workshop site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ai-agent-teacher-workshop.git
git push -u origin main
```

先在 GitHub 建立空的遠端儲存庫，並把 `YOUR_USERNAME` 換成你的 GitHub 帳號。接著按照方法一啟用 Pages。

## 修改教材

網站所有 CSS 與 JavaScript 都寫在 `index.html`，方便研習現場直接展示與修改。

- 30 個案例：尋找 `const raw = [`，每筆資料包含「分類、標題、描述、難度」。
- 8 個專題：尋找 `const projects = [`。
- 課程時數：尋找 `const schedules =`，分別編輯 `120`、`180`、`360`。
- 提示詞：尋找 `const prompts =`，可修改 `teaching`、`meeting`、`website`。
- Skills：尋找 `const skills = [`。
- 檢核項目：尋找 `const checklist = [`。
- 配色：修改 CSS `:root` 中的變數。

修改後儲存，重新整理網頁即可。更新 GitHub 儲存庫後 Pages 會重新部署。

## 教師授課建議

1. 先使用首頁說明「AI 對話」與「AI Agent 做事」的差異。
2. 透過 30 個案例搜尋、篩選與開啟任務視窗，讓學員選擇專題。
3. 用「工作流」介紹規劃、檔案讀取、工具執行、跨系統整合、驗證及交付。
4. 切換 2／3／6 小時課表，介紹研習安排。
5. 在提示詞區複製範本，貼到 Codex、Antigravity 或 Claude Code 實作。
6. 最後使用檢核表記錄學員成果並下載。

## 存取、安全與限制

- **本頁不是 AI Agent 執行引擎**：網站只展示教學內容與互動教材，**不會自行呼叫 Codex、Antigravity、Claude Code**，也不會存取電腦中的教材。
- 不會把檢核資料傳送到任何伺服器；檢核勾選儲存在同一瀏覽器的 `localStorage`，可能因清除瀏覽資料或私密模式而遺失。
- 課表及檢核結果下載為 UTF-8 文字檔。
- 正式應用於學生資料、成績、輔導紀錄或校內機敏資料前，需符合學校政策、相關法規及服務權限。
- 網站擷取須尊重網站使用條款、存取控制與著作權；不要繞過驗證或擷取未授權資料。
- 發信、資料覆寫、刪除與公開部署等具外部影響的操作，應保留人工核准。
- 範本產物須由教師或行政承辦人複核，不應直接視為權威答案。

## 授權說明

本專案作為教學展示範本提供，可自行修改與使用。上傳至公開儲存庫前，請確認新增素材、照片、內容與第三方字型的使用權限。

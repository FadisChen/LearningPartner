# iPAS AI 應用規劃師 - 智慧學習中心 Learning Hub

這是一個專為「iPAS AI 應用規劃師」考照準備的互動式學習平台。整合了知識架構圖 (Mind Map) 與 Google Gemini AI，讓您可以像使用 AI 家教一樣，針對官方學習指引進行問答與重點解析。

## ✨ 主要功能

- **🚀 知識地圖可視化**：
  - 完整收錄三個科目的考試重點。
  - 使用 Markmap 技術呈現動態心智圖。
  - **點擊互動**：點擊節點即可叫出 AI 選單（解釋概念、產生考題）。

- **🤖 AI 智能家教 (Gemini)**：
  - **自帶 Key (BYOK)**：使用您個人的 Google Gemini API Key，確保隱私與控制權。
  - **文件對話 (RAG-like)**：直接上傳官方 PDF 學習指引，AI 會基於文件內容回答問題，避免胡說八道。
  - **流式輸出**：回應即時顯示，無需漫長等待。
  - **圖文整合**：在對話中支援 Markdown 格式渲染。

- **⚙️ 高度客製化**：
  - **模型選擇**：預設使用 `gemini-2.5-flash`，亦可切換至 `gemini-1.5-pro` 或自訂其他模型 ID。
  - **繁體中文介面**：全在地化設計，親切易用。

## 🛠️ 使用方式

1. **啟動應用**：
   直接使用瀏覽器（推薦 Chrome 或 Edge）開啟 `LearningHub.html` 檔案。

2. **設定 API Key**：
   - 首次使用請點擊左上角的輸入框。
   - 貼上您的 [Google Gemini API Key](https://aistudio.google.com/app/apikey)。
   - 點擊儲存（Key 僅儲存於您的瀏覽器 LocalStorage，不會上傳至任何第三方伺服器）。

3. **開始學習**：
   - **選擇科目**：點擊左側 1, 2, 3 按鈕切換科目。
   - **上傳指引**：點擊左側虛線框，選擇對應科目的 PDF 檔案（每次重新整理頁面需重新選擇）。
   - **互動**：
     - 在地圖上點擊節點 -> 選擇「💡 解釋」或「❓ 出題」。
     - 切換到「AI 導師」分頁 -> 自由提問。

## 📁 檔案結構

```
.
├── LearningHub.html          # 主程式 (單一檔案，包含 HTML/JS/CSS)
├── 學習指引/                 # 官方 PDF 資料夾
│   ├── ...科目1.pdf
│   ├── ...科目2.pdf
│   └── ...科目3.pdf
└── 知識圖譜/                 # (已整合至 LearningHub，此資料夾為備份原始檔)
```

## ⚠️ 注意事項

- 本工具為純前端應用 (Client-Side App)，不會儲存您的對話紀錄至伺服器。
- PDF 解析使用瀏覽器內建 API 轉換為 Base64 傳送給 Gemini，請留意 API 使用量限制。
- 若遇到 API Error，通常是 API Key 無效或配額已滿。

---
*Created by Antigravity Agent*

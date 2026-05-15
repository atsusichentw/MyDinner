# 🍲 晚餐吃什麼？—— 雲端雙向同步抽籤器

這是一個專為「晚餐選擇困難症」設計的輕量化網頁工具。不僅能幫你從自定義菜單中隨機抽籤，還具備 **14 天不重複機制**，並能將資料即時同步至你的 **Google Sheets**，讓你在不同裝置間無縫切換！

![Version](https://img.shields.io/badge/Version-2.0-red)
![License](https://img.shields.io/badge/License-MIT-green)
![Platform](https://img.shields.io/badge/Platform-Web-blue)

---

## ✨ 功能亮點

- 🎲 **隨機抽籤**：一鍵決定今晚吃什麼，告別猶豫不決。
- 🚫 **14 天排除機制**：自動記住最近 14 天吃過的菜色，抽籤時自動過濾，確保飲食多樣化。
- ☁️ **Google Sheets 同步**：登入 Google 帳號後，自動在雲端硬碟建立 `Dinner_History_Sync` 試算表，實現雙向資料同步。
- 📱 **響應式設計**：基於 Bootstrap 5 構建，手機、平板、電腦都能完美操作。
- 🛠️ **自訂菜單**：隨時新增、刪除你的私藏菜單，或一鍵還原預設的 31 樣經典菜色。

---

## 🚀 快速開始

### 1. 取得程式碼
下載 `index.html` 檔案至你的電腦。

### 2. 配置 Google Cloud 憑證 (重要)
為了使用雲端同步功能，你需要申請自己的 API Key：
1. 前往 [Google Cloud Console](https://console.cloud.google.com/)。
2. 建立新專案，並啟用 **Google Sheets API** 與 **Google Drive API**。
3. 在「憑證」頁面：
   - 建立 **API 金鑰 (API Key)**。
   - 建立 **OAuth 2.0 用戶端 ID** (應用程式類型選擇「網頁應用程式」)。
4. 將你的網址（如 `https://yourname.github.io`）加入「授權的 JavaScript 來源」。
5. 打開 `dinner.html`，將 `CLIENT_ID` 與 `API_KEY` 填入程式碼開頭的變數中。

### 3. 部署
將檔案上傳至 GitHub Pages、Firebase Hosting，或直接用瀏覽器開啟即可使用。

---

## 🛠️ 技術棧
- **Frontend**: HTML5, JavaScript (ES6+), Bootstrap 5
- **Icons**: Bootstrap Icons
- **Backend**: Google Identity Services (GIS), Google API Client (GAPI)
- **Storage**: LocalStorage & Google Sheets API v4

---

## 📸 介面預覽
- **頂部狀態欄**：即時顯示雲端連線狀態與使用者頭像。
- **抽籤面板**：超大字體顯示結果，伴隨動態滾動效果。
- **管理清單**：清晰列出所有菜色，排除中的項目會自動劃線標記。

---

## 💡 使用小技巧
- **資料不及時？**：請確保頂部顯示「雲端同步已就緒」綠色標籤再開始抽籤。
- **想重頭開始？**：點擊「清除歷史」即可解除 14 天的排除限制。
- **換手機了？**：在新手機登入同一個 Google 帳號，程式會自動從試算表抓回你的吃飯紀錄！

---

## 📄 授權協議
本專案採用 MIT 授權協議。您可以自由修改、分發及使用。

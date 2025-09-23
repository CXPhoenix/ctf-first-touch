# CTF 第一次接觸 - 資安教學簡報

[![Slidev](https://img.shields.io/badge/Slidev-v52.1.0-blue?style=flat-square&logo=vue.js)](https://sli.dev)
[![Vue 3](https://img.shields.io/badge/Vue-3.5.18-4FC08D?style=flat-square&logo=vue.js)](https://vuejs.org)
[![Slidev Theme - FHSH AiSP Theme](https://img.shields.io/npm/v/%40cxphoenix%2Fslidev-theme-fhsh-aisp?style=flat-square&logo=npm&label=%40cxphoenix%2Fslidev-theme-fhsh-aisp)](https://www.npmjs.com/package/@cxphoenix/slidev-theme-fhsh-aisp)
[![TLDraw Addon](https://img.shields.io/npm/v/slidev-addon-tldraw?style=flat-square&logo=npm&label=slidev-addon-tldraw)](https://www.npmjs.com/package/slidev-addon-tldraw)
[![CC BY 4.0](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)

> 專為資訊安全初學者設計的 CTF 入門教學簡報，使用 Slidev 框架建置，涵蓋資安基礎概念、CTF 競賽介紹與實戰練習

## 📋 目錄

- [簡報簡介](#簡報簡介)
- [教學內容](#教學內容)
- [技術架構](#技術架構)
- [快速開始](#快速開始)
- [專案結構](#專案結構)
- [部署方式](#部署方式)
- [自訂元件](#自訂元件)
- [開發功能](#開發功能)
- [授權條款](#授權條款)

## 📖 簡報簡介

這是一份關於「**CTF 第一次接觸**」的資訊安全教學簡報，由 **@CXPh03n1x** 製作。簡報旨在幫助初學者了解資訊安全領域的基礎知識，並透過 CTF（Capture The Flag）競賽和 Wargame 實戰來學習資安技能。

### 教學目標

- 🎯 **資安入門**：介紹資訊安全核心概念與專業術語
- 🏁 **CTF 啟蒙**：了解 CTF 競賽模式與訓練方式
- ⚡ **實戰練習**：透過 Natas Wargame 平台進行實作
- 📝 **筆記習慣**：培養撰寫 Writeup 的技術文件能力

## 📚 教學內容

### 第一章：基礎知識
- **資安三本柱（C.I.A）**：機密性、完整性、可用性
- **風險評估概念**：風險、弱點、漏洞的區別
- **駭客文化**：駭客精神與道德準則
- **資安專業術語**：OWASP、CVE、CWE、ATT&CK 等

### 第二章：訓練模式
- **CTF 競賽類型**：
  - Jeopardy（解題模式）
  - Attack & Defense（攻防模式）
  - King of Hill（占地模式）
- **Wargame 訓練**：傳統闖關式學習

### 第三章：實戰練習
- **Natas 平台介紹**：OverTheWire 經典 Web 安全挑戰
- **實作練習**：從 Natas 0 開始的 Web 安全實戰
- **Writeup 撰寫**：技術文件記錄與分享

## 🛠️ 技術架構

- **簡報框架**：[Slidev](https://sli.dev) v52.1.0
- **前端框架**：[Vue.js](https://vuejs.org) v3.5.18
- **主題樣式**：[@cxphoenix/slidev-theme-fhsh-aisp](https://www.npmjs.com/package/@cxphoenix/slidev-theme-fhsh-aisp) v1.2.0
- **互動擴充**：[slidev-addon-tldraw](https://www.npmjs.com/package/slidev-addon-tldraw) v0.4.2
- **字型支援**：繁體中文（edukai, Noto Sans Traditional Chinese）
- **部署平台**：Netlify / Vercel

## 🚀 快速開始

### 1. 複製專案

```bash
git clone <repository-url>
cd ctf-first-touch
```

### 2. 安裝相依套件

```bash
# 推薦使用 pnpm
pnpm install

# 或使用 npm
npm install
```

### 3. 啟動開發伺服器

```bash
pnpm dev
# 或
npm run dev
```

開啟瀏覽器前往 http://localhost:3030 即可預覽簡報。

### 4. 建置靜態檔案

```bash
pnpm build
# 或
npm run build
```

## 📁 專案結構

```
├── slides.md              # 簡報主要內容檔案
├── package.json           # 專案配置與相依性
├── components/            # 自訂 Vue 元件
│   ├── CenterFlexBlock.vue    # 置中彈性容器元件
│   ├── CustomToc.vue          # 自訂目錄元件
│   └── GridBlock.vue          # 格線佈局元件
├── public/                # 靜態資源目錄
│   ├── fonts/                 # 字型檔案
│   ├── natas.png             # Natas 平台截圖
│   └── level_2.png           # Level 2 示範圖片
├── pages/                 # 額外頁面（如果有）
├── snippets/             # 程式碼片段（如果有）
├── styles/               # 樣式檔案
├── netlify.toml          # Netlify 部署配置
└── vercel.json           # Vercel 部署配置
```

## 🌐 部署方式

### GitHub Pages

透過 GitHub Actions 自動部署：

1. 在 repository 的 Settings > Pages
2. 選擇 "GitHub Actions" 作為 source
3. 推送程式碼後自動部署

### Netlify 部署

1. 連接你的 GitHub repository
2. 專案會自動讀取 `netlify.toml` 配置檔案
3. 建置命令：`npm run build`
4. 發布目錄：`dist`

### Vercel 部署

1. 匯入 GitHub repository
2. 專案會自動讀取 `vercel.json` 配置檔案
3. 支援自動 CI/CD

## 🧩 自訂元件

### CenterFlexBlock
置中彈性佈局容器，用於內容居中顯示。

### CustomToc
自訂目錄元件，自動生成簡報章節導覽。

```markdown
<CustomToc />
```

### GridBlock
格線佈局元件，用於整齊排列多個內容區塊。

## 💻 開發功能

### 即時預覽

開發模式下支援即時預覽，修改 `slides.md` 後瀏覽器會自動重新載入。

```bash
pnpm dev --open  # 自動開啟瀏覽器
```

### 簡報者模式

在瀏覽器中按 `?` 鍵檢視所有快捷鍵：

- `f`：全螢幕模式
- `o`：總覽模式
- `d`：深色模式切換
- `g`：跳轉到指定頁面

### 匯出功能

```bash
# 匯出為 PDF
pnpm export

# 匯出為 PNG (每頁一張)
pnpm export --format png

# 匯出為 PPTX
pnpm export --format pptx
```

### TLDraw 整合

支援 TLDraw 手繪工具，可在簡報中進行即時繪製和標註。

## 🎓 使用建議

### 教學者
- 建議在實際教學前先熟悉簡報內容與操作
- 可根據學員程度調整 Natas 練習的進度
- 鼓勵學員做筆記並分享 Writeup

### 學習者
- 跟隨簡報進度逐步學習資安概念
- 實際操作 Natas 平台練習
- 養成記錄學習過程的習慣

## 🔧 故障排除

### 常見問題

**Q: 開發伺服器無法啟動**
- 確保 Node.js 版本 ≥ 18.0
- 檢查 3030 port 是否被佔用
- 嘗試清除 node_modules 後重新安裝

**Q: 字型顯示異常**
- 檢查字型檔案是否正確載入
- 確認字型路徑設定正確

**Q: 部署後圖片無法顯示**
- 確認圖片檔案在 public 目錄中
- 檢查圖片路徑是否正確

### 系統需求

- **Node.js**: ≥ 18.0
- **套件管理工具**: npm、pnpm、或 yarn
- **瀏覽器**: 支援現代 Web 標準的瀏覽器

## 📚 參考資源

### 資安學習平台
- [OverTheWire - Natas](https://overthewire.org/wargames/natas/)
- [OWASP 專案](https://owasp.org/)
- [CVE 漏洞資料庫](https://www.cve.org/)
- [MITRE ATT&CK 框架](https://attack.mitre.org/)

### 技術文件
- [Slidev 官方文件](https://sli.dev/guide/)
- [Vue.js 官方教學](https://vuejs.org/tutorial/)
- [FHSH AiSP 主題文件](https://www.npmjs.com/package/@cxphoenix/slidev-theme-fhsh-aisp)

### CTF 相關資源
- [CTF 入門指南](https://ctf101.org/)
- [Phrack 電子雜誌](https://phrack.org/)

---

## 📄 授權條款

本專案採用 CC BY 4.0 授權條款，詳見 [LICENSE](./LICENSE) 檔案。

---

**🎯 讓我們一起透過 CTF 踏入資訊安全的世界！**
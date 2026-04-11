# TEAM SPACE - 團隊協作網站

## 網站結構

```
team-space/
├── login.html      # 登入頁面（入口）
├── index.html      # 主頁面（公告、檔案、相簿）
└── README.md       # 說明文件
```

## 功能說明

### 🔐 登入系統
- **入口頁面**: `login.html`
- **密碼**: `tribunal`
- **記住密碼**: 可選，記住 30 天

### 📱 主頁面功能
1. **Announcements (公告)** - 水平滑動卡片
2. **Files (檔案下載)** - 檔案列表配下載按鈕
3. **Gallery (相簿)** - Masonry 瀑布流佈局

### 🔒 安全機制
- 未登入會自動跳轉到登入頁
- 已登入用戶直接進入主頁
- 勾選「記住密碼」可保持 30 天登入狀態
- 未勾選則 1 小時後需重新登入
- 底部導航欄最右邊按鈕可登出

## 使用方式

### 本地預覽
```bash
cd team-space
python3 -m http.server 8080
# 開啟 http://localhost:8080/login.html
```

### 部署到 GitHub Pages
1. 建立 GitHub Repository
2. 上傳 `team-space` 資料夾內容
3. 啟用 GitHub Pages（設定為 main branch / root）
4. 訪問 `https://yourusername.github.io/repo-name/login.html`

## 設計規格

- **風格**: iOS 簡約風格
- **配色**: 米白背景 #FAFAF8，柔和陰影
- **字體**: SF Pro Display / 系統默認字體
- **圓角**: 12-20px
- **動畫**: Fade in, hover 浮起效果

## 注意事項

- 密碼驗證使用前端 JavaScript (localStorage)
- 不適用於高安全性要求的場景
- 建議在 HTTPS 環境下使用

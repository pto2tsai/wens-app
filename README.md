# 生產作業管理 App 外殼（WENS PRODUCTION OPS）

手機「加入主畫面」用的外殼網頁，放在公開的 GitHub repo `pto2tsai/wens-app`，用 GitHub Pages 發布：

- 網址：`https://pto2tsai.github.io/wens-app/`
- 內容只有：入口頁（`index.html`）、App 名稱與圖示（`manifest.webmanifest`、`icon-*.png`、`apple-touch-icon.png`）
- **沒有任何程式邏輯、資料或密碼**，打開後把 Apps Script 的首頁包在裡面

原始檔放在 `weightchecker` repo 的 `app-shell/`，改完複製到 `wens-app` repo。

## 要改的地方

- `index.html` 的 `APP_URL`：Apps Script 部署網址（結尾 `/exec`）
- 圖示：由 `weightchecker/assets/logo/mark-512.png` 產生

## 限制

- 別的 Apps Script 專案（MES）不允許被包起來，所以從 App 裡點 MES 會另開視窗
- 從 App 打開和從瀏覽器打開，手機裡暫存的資料（例如還沒送出的一批）是分開的；請固定用同一種方式打開

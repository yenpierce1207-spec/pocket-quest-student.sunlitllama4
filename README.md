# 存錢勇者 Pocket Quest

以「每天養成角色、每週挑戰怪獸」為核心的學生財務遊戲網頁原型。使用 HTML、CSS 與 JavaScript，可直接部署到 GitHub Pages，無須安裝套件或建置。

## 上傳與公開網站

1. 解壓縮 `pocket-quest-github.zip`。
2. 在 GitHub 建立一個 **Public** repository，例如 `pocket-quest`。
3. 選擇 **Add file → Upload files**（全新儲存庫可點選 **uploading an existing file**）。
4. 上傳解壓縮後的所有檔案，再按 **Commit changes**。請讓 `index.html` 直接位於儲存庫最外層，不要只上傳 ZIP，也不要多包一層資料夾。
5. 開啟儲存庫的 **Settings → Pages**。
6. 在 **Build and deployment** 設定 **Source: Deploy from a branch**，選擇 **main** 與 **/(root)**，按 **Save**。若預設分支不是 main，請選擇實際上傳的分支。
7. 等候部署完成，使用 Pages 顯示的 **Visit site** 連結開啟網站。

一般專案網站網址格式為 `https://你的帳號.github.io/pocket-quest/`。請以 GitHub Pages 顯示的實際網址為準。部署為公開網站後，訪客不需登入 GitHub 即可使用。

官方操作說明：[設定 GitHub Pages 發布來源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

> `.nojekyll` 是空白設定檔，用於讓 GitHub Pages 直接提供靜態檔案。若檔案選擇器未顯示點號開頭的檔案，可開啟隱藏檔案顯示，或在 GitHub 使用 Add file → Create new file 建立 `.nojekyll`。

## 檔案結構

```text
index.html      網頁入口與畫面結構
style.css       配色、角色造型、動畫及響應式排版
app.js          記帳、任務、戰鬥、儲蓄與本機存檔
.nojekyll       GitHub Pages 靜態網站設定
.gitignore      排除本機開發與暫存資料
README.md       專案與部署說明
```

## 功能

- 記錄消費、選擇分類、標記必要支出、刪除誤登項目。
- 查看今日支出與本週剩餘預算。
- 完成每日記帳與每週回顧，領取一次性任務獎勵。
- 消耗能量攻擊怪獸，通關獲得金幣、經驗與徽章。
- 接受並完成訂閱整理任務。
- 設定儲蓄金額與日期、登記儲蓄、解鎖進度里程碑。
- 上週預算結算與補登後的獎勵調整。

## 展示順序

1. 點選「記一筆消費」，輸入一筆示範消費並儲存。
2. 在每日任務領取能量與經驗。
3. 點選「發動攻擊」，觀察怪獸血量下降。
4. 完成本週回顧，領取更多能量並挑戰通關。
5. 進入「儲蓄冒險」，記錄儲蓄並查看目標進度。

## 原型範圍

- 資料儲存在瀏覽器的 localStorage，沒有後端資料庫，也不會跨裝置同步。
- 原始碼內只有示範資料；使用者在舊網站輸入的紀錄不包含在這份專案中。
- 不同網址的瀏覽器存檔互不共用，因此 GitHub Pages 版會從示範資料開始。
- 任務教練使用固定規則，尚未串接 AI、電子發票或銀行。
- 儲蓄進度由使用者自行確認，未驗證實際存款。
- 金幣與徽章是遊戲展示獎勵，沒有購買或兌現功能。
- 字體使用 Google Fonts；無法載入時會使用系統替代字體。

## QR Code

先前的 QR Code 指向原本的 Sites 網站，不會自動改成 GitHub Pages 網址。完成部署後，請用 Pages 顯示的新網址重新製作 QR Code。

## 本機開發

可使用任意靜態 HTTP 伺服器在此資料夾預覽。例如已安裝 Python 時執行：

```sh
python -m http.server 4173 --bind 127.0.0.1
```

再開啟 `http://127.0.0.1:4173`。停止伺服器可按 Ctrl+C。正式分享請使用 GitHub Pages 的 HTTPS 網址。

## 更新網站

修改對應的 HTML、CSS 或 JavaScript 檔案後，上傳並提交到已選定的發布分支，GitHub Pages 會重新部署。

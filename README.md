# KK 音標互動學習

靜態網站，含三層頁面、41 個音標的音檔、口型與舌位圖片，以及練習短句和繁體中文翻譯。沒有外部套件或建置步驟。

網站檔案在 `docs/`。GitHub Pages 從這個資料夾發布後，網址是：

https://etbase.github.io/kk-phonetic-learning/

## 放到 GitHub 並開啟網站

1. 在這個資料夾提交並推上 `main`。
2. 打開倉庫的 Settings → Pages。
3. Build and deployment 的 Source 選 **Deploy from a branch**。
4. Branch 選 `main`，資料夾選 **`/docs`**，然後 Save。
5. 等一兩分鐘，上面的網址就可以開啟。

`docs/.nojekyll` 讓 Pages 直接提供圖片和音檔，不會用 Jekyll 再處理一次。

## 在本機預覽

安裝 Node.js 後，在專案根目錄執行：

```bash
npm run dev
```

再開啟 http://localhost:8000。不需執行 `npm install`。

也可以直接開啟 `docs/index.html`。請保留 `docs` 內的資料夾結構。單音音檔與圖片隨專案附上；例字和短句的朗讀使用瀏覽器或作業系統的美式英語語音，音色會因裝置而異。

## 主要檔案

- `docs/index.html`：網頁入口與載入順序。
- `docs/styles.css`：版面與樣式。
- `docs/app.js`：三層頁面、播放和互動邏輯。
- `docs/data.js`、`docs/word-kk.js`、`docs/phrases-v2.js`、`docs/translations.js`：音標、例字、練習短句與中文翻譯。
- `docs/assets/`：圖片和音檔。
- `docs/side-manifest.js`：本機直接開啟時也能顯示側面圖；`side-manifest.json` 是原始對照表。

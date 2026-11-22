# 賀昭恩 建築作品集 App

這個資料夾是一個完整的「可安裝網頁 App」（PWA）。放上 GitHub Pages（免費）之後：

- 任何人都可以用網址瀏覽你的作品集
- 手機可以「加入主畫面」，有自己的「昭」字圖示，開啟時是全螢幕，像一般 App
- 看過一次之後，沒有網路也能打開
- 你更新內容後，網站和已安裝的 App 會自動更新

## 資料夾內容

| 檔案 | 用途 |
|---|---|
| `index.html` | App 本體（版面與功能） |
| `content.json` | **所有文字內容、配色、作品清單**，平常更新只需要改這個檔 |
| `images/` | 所有圖片 |
| `icons/` | App 圖示 |
| `manifest.webmanifest`、`sw.js` | 讓網頁可以安裝成 App、離線使用 |

---

## 一、第一次上線（約 10 分鐘）

1. 到 <https://github.com> 註冊或登入帳號。
2. 右上角「＋」→ **New repository**。名稱輸入 `portfolio`，選 **Public**，按 **Create repository**。
3. 在新專案頁面點 **uploading an existing file**（或 Add file → Upload files）。
4. 把這個資料夾**裡面的所有東西**（index.html、content.json、images、icons 等，不是外層資料夾本身）一起拖進去，等上傳完成，按 **Commit changes**。
5. 到專案的 **Settings → Pages**：
   - Source 選 **Deploy from a branch**
   - Branch 選 **main**、資料夾選 **/ (root)**，按 **Save**
6. 等 1–2 分鐘，重新整理 Pages 頁面，會出現網址：
   `https://你的帳號.github.io/portfolio/`

## 二、安裝到手機

- **iPhone**：用 Safari 打開網址 → 下方「分享」按鈕 → **加入主畫面**
- **Android**：用 Chrome 打開網址 → 右上角選單 → **安裝應用程式**（或「加到主畫面」）

## 三、之後怎麼更新

### 方法 A：請 Claude 幫你改（最省事）
到 claude.ai 的 **設定 → Connectors** 連結你的 GitHub 帳號。之後直接告訴 Claude 要改什麼（例如「新增一個作品」「換掉 Trans-city 的縮圖」），Claude 會直接更新你的 GitHub 專案，網站與 App 約 1 分鐘後自動更新。

### 方法 B：用網站內建的編輯模式（自己改，按一下就發布）
1. 打開 `https://chaoenho-hub.github.io/portfolio/#admin`（網址最後加上 `#admin`）。
2. **第一次使用**：按「GitHub 設定」，照畫面說明到 GitHub 產生一組存取金鑰（只開放 `portfolio` 專案、Contents 設為 Read and write），貼上後儲存。金鑰只存在這台裝置的瀏覽器，換裝置要再設定一次。
3. 用 **新增專案、編輯簡介、橫幅與配色**，或點進作品按 **編輯** 修改內容與圖片。
4. 按 **發布到 GitHub**。文字與新圖片會一次上傳，約 1–2 分鐘後網站與 App 自動更新。

> 發布之前，修改只存在你這台裝置的瀏覽器裡，別人看不到；新加的圖片請在關閉頁面前發布。
> 其他人就算打開 `#admin`，沒有你的金鑰也無法改動網站。
> 不想用金鑰的話，也可以按「匯出 content.json」，再手動上傳到 GitHub 取代舊檔（新圖片放進 `images` 資料夾）。

### 方法 C：直接改 content.json
在 GitHub 專案點 `content.json` → 右上鉛筆圖示，直接修改文字後按 **Commit changes**。

---

## 圖片建議

- 作品內頁圖板：寬 2000–2500 px 的 JPG
- 作品縮圖：約 800 × 800 px 的正方形 JPG
- 目前的圖片來自 Weebly 匯出的 Word 檔，解析度偏低；有原始高解析度檔時建議替換（檔名相同直接覆蓋即可，不用改 content.json）。

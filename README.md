# MayIdea
html mvp
下面教你用 **GitHub 直接部署靜態 HTML/CSS/JS 網站**（最常用、最簡單的是 **GitHub Pages**）。我用「一步一步」帶你做，照做就會上線。

---

## 方法 1：GitHub Pages（推薦，免費、最簡單）

### 1) 準備你的專案資料夾

確保裡面至少有：

* `index.html`（首頁一定要叫這個，大小寫要正確）
* 其他像 `css/`, `js/`, `images/` 等

> 小提醒：連結路徑建議用相對路徑，例如 `./css/style.css`、`./images/logo.png`

---

### 2) 建立 GitHub Repo 並上傳檔案

1. 到 GitHub → New repository
2. Repo 名稱隨便取，例如 `my-site`
3. 建立後進 Repo，按 **Add file → Upload files**
4. 把你的整包網站檔案拖進去（含 `index.html`）
5. 按 **Commit changes**

---

### 3) 開啟 GitHub Pages

1. 進入 Repo → **Settings**
2. 左側選單 → **Pages**
3. **Build and deployment**

   * Source 選 **Deploy from a branch**
   * Branch 選 `main`（或 `master`）
   * Folder 選 `/ (root)`（通常選這個）
4. 按 **Save**

---

### 4) 取得你的網站網址

同一頁（Pages）會出現網址，通常像：

* `https://你的帳號.github.io/my-site/`

第一次可能要等一下下（通常 1~3 分鐘）才會生效。

---

## 方法 2：用專屬網域形式（repo 必須叫 `你的帳號.github.io`）

如果你希望網址是：

* `https://你的帳號.github.io/`（不帶 repo 名）

做法：

1. 建立 Repo 名稱 **一定要**叫：`你的帳號.github.io`
2. 上傳 `index.html` 到根目錄
3. Settings → Pages → root → main
   完成後就是乾淨網域。

---

## 常見踩雷與修正

### A) 打開後 404

* 檢查 Pages 設定的 Branch / Folder 是否正確
* 確認 repo 內真的有 `index.html`，而且在你選的資料夾（root 或 docs）裡

### B) CSS/圖片不見

* 你的路徑可能寫成 `/css/style.css`（開頭 `/` 會以網域根目錄解釋，常出錯）
* 改成 `./css/style.css` 或 `css/style.css`

### C) SPA（React/Vue）刷新就 404

* 需要額外處理 404 重導（或改用 Actions / 設定 base path）
* 你如果是純 HTML 網站通常不會遇到

---

## 你如果要「從 GitHub 存放庫直接佈署」最推薦的流程（最短版）

1. 建 repo → 上傳網站檔案（有 `index.html`）
2. Settings → Pages → main + root
3. 打開 `https://帳號.github.io/repo名/`

---

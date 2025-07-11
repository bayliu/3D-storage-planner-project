# 📦 3D 倉儲空間規劃工具 (3D Storage Planner)

這是一個互動式的 3D 網頁應用程式，旨在幫助使用者視覺化地規劃倉儲空間。使用者可以選擇不同尺寸的倉庫，新增常見物品（如箱子、家具），並在 3D 場景中自由拖曳、旋轉和堆疊這些物品。應用程式會即時計算空間使用率，幫助使用者做出最佳的租賃決策。

這個專案是使用 **React** 和 **Three.js** (透過 `@react-three/fiber`) 構建的，並使用 `@react-three/rapier` 實現了物理效果。

[![預覽圖片](https://storage.googleapis.com/assistly/static/3d-planner-preview.gif)](https://github.com/bayliu/3D-storage-planner-project.git/)

**[➡️ 點此查看線上 Demo](https://github.com/bayliu/3D-storage-planner-project.git/)**

---

## ✨ 主要功能

*   **多種倉庫尺寸選擇**：提供 S, M, L 等預設尺寸供使用者切換。
*   **新增常用物品**：可快速新增預設尺寸的箱子、床墊、冰箱等。
*   **全 3D 互動**：
    *   在 3D 空間中用滑鼠拖曳移動物品。
    *   用滑鼠右鍵點擊物品進行 90 度旋轉。
    *   透過物理引擎實現自然的堆疊和碰撞效果。
    *   自由旋轉、縮放、平移視角來檢視空間的每個角落。
*   **即時空間分析**：
    *   以進度條顯示空間體積使用率。
    *   顯示總空間體積和已放置物品的總體積。
    *   即時更新已放置物品的列表，並可單獨移除。

---

## 🛠️ 技術棧

*   **前端框架**: [React](https://reactjs.org/)
*   **3D 渲染**: [Three.js](https://threejs.org/) + [@react-three/fiber](https://github.com/pmndrs/react-three-fiber)
*   **3D 輔助工具**: [@react-three/drei](https://github.com/pmndrs/drei)
*   **物理引擎**: [@react-three/rapier](https://github.com/pmndrs/react-three-rapier)
*   **狀態管理**: [Zustand](https://github.com/pmndrs/zustand)
*   **建置工具**: [Vite](https://vitejs.dev/)
*   **樣式**: [TailwindCSS](https://tailwindcss.com/)

---

## 🚀 快速開始與部署指南

您可以輕鬆地將這個專案部署到自己的 GitHub Pages，並將其嵌入到任何網站（如 WordPress）中。

### 第 1 步：下載並設定專案

1.  **Clone 或下載專案**
    ```bash
    git clone https://github.com/bayliu/3D-storage-planner-project.git
    cd YOUR_REPOSITORY_NAME
    ```

2.  **安裝依賴套件**
    在專案的根目錄下，執行以下指令。這會下載所有必要的函式庫。
    ```bash
    npm install
    ```

3.  **在本地端預覽**
    執行以下指令，即可在本地電腦上啟動開發伺服器進行預覽。
    ```bash
    npm run dev
    ```
    然後在瀏覽器中打開 `http://localhost:5173`。

### 第 2 步：個人化設定 (部署前的關鍵步驟)

在部署之前，您需要修改兩個檔案，將其指向您自己的 GitHub 倉庫。

1.  **修改 `package.json`**
    打開 `package.json` 檔案，將 `homepage` 的值改為您的 GitHub Pages URL。
    ```json
    "homepage": "https://github.com/bayliu/3D-storage-planner-project.git",
    ```

2.  **修改 `vite.config.js`**
    打開 `vite.config.js` 檔案，將 `base` 的值改為您的倉庫名稱。
    ```javascript
    export default defineConfig({
      base: '/YOUR_REPOSITORY_NAME/',
      // ...
    })
    ```
    > **注意**: 請將 `YOUR_GITHUB_USERNAME` 和 `YOUR_REPOSITORY_NAME` 替換為您自己的 GitHub 使用者名稱和倉庫名稱。

### 第 3 步：一鍵部署到 GitHub Pages

1.  **執行部署指令**
    在終端機中，執行以下指令：
    ```bash
    npm run deploy
    ```
    這個指令會自動建置專案，並將其推送到您倉庫的 `gh-pages` 分支。

2.  **設定 GitHub Pages**
    *   前往您在 GitHub 上的專案倉庫，點擊 `Settings` -> `Pages`。
    *   在 "Build and deployment" 下，將 `Source` 設定為 **`Deploy from a branch`**。
    *   將 `Branch` 設定為 **`gh-pages`**，資料夾設定為 **`/(root)`**。
    *   點擊 `Save`。

等待幾分鐘後，您的網站就會成功部署！您可以在同一個頁面上找到您的公開網站網址。

---

## 嵌入到 WordPress 或其他網站

部署成功後，您會得到一個公開的網址。您可以使用 `<iframe>` 將這個應用程式嵌入到任何支援 HTML 的網站中。

**範例程式碼：**

```html
<div style="width: 100%; max-width: 900px; margin: 20px auto; aspect-ratio: 16 / 10; border: 1px solid #ccc; border-radius: 8px; overflow: hidden;">
  <iframe
    src="https://github.com/bayliu/3D-storage-planner-project.git/"
    title="3D 倉儲空間規劃工具"
    style="width: 100%; height: 100%; border: none;"
  >
  </iframe>
</div>
```

---

## 📝 授權

本專案採用 MIT 授權。

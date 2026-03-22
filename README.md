# WFGY 3.0 · Tension Universe

131 個世界級未解難題的互動展示。每個問題以「張力語言」重新編碼——
不是學術摘要，而是讓任何人都能感受到問題核心張力的故事。

基於開源專案 [WFGY](https://github.com/onestardao/WFGY)（MIT）衍生製作。

🔗 **Live demo**: https://scyprodigy.github.io/wfgy-scy

---

## 技術選擇

**React 18 + Babel CDN，無 build 流程**

刻意不使用 Vite / CRA / Next.js，原因：
- 目標是快速迭代內容，不是建工程架構
- 單一 `index.html` 推上去就能跑，零配置
- 驗證想法優先，工程化是下一階段的事

**純 inline CSS，無 UI 框架**

不用 Tailwind / MUI / Chakra，原因：
- 宇宙感的視覺效果需要精確控制每個 color / opacity / glow
- 套框架反而要花時間對抗預設樣式
- 規模還小，inline 最直接

**Canvas 動畫（StarFieldWarp）**

- 不依賴任何動畫 library
- Canvas 直接操作像素緩衝區，繞過 DOM layout/repaint，手機效能友好
- Warp speed 效果：星星從中心向外加速飛散，`rgba` 半透明清除製造尾跡

**GitHub Pages 部署**

- 零成本，推 main 分支自動更新
- 適合純靜態內容的快速展示

---

## 現況與規劃

**現在**：單一 HTML，內容優先，快速驗證

**之後**：拆成正式 React 專案
src/
├── data/          ← 題目內容與領域設定
├── components/    ← StarFieldWarp / ProblemCard / Modal
├── store/         ← 狀態管理
└── App.jsx

基於 [WFGY 3.0](https://github.com/onestardao/WFGY) by PSBigBig · MIT License  
展示層為獨立衍生作品

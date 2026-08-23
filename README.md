# 深夜審核台 · Night Shift 👁️

> 凌晨三點，你是夜班內容審核員。
> 一件一件，核准或移除被系統標記的訊息。
> 你以為，你只是在做你的工作。

一款用**純 HTML / CSS / JavaScript**（零依賴、單一檔案）打造的文字心理恐怖小品。約 8–10 分鐘玩得完。主題圍繞資訊污染、認知扭曲、系統控制——帶一點反烏托邦與賽博龐克。

**▶ 線上遊玩：** https://maymap.github.io/nightshift/

<!-- TODO: 錄一段 5 秒 GIF（火球…不，是審核台 + 一次「介面攻擊」）放這裡，是整個專案最重要的門面 -->
<!-- ![gameplay](docs/preview.gif) -->

---

## 這是什麼

不是一個「有很多分支選項的故事」。它的恐怖不靠嚇人的畫面，而是一種**慢慢滲出來的不對勁**——玩下去你就會知道為什麼。剩下的，留給你自己在凌晨三點發現。

> 最好的體驗：**桌機、關燈、戴耳機、半夜玩，一氣呵成不要暫停。**

## 玩法

- 讀一則被標記的訊息，決定 **核准** 或 **移除**。
- 系統會盯著你的**配合度**。太有主見，它不會高興。
- 全程可**點擊空白處跳過打字動畫**。

## 技術

- **零依賴、零建置**：單一 `index.html`，原生 JS，一個小型「劇情狀態機」驅動所有場景。
- **把瀏覽器 API 當敘事工具**：用 `Page Visibility API`、`localStorage`、即時時鐘等，讓「介面的行為」本身成為敘事的一部分（怎麼用，就不劇透了）。
- **氛圍**：CRT 掃描線 + 暈影 + 磷光終端機配色（IBM Plex Mono / Sans），打字機效果，glitch 文字。
- **無障礙**：尊重 `prefers-reduced-motion`（關閉閃爍與抖動）、鍵盤焦點可見、語意化按鈕。
- **RWD**：桌機與手機皆可玩（建議桌機、關燈、戴耳機）。

## 本地執行

因為用到 `localStorage`（在 `file://` 下受限），建議開一個本機伺服器：

```bash
# 進到專案資料夾後，任選一種
python3 -m http.server 8000
# 或
npx serve .
```

然後開 `http://localhost:8000`。（單純看畫面的話，直接用瀏覽器開 `index.html` 也行，只是「它記得你」那招不會生效。）

## 部署（GitHub Pages）

本專案是純靜態站，`index.html` 在根目錄，可直接由 GitHub Pages 服務：

1. 推上 GitHub。
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**，選 `main` / `/ (root)`。
3. 稍等一分鐘，站點會出現在 `https://<你的帳號>.github.io/nightshift/`。

（`.nojekyll` 已包含，避免 Jekyll 處理靜態檔。）

## 內容提醒

心理恐怖題材：包含監控、失去自主、被凝視的不安感，以及**刻意違反使用者預期的介面行為**——遊玩中若覺得「介面怎麼怪怪的」，那是設計的一部分，不是 bug。無血腥、無 jump scare。

## 授權

[MIT](LICENSE) © 2026 maymap

# 深夜審核台 · Night Shift 👁️

> 凌晨三點，你是夜間內容審核員。

**▶ 玩：** https://maymap.github.io/nightshift/

<!-- TODO: 之後放一段 5 秒 GIF -->

一款單一 `index.html`、零依賴的內容審核敘事遊戲。

---

### 玩法

讀被標記的內容 → 用 **[查作者]／[比對紀錄]／[展開全文]** 查證 → **核准** 或 **移除**。

### 技術

零建置的原生 JS 單檔：`localStorage` 跨場記憶、`Web Audio` 生成音效、CRT 磷光介面；支援 `prefers-reduced-motion`、RWD。

### 本地執行

```bash
python3 -m http.server 8000
```

（用到 `localStorage`，建議走 http 而非 `file://`。）

---

MIT © 2026 maymap ｜ 設計筆記：[`docs/SCRIPT_A.md`](docs/SCRIPT_A.md)

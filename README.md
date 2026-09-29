# Klingon

**A single-file cognition & output system.** One `index.html`, your browser, your data — no build step, no framework, no backend, no account.

**單檔案認知與輸出系統。** 一個 `index.html`，你的瀏覽器，你的資料——無需建置、無框架、無後端、無帳號。

## Screenshots

| Morning Notebook 晨間行動手帳 | Night Notebook 晚思心靈手帳 |
|:---:|:---:|
| ![Morning notebook](docs/morning.png) | ![Night notebook](docs/night.png) |

*Monthly notebooks: a 30-day life grid, per-day ledgers, and print-ready A4 PDF output.*

## Background 背景

Klingon is built around the **D1 → D3 → D7 output method** (inspired by Shion Kabasawa's memory books): an idea is captured as a one-line intuition on **Day 1**, transformed into written reflection on **Day 3**, and distilled into practice on **Day 7**. A gentle 7-day loop, morning dopamine focus, and a night review close the circle; at each month's end everything settles into a printed notebook.

It is also an experiment in **"less is more" software**: no colors louder than one teal accent, no emoji, no modals stacked on modals — just warm paper, serif type, and small sounds. It was designed to be the kind of tool a person can actually use every day, which means it never scolds you for missing a day (the "grace period" rule).

Klingon 以**樺澤紫苑式輸出法**為骨幹：**D1** 直覺留痕（一句話捕捉靈感）→ **D3** 轉化書寫（展開成反思）→ **D7** 沉澱實踐（化為行動），構成一條溫和的 7 日記憶迴路。晨間三件聚焦、晚間三行微反思、月底自動成冊，讓輸入與輸出閉環。

它同時也是一次「**少即是多**」的軟體實驗：全站只允許一種強調色、零彩色 emoji、不疊彈窗——只有溫潤紙白、襯線字體與輕微的聲音回饋。它被設計成「真的可以每天用」的工具，因此**永不責備你漏掉的任何一天**（記憶寬容期）。

## Features 功能

- **Morning Focus 晨間待辦** — up to 3 tasks with a rising-sun badge that fills as you check them off; drag & drop ordering; last night's "one small step" appears as a ghost placeholder you can adopt with Tab.
  最多 3 件聚焦事項，朝陽徽章隨完成數升起；支援拖拽排序；昨晚寫下的「一小步」會化作幽靈浮水印，按 Tab 即可採納。

- **Output Tracker 輸出追蹤** — magazine-style cards with punched-ticket stubs (STUB 01 已顯影 → STUB 02 今日待打孔 → STUB 03 鎖定), red PUNCHED stamps on each stage you complete, and a frameless writing drawer that preserves every line break.
  雜誌式卡片搭配打孔票根；完成階段即在票根上蓋紅色 PUNCHED 鋼印；無邊框寫作抽屜嚴格保留你的每一個換行與分段。

- **Night Review 晚思覆盤** — today's traces aggregated into a light accordion, three-line micro reflection, 4-7-8 breathing rhythm, and a synthesized singing bowl when you turn off the light.
  今日留痕輕量摺疊呈現；三行微反思即時存檔；4-7-8 呼吸節律；熄燈時響起合成頌缽。

- **Monthly Notebooks 月度雙手帳** — a 30-day life grid (life rhythm rate), morning & night ledgers, and print-ready A4 PDF with binding margin; day blocks never split across pages.
  30 天生命星圖與節律達成率；晨間行動／晚思心靈雙本切換；出版級 A4 PDF 導出，同日內容絕不跨頁腰斬。

- **Spotlight 全域檢索** — `Ctrl / ⌘ + K` to search everything you've ever written.

- **Multi-window safe storage 多視窗安全存儲** — merge-on-save with tombstones (deleted items never resurrect), order-is-data semantics, rotating timestamped backups (20 restore points), a snapshot rescue layer, and a **history panel** to browse and restore any past state.
  寫入前自動合併多視窗改動；刪除墓碑防止復活；「順序即資料」；每次儲存留存時間戳備份（最多 20 個還原點）；快照救援與歷史版本面板。

- **Local file persistence 本地存檔** — optionally grant access to a folder and every save also writes a plain `klingon-data.json` you can see in Explorer; if browser storage is ever cleared, the app restores itself from that file on next launch.
  可選授權一個資料夾，每次儲存同步寫入明文 JSON；即使瀏覽器資料被清空，下次開啟自動復原。

- **Export 導出** — share cards in Paper White / Obsidian Dark (copy or download as PNG), plus JSON backup / restore for the whole archive.
  紙白／曜石雙主題分享卡（複製或下載 PNG）；整庫 JSON 備份／恢復。

## Design rules 設計原則

- Zero colored emoji — every icon is a 1.5px monochrome geometric SVG. 全站零彩色 emoji，所有圖標皆為 1.5px 單色幾何線條。
- English-only category labels: **All · Book · Movie · Show · Podcast · Life**. 分類標籤恆為英文。
- Long-form text always preserves paragraph structure: `pre-wrap`, Georgia serif, 1.8 line height. 長文永遠保留換行與分段。
- No closed focus frames on writing surfaces — underline only. 寫作區域物理級滅框，僅保留底線。
- Warm paper palette: `#FBFAF4` paper · `#F8F7F0` sidebar · `#E6E2D4` ecru · `#20808D` teal accent.

## Run 使用方式

1. Download `index.html` 下載 `index.html`
2. Double-click it (Chrome or Edge recommended) 直接雙擊開啟（建議 Chrome 或 Edge）
3. That's it. 就這樣。

Optional: click 啟用本地存檔 in the sidebar to mirror every save to a folder of your choice. 可選：點擊側欄「啟用本地存檔」，將每次儲存同步到指定資料夾。

## Data & privacy 資料與隱私

Everything lives in your browser's localStorage (key `klingon.v1`) plus, optionally, a JSON file in a folder you choose. **Nothing is ever uploaded anywhere.** The only network request the page makes is loading the optional html2canvas library from a CDN — every feature, including image export, works offline with the built-in canvas engine.

所有資料只存在你的瀏覽器 localStorage（鍵值 `klingon.v1`）與你指定的本地資料夾中，**永不上傳任何伺服器**。頁面唯一的網路請求是由 CDN 載入 html2canvas；包括圖片導出在內的所有功能皆可離線運作。

## License

[MIT](LICENSE) © suzie — free to use, modify, and build upon. Attribution appreciated.

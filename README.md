# Claude 做的設計為什麼都長一個樣：Nate Parrott 談怎麼擺脫 AI slop

Peter Yang 頻道訪談 Anthropic 產品設計師 Nate Parrott（2026-10-23 錄影，2026-11-15 上傳，42:01）的深度導讀。內容涵蓋 Claude 預設設計風格的「四個破綻」從哪裡來、怎麼用上下文蓋過它、從手機筆記到設計稿的流程、做原型變快之後慢的是哪一段、Claude Design 的產品沿革、儀表板與 Claude Motion 示範、怎麼測一個模型判斷不了好壞的設計 skill、Claude Tag 的內部用法，以及講者說法與官方方案限制的對照。

## 製作聲明

本導讀的分析與撰稿由 AI 模型完成，不是人類分析，也沒有經過人工逐句校稿。分工（以主文〈製作說明〉為準）：逐句中文翻譯由 agy 的 gemini-3.8-flash-medium 完成，再由 Claude Opus 5.5 讀完全部 581 句中英對照、修正其中 35 句（含依聽音結果修正的 9 句）；存疑句的聽音校對用 agy 的 gemini-3.8-flash-high；研究與撰稿由 Claude Opus 5.5 完成；獨立審稿三路，事實審稿用 Claude Opus 5.5（另做第二方查證），編輯審稿用 Claude Sonnet，修稿後的終審用 Claude Opus 5.5；最後由 Claude Opus 5.5 依總編輯準則潤稿並標示重點，其後又經兩輪總編輯審查與潤稿（共三輪，皆為 AI 模型執行）。整體流程由 Claude Sonnet 5.5 統籌派工與合併審稿意見。圖由 Claude Opus 5.5 以 SVG、動態 SVG 與 Mermaid 繪製，未使用 AI 生圖：封面是抽象示意圖，四個破綻與做原型週期兩張是本文的示意，Motion 三案風格依影片畫面重繪，流程圖依講者描述整理；除 Motion 三案外，都不是影片畫面。封面 `hero-zh.svg` 無文字、以極慢速度循環漂移，做原型週期一張的動畫只播一次、停在完整畫面；系統設定開啟減少動態效果時，兩張都直接顯示靜態畫面；`images/og-hero.jpg` 是封面 `hero-zh.svg` 的靜態畫面以瀏覽器截圖轉成的 1200×630 圖（左右以背景色補邊），不是另外生成的圖。

字幕是 YouTube 機器字幕，沒有說話者標記；約 55 句存疑句由 AI 聆聽原音片段核對，其餘句子沒有對照原音。引言的中文是翻譯，不是講者原話，可能有誤。

## 檔案

| 檔案 | 說明 |
|---|---|
| `nate-parrott-claude-design.md` | 正式導讀 Markdown |
| `index.html` | 導讀網頁（可直接用瀏覽器開啟，圖片為相對路徑；Mermaid 由 CDN 載入；CDN 失效或關閉 JavaScript 時，文章、封面與三張 SVG 圖照常顯示，流程圖改成顯示 Mermaid 原始碼） |
| `player.html` | 中英雙語字幕同步播放器（YouTube 嵌入，581 句、9 章） |
| `translation-zh.html` | 全文繁中譯本（非官方，依 YouTube 機器字幕，AI 翻譯） |
| `images/` | 封面 `hero-zh.svg`（抽象示意、緩慢循環；手機版 `hero-zh-mobile.svg` 為 1:1）與三組示意圖 SVG（四個破綻、做原型週期〔動畫只播一次〕、Motion 三案風格），各有桌面版與 `-mobile` 版；`og-hero.jpg` 由封面截圖而成 |

## 原始來源

- 影片：Full Tutorial: How to Fix AI Slop with Claude Design in 40 Minutes | Nate Parrott，Peter Yang 頻道，https://www.youtube.com/watch?v=604T-74s3KE
- 逐字稿：YouTube 機器字幕（en-orig），原檔不另外公開；播放器與譯文頁顯示的是逐句定稿

## 重要來源

- Claude 部落格〈How the product designer who built Claude Design uses it to explore ideas before building them〉（2026-07-24）
- Anthropic：Claude Design 發布公告（2026-04-17）、〈Introducing Claude Tag〉（2026-06-23）
- Claude：〈Cowork is now Claude〉（2026-09-16）；Claude 部落格〈Dashboards and Motion〉（2026-10-08）、〈Claude Duet〉（2026-10-21）
- Claude 說明中心〈Get started with Claude Design〉、Claude Artifacts 功能頁、Claude Tag 說明文件
- 完整清單與可信度見導讀文末〈來源清單〉

## 狀態

已發布（2026-11-22）：https://lushinshang.github.io/nate-parrott-claude-design/ ；repo `lushinshang/nate-parrott-claude-design`（公開，GitHub Pages，main／根目錄）。公開 repo 只含 `index.html`、`player.html`、`translation-zh.html`、`nate-parrott-claude-design.md`、`README.md`、`share_post.md`、`images/`；研究與 QA 紀錄不公開。

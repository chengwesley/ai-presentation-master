# Presentation Thinking

**一個幫你「想清楚再做」的簡報教練 skill。**

Presentation Thinking 是一個 AI agent skill（通用的 `SKILL.md` 格式），Claude Code、Codex、Gemini CLI、Cursor 等支援 agent skills 的工具都能安裝。它不負責一鍵生成投影片，而是陪你把簡報背後的事想清楚：要講給誰聽、有多少時間、核心主張是什麼、該用什麼故事結構、哪一頁該畫成什麼圖、上台前要準備哪些 Q&A。

> An agent skill (standard `SKILL.md` format) that coaches you through the *thinking* behind a presentation — audience, time budget, argument structure, visual logic, script and Q&A — rather than generating slides in one click. Content is in Traditional Chinese.

---

## 為什麼要做這個

把題目丟給 AI，通常會得到一份條列整齊、版面漂亮，但沒有觀點、沒有故事的簡報。原因很簡單：AI 很會整理資料，卻不知道哪件事對你的聽眾最重要，也沒有你的真實經驗。

這個 skill 的分工原則是：**講者是總導演，AI 是特效團隊。** 觀點、案例與現場判斷由你負責；資料蒐集、初稿、版面與圖表由 AI 協助。中間最重要的一步，是和 AI 進行批判性對話，而不是直接接受第一版。

## 涵蓋範圍

四種場合：**商業提案、對內匯報、公開講座、教育訓練**，各有不同的成功標準與閱讀路徑。

| 階段 | 內容 |
|---|---|
| 構思 | 三個前置問題（時間、場合、現場講或給人讀）、GAP-T、時間→頁數換算、金字塔原理／SCQA、P-S-B／英雄之旅／三幕劇、DISC 受眾模擬 |
| 寫作 | 初稿提示詞、去 AI 味潤稿、詰問測試 |
| 視覺 | 內容邏輯→圖解形式對照、版型與網格、圖示系統、配色語意、圖表常見雜訊、讓數字有感 |
| 表達 | 開場鉤子、轉場、結尾、Q&A 準備與現場應對 |
| 課程 | 學習目標、注意力曲線、模組時間表、互動設計 |
| 交付 | 把規格交給 Gamma／Canva／open-slide 等工具的翻譯方式、16:9 vs 4:3、字型嵌入與 PDF 輸出檢查 |

## 安裝

把整個資料夾放進你的 agent 的 skills 目錄，例如 Claude Code：

```bash
git clone https://github.com/chengwesley/presentation-thinking ~/.claude/skills/presentation-thinking
```

之後說「幫我做簡報」「這份簡報怎麼講故事」「20 分鐘要做幾頁」「怕被問倒」之類的話就會啟動。

## 檔案結構

```
presentation-thinking/
├── SKILL.md            # 入口：流程、情境路由、使用原則
├── references/         # 14 份主題文件，依情境或症狀按需讀取
└── evals/              # 9 個情境測試案例＋20 題觸發測試
```

## 授權

[MIT](LICENSE)

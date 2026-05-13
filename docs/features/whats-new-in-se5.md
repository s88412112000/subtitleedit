# Subtitle Edit 5 的新功能

Subtitle Edit 5 是基於 Avalonia 的跨平台版本。它保留了 Windows Forms 版本中令人熟悉的字幕編輯工作流程，同時擴充了許多新功能。

## 應用程式平台

- 適用於 Windows、Linux 和 **macOS** 的跨平台 Avalonia UI — macOS 是 SE 5 新增支援的平台。
- 更簡潔、支援高 DPI (High-DPI-aware) 的 UI，能在現代顯示器上正確縮放。
- 自動跟隨系統主題 (淺色、深色等)，或手動選擇主題。
- 針對 Linux 的全新 Flatpak 套件包裝作業。
- 新增許多設定選項，且設定對話方塊內建搜尋功能，可快速找到任何選項。
- 在需要選擇資料夾時使用原生的資料夾選擇對話方塊 (這在 WinForms 4.x 系列中缺失)。

## 編輯與網格

- **在網格中顯示格式** — 格式標籤 (斜體、粗體、顏色等) 現在可以在字幕網格中以視覺化方式呈現。
- 編輯控制項的顯示/隱藏/持續時間現在是選擇性的，可以切換開啟或關閉。
- 在字幕網格 / 列表檢視中一次刪除多行的速度大幅提升。
- 新增 **工具 (Tools) → 變更格式 (Change formatting)** 對話方塊，用於在選取的行中新增或移除斜體、粗體、底線及其他格式。
- 新增 **工具 (Tools) → 合併兩個字幕 (Merge two subtitles)** 工具，可以將兩個字幕 (或已載入的字幕文字 + 翻譯) 合併為一個雙語字幕。輸出可為 SubRip 格式 (重疊配對以上下行堆疊) 或 ASSA 格式，具備兩種可設定的樣式 (字型、顏色、外框、陰影、頂部/底部對齊) 及即時預覽。

## 影片

- 新增 **影片 (Video) → 重新編碼 (Re-encode)** 工具，將影片重新編碼為更適合字幕工作的格式。
- 新增 **影片 (Video) → 剪輯影片 (Cut video)** 工具，直接從 Subtitle Edit 中裁剪影片片段。
- **影片 (Video) → 燒錄帶有標誌的字幕 (Burn-in with logo)** — 現在將字幕內嵌到影片中時可以包含標誌/浮水印圖片。
- 許多新的語音轉文字引擎 (參見下方的[語音轉文字](#speech-to-text))。
- 改善了讀取 MP4 檔案中內嵌字幕的功能。

## 同步

- **視覺化同步 (Visual Sync)** 現在包含波形圖，讓挑選精確的同步點變得更容易。

## 波形圖與頻譜圖

- 波形圖工具列按鈕可以自訂、排序、匯入和匯出。
- 波形圖主題可以匯入和匯出。
- **頻譜圖樣式 (Spectrogram style)** 可以在執行階段更改 — 無需重新生成。
- 波形圖和頻譜圖有更多自訂選項，包含顏色、鏡頭切換顏色及視覺樣式。

## 語音轉文字

語音辨識不再侷限於經典的 Whisper 工作流程。Subtitle Edit 5 包含了更廣泛的本機和可下載引擎：

- Purfview Faster-Whisper XXL、CTranslate2、Whisper.cpp、OpenAI Whisper 以及 Const-me's Whisper。
- 具備多種 GGUF 模型大小的 Qwen3 ASR。
- 包含 GLM、Qwen3、Granite、Omni、Parakeet、Canary、Cohere 和 Fire Red 等 Crisp ASR 變體。
- 每個引擎獨立的進階參數和批次轉錄的改進。
- 幾個較新的引擎支援自動語言選擇。

有關目前的引擎清單和工作流程，請參閱[語音轉文字](speech-to-text.md)。

## 文字轉語音

文字轉語音現在包含更多本機與雲端引擎：

- Edge-TTS。
- Mistral TTS。
- 提供可下載本機伺服器版本與模型的 Qwen3 TTS。
- 提供可下載本機伺服器版本與模型的 Kokoro TTS。
- 提供 CUDA 和 Metal 版本，以及可下載本機伺服器版本與模型的 OmniVoice TTS。
- 審核音訊片段、重新生成個別行、保留重新生成歷史紀錄，並匯出包含中繼資料的生成片段。

詳細資訊請參閱[文字轉語音](text-to-speech.md)。

## OCR (光學字元辨識) 與批次轉換

- 批次轉換 (Batch Convert) 可以使用 Binary OCR，並能自動偵測多項 nOCR/Binary OCR 設定。
- OCR 工作流程中提供 PaddleOCR、Ollama OCR、Mistral OCR、Google Lens、Google Vision 以及 Llama.cpp OCR。

請參閱 [OCR](ocr.md)、[批次轉換](batch-convert.md) 及 [命令列 (seconv)](../reference/command-line.md)。

## ASSA 工具

- 新增 **套用進階效果 (Apply advanced effects)** 工具，可生成電影級與充滿創意的 ASSA 覆寫標籤動畫 (打字機、卡拉 OK、彈出、霓虹燈、故障特效、彩虹、星空、雨、雪、螢火蟲等)，並具備即時影片預覽。
- **隱藏圖層 (Hide layer)** — 現在可以在預覽中隱藏個別的 ASSA 圖層，讓您能專注於正在處理的行。
- **ASSA 過濾 (ASSA filtering)** — 透過樣式、演員、圖層或標籤內容，在 ASSA 網格中過濾與搜尋行。

## 字幕格式

- 新增支援 **IMSC-Rosetta Timed Text** 字幕格式。
- 新增 **使用自訂欄位匯入 CSV/XLSX (Import CSV/XLSX with custom columns)** 視窗，適用於不符合標準佈局的試算表 — 可選擇哪些欄位對應至開始時間、結束時間、文字等。

## 命令列 (seconv)

`seconv` 無頭 (headless) 轉換器現在位於 Subtitle Edit 主儲存庫中 — 它與桌面應用程式同步構建、發布及更新。

- **精美的終端機 UI (Polished terminal UI)** — 彩色輸出、每個檔案的進度、摘要表格，以及適用於 CI 流程和腳本的 `--json` 模式。
- **跨平台 (Cross-platform)** — 在 Windows、Linux 和 macOS 上執行，只需要 .NET 執行階段；無需顯示器或 GUI，適合伺服器和 Docker。
- **更廣泛的功能集 (Broader feature set)** — 額外的時間與清理操作、OCR 引擎選擇 (Tesseract / nOCR / Binary OCR / Ollama / PaddleOCR)、從 `.mkv` / `.mp4` / `.mcc` 輸入容器、用於檢查的 `info` 與 `lint` 子命令、自訂輸出範本，以及 POSIX 風格的旗標名稱 (舊版 SE 4.x 的旗標仍然可用)。

有關用法和範例，請參閱[命令列 (seconv)](../reference/command-line.md)。

## 接下來看哪裡

- [主視窗](main-window.md) - 更新後的應用程式佈局。
- [音訊視覺化 / 波形圖](audio-visualizer.md) - 波形圖、頻譜圖及鏡頭切換工具。
- [第三方元件](../third-party-components.md) - 元件設定和資料夾位置。
- [命令列 (seconv)](../reference/command-line.md) - 無頭轉換與 OCR。

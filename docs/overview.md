# 總覽 (Overview)

## 什麼是 Subtitle Edit？

Subtitle Edit 是一個免費、開源的影片字幕編輯器。它讓您可以建立、編輯、調整和轉換各種不同格式的字幕。

**Subtitle Edit 5** 是最新一代，使用 [Avalonia UI](https://avaloniaui.net/) 建立，支援跨平台 (Windows、Linux、macOS)。

> **注意:** Subtitle Edit 5 目前處於 Beta 測試階段。

## 主要功能

- **建立和編輯** 超過 300 種格式的字幕
- **同步** 字幕到影片，提供視覺化工具
- **語音轉文字** — 使用 Whisper 引擎轉錄音訊
- **文字轉語音** — 從字幕文字生成音訊
- **自動翻譯** 字幕
- **OCR** — 將基於圖片的字幕 (藍光、DVD 等) 轉換為文字
- 自動 **修復常見錯誤**
- 支援字典的 **拼字檢查**
- 將字幕 **內嵌 (Burn-in)** 到影片中
- **批次轉換** 多個檔案
- **ASSA/SSA 樣式設定**，具備進階的覆寫標籤、繪圖和定位功能
- 用於精確時間軸調整的 **波形圖/頻譜圖**
- 用於專業工作流程的 **鏡頭切換偵測**
- **匯出為圖片式字幕** (藍光 SUP、BDN-xml、VobSub 等)

## 系統需求

- Windows 10+ / Linux / macOS 
- [FFmpeg](https://ffmpeg.org/) (用於音訊/影片處理)
- [libmpv](https://mpv.io/) 用於影片播放

## 開始使用

遵循這些簡單的步驟來開始在 Subtitle Edit 中處理字幕：

1. **安裝 Subtitle Edit**  
   從官方網站下載並安裝最新版本。

2. **開啟影片檔案**  
   前往 **影片 (Video) → 開啟影片檔案 (Open video file)...** 並選擇您的影片。  
   這可讓您準確地預覽和同步字幕。

3. **開啟、建立或生成字幕檔案**  
   - 透過 **檔案 (File) → 開啟 (Open)** 開啟現有檔案
   - 透過 **檔案 (File) → 新增 (New)** 建立新檔案
   - 或使用 **語音轉文字** (**影片 (Video) → 語音轉文字 (Speech to text)**) 自動生成字幕

4. **編輯您的字幕**  
   使用字幕網格和文字編輯器來：
   - 調整文字  
   - 分割或合併行  
   - 微調時間  

5. **視覺化調整時間**  
   使用波形圖顯示來精確地將字幕與音訊同步。

6. **儲存您的工作**  
   前往 **檔案 (File) → 儲存 (Save)** (或按 **Ctrl+S**) 來儲存您的字幕檔案。

<!-- Screenshot: Main window overview -->
![Main Window](screenshots/main-window.png)

## 主視窗佈局

主視窗包含幾個主要區域：

- **選單列 (Menu Bar)** — 存取所有功能
- **工具列 (Toolbar)** — 快速存取常用動作
- **字幕網格 (Subtitle Grid)** — 包含時間和文字的所有字幕行列表
- **文字編輯器 (Text Editor)** — 編輯目前選取的字幕文字
- **影片播放器 (Video Player)** — 預覽包含字幕的影片
- **音訊視覺化 (Audio Visualizer)** — 波形圖/頻譜圖，用於精確的時間調整

Subtitle Edit 提供 **12 種不同的佈局** 來排列這些區域。您可以透過 **選項 (Options) → 選擇佈局 (Choose layout)** 來選擇和自訂佈局。

如需每個區域的詳細指南、滑鼠互動和鍵盤快捷鍵，請參閱 **[主視窗 (Main Window)](features/main-window.md)** 說明文件。

<!-- Screenshot: Main window with light mode -->
![Main Window (light mode)](screenshots/main-window-light.png)

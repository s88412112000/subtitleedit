# Subtitle Edit - 說明文件

Subtitle Edit 是一個免費、開源的影片字幕編輯器。這是基於 Avalonia 的跨平台版本 (Subtitle Edit 5) 的說明文件。

## 開始使用

- [總覽](overview.md) — 什麼是 Subtitle Edit 以及如何開始使用
- [Subtitle Edit 5 的新功能](features/whats-new-in-se5.md) — 從 Windows Forms 版本到 Avalonia 版本的主要變更
- [主視窗](features/main-window.md) — 主視窗佈局、區域和互動指南
- [常見問題 (FAQ)](faq.md) — 常見問題解答

## 功能區域

### 檔案操作
- [檔案選單](features/file.md) — 新增、開啟、儲存、匯入、匯出

### 編輯
- [編輯選單](features/edit.md) — 尋找、取代、多重取代、修改選取範圍、歷史紀錄
- [字幕網格](features/subtitle-grid.md) — 使用字幕列表/網格
- [文字編輯器](features/text-editor.md) — 編輯字幕文字

### 工具
- [修復常見錯誤](features/fix-common-errors.md) — 自動錯誤偵測與修復
- [檢查並修復 Netflix 錯誤](features/netflix-errors.md) — Netflix 品質檢查、建議修復與 CSV 報表
- [批次轉換](features/batch-convert.md) — 轉換多個字幕檔案
- [變更大小寫](features/change-casing.md) — 修復大小寫問題
- [變更格式](features/change-formatting.md) — 修改字幕格式
- [轉換演員](features/convert-actors.md) — 在不同樣式間轉換演員/配音標籤
- [建立空白翻譯](features/empty-translation.md) — 從目前字幕建立一個空白的翻譯欄位
- [調整持續時間](features/adjust-duration.md) — 調整字幕顯示的持續時間
- [套用持續時間限制](features/apply-duration-limits.md) — 強制執行最小/最大持續時間規則
- [橋接間隙](features/bridge-gaps.md) — 橋接字幕間的間隙
- [套用最小間隙](features/apply-min-gap.md) — 設定字幕間的最小間隙
- [合併短行](features/merge-short-lines.md) — 合併簡短的字幕行
- [合併相同文字的行](features/merge-same-text.md) — 合併重複的文字行
- [合併相同時間碼的行](features/merge-same-timecodes.md) — 合併時間相同的行
- [重新編號](features/renumber.md) — 從選擇的起始數字重新編號字幕行
- [分割/斷開長行](features/split-break-long-lines.md) — 斷開過長的行
- [分割字幕](features/split-subtitle.md) — 將一個字幕檔案分割成多個檔案
- [合併字幕](features/join-subtitles.md) — 合併多個字幕檔案
- [排序方式](features/sort-by.md) — 依據各種條件對字幕進行排序
- [移除聽障人士專用文字](features/remove-text-hi.md) — 移除 HI 註解

### 同步
- [調整所有時間](features/adjust-all-times.md) — 位移所有時間
- [視覺化同步](features/visual-sync.md) — 與影片視覺化同步
- [點同步](features/point-sync.md) — 使用參考點同步
- [透過其他字幕進行點同步](features/point-sync-via-other.md) — 使用其他字幕進行同步
- [變更影格率](features/change-frame-rate.md) — 在不同影格率間轉換
- [變更速度](features/change-speed.md) — 調整播放速度

### 影片
- [影片播放器](features/video-player.md) — 影片播放控制
- [音訊視覺化 / 波形圖](features/audio-visualizer.md) — 波形圖顯示與編輯
- [語音轉文字](features/speech-to-text.md) — 使用 Whisper、Qwen3、Parakeet、Crisp ASR 及相關引擎進行自動語音辨識
- [文字轉語音](features/text-to-speech.md) — 從字幕生成語音
- [燒錄字幕](features/burn-in.md) — 將字幕內嵌（硬字幕）到影片中
- [內嵌字幕](features/embedded-subtitles.md) — 在 Matroska/WebM 檔案中新增、移除、預覽及編輯字幕軌
- [透明字幕](features/transparent-subtitles.md) — 生成透明字幕影片
- [鏡頭切換](features/shot-changes.md) — 偵測與管理鏡頭切換
- [空白影片](features/blank-video.md) — 生成空白影片
- [重新編碼影片](features/re-encode-video.md) — 重新編碼影片檔案
- [剪輯影片](features/cut-video.md) — 剪輯影片片段

### 翻譯
- [自動翻譯](features/auto-translate.md) — 自動字幕翻譯
- [複製/貼上翻譯](features/copy-paste-translate.md) — 透過複製/貼上工作流程進行翻譯

### 拼字檢查
- [拼字檢查](features/spell-check.md) — 檢查字幕拼字
- [尋找雙重字](features/find-double-words.md) — 尋找重複的單字
- [尋找雙重行](features/find-double-lines.md) — 尋找連續重複的字幕行

### OCR (光學字元辨識)
- [OCR](features/ocr.md) — 將基於圖片的字幕轉換為文字 (nOCR、Binary OCR、Tesseract)

### ASSA (Advanced SubStation Alpha)
- [ASSA 樣式](features/assa-styles.md) — 管理 ASS/SSA 樣式
- [ASSA 屬性](features/assa-properties.md) — 編輯腳本屬性
- [ASSA 附件](features/assa-attachments.md) — 管理字型/圖片附件
- [ASSA 繪圖](features/assa-draw.md) — 向量繪圖工具
- [ASSA 設定位置](features/assa-set-position.md) — 在畫面上定位字幕
- [ASSA 設定背景](features/assa-set-background.md) — 新增背景方塊
- [ASSA 進度條](features/assa-progress-bar.md) — 生成進度條
- [ASSA 解析度重新取樣](features/assa-resolution-resampler.md) — 針對不同解析度重新取樣
- [ASSA 圖片色彩選擇器](features/assa-image-color-picker.md) — 從影片中挑選色彩
- [ASSA 套用進階效果](features/assa-apply-advanced-effects.md) — 套用電影和創意動畫效果
- [ASSA 套用自訂覆寫標籤](features/assa-override-tags.md) — 套用自訂標籤

### 選項
- [設定](features/settings.md) — 應用程式設定
- [快捷鍵](features/shortcuts.md) — 鍵盤快捷鍵
- [單字清單](features/word-lists.md) — 自訂單字清單和字典

### 其他
- [比較](features/compare.md) — 比較字幕檔案
- [統計資料](features/statistics.md) — 字幕統計資料

## 貢獻

- [翻譯 Subtitle Edit](translating.md) — 如何將使用者介面翻譯成其他語言

## 參考資料

### 格式文件
- [支援的格式](reference/supported-formats.md) — 所有支援的字幕格式清單
- [SubRip (SRT) 格式](reference/subrip.md) — 完整的 SubRip 格式參考與指南
- [WebVTT 格式](reference/webvtt.md) — 完整的 WebVTT 格式參考 (HTML5 標準)
- [Advanced Sub Station Alpha (ASSA) 格式](reference/assa.md) — 完整的 ASSA 格式參考與指南
- [ASSA 覆寫標籤參考](reference/assa-override-tags.md) — 完整的 ASSA/SSA 覆寫標籤參考

### 應用程式參考
- [鍵盤快捷鍵參考](reference/keyboard-shortcuts.md) — 完整的鍵盤快捷鍵清單
- [滑鼠控制參考](reference/mouse-controls.md) — 滑鼠互動
- [命令列 (seconv)](reference/command-line.md) — 無頭命令列轉換器
- [第三方元件](third-party-components.md) — FFmpeg、MPV、OCR、語音轉文字和文字轉語音設定指南

# 文字轉語音 (Text to Speech)

使用各種 TTS (文字轉語音) 引擎，從字幕文字生成語音音訊。

- **選單:** 影片 (Video) → 文字轉語音 (Text to speech)...
- **快捷鍵:** 可設定

<!-- Screenshot: Text to Speech window -->
![Text to Speech](../screenshots/text-to-speech.png)

## 如何使用

1. 開啟 **影片 (Video) → 文字轉語音 (Text to speech)...**
2. 從下拉選單中選擇一個 TTS 引擎
3. 選擇語言和語音
4. 選擇性啟用 **審核音訊片段 (Review audio clips)** 來審核每個生成的片段
5. 選擇性啟用 **生成影片檔案 (Generate video file)** 來建立包含音訊的影片
6. 點擊 **生成 (Generate)** 開始

## 支援的引擎

- **Piper** — 本機、開源 TTS
- **Edge-TTS** — Microsoft Edge 線上語音
- **AllTalk** — 本機 TTS 伺服器
- **ElevenLabs** — 雲端型、高品質語音 (需要 API 金鑰)
- **Azure Cognitive Services** — Microsoft 雲端 TTS (需要 API 金鑰和地區)
- **Mistral TTS** — 雲端型 Mistral 語音生成 (需要 API 金鑰)
- **Google Cloud** — Google 雲端 TTS (需要金鑰檔案)
- **Qwen3 TTS** — 本機可下載的 Qwen3 TTS 伺服器與模型
- **Kokoro TTS** — 本機可下載的 Kokoro TTS 伺服器與模型
- **Murf.ai** — 雲端 TTS (需要 API 金鑰)

當您接受下載提示時，本機可下載的引擎會安裝到 Subtitle Edit 的資料夾中。

## 引擎設定

某些引擎需要額外的設定：

- **API 金鑰 (API Key)** — 輸入您用於雲端引擎的 API 金鑰
- **地區 (Region)** — 選擇 Azure 地區 (適用於 Azure 引擎)
- **模型 (Model)** — 選擇語音模型
- **金鑰檔案 (Key file)** — 瀏覽 Google Cloud 服務帳戶金鑰檔案

## 本機 SE5 引擎

### Qwen3 TTS

Qwen3 TTS 執行一個本機伺服器。Subtitle Edit 可以在首次使用時下載引擎和所選模型。

- 可用的模型選項包含 **0.6B** 和 **1.7B Base**。
- 模型下載也需要 tokenizer 模型。
- Qwen3 TTS 支援匯入參考 WAV 語音。匯入的語音會出現在語音下拉選單中。
- 在 Windows 上，Subtitle Edit 可以根據可用性提供 CPU 或 Vulkan 版本。

### Kokoro TTS

Kokoro TTS 執行一個本機伺服器以及可下載的模型。

- Subtitle Edit 會在需要時下載引擎和模型檔案。
- 可以立即從內建的語音清單中使用語音名稱，也可以從執行中的伺服器重新整理。
- 當您想要一個不需要 API 金鑰的本機、多語言 TTS 引擎時，這是一個不錯的選擇。

### Mistral TTS

Mistral TTS 是透過設定 API 金鑰和選擇模型來使用的。選擇的模型會被記憶在設定中。

## 審核音訊片段

當啟用 **審核音訊片段 (Review audio clips)** 時，生成後會開啟一個專屬的審核視窗。這個視窗讓您可以在套用結果前，檢查、播放並重新生成每一行字幕的音訊。

### 審核網格

每一行字幕會顯示為一列，包含以下欄位：

| 欄位 | 說明 |
|--------|-------------|
| **包含 (Include)** | 核取方塊，用於將該行包含在最終輸出中或排除 |
| **#** | 字幕行號 |
| **文字 (Text)** | 字幕文字 (可編輯 — 在重新生成前連按兩下修改) |
| **語音 (Voice)** | 該行使用的語音 |
| **速度 (Speed)** | 為了讓音訊符合字幕持續時間所套用的速度係數 |
| **CPS** | 該行字幕的每秒字元數 (Characters per second) |

### 播放控制

- **播放 (Play)** — 播放所選行的音訊片段
- **停止 (Stop)** — 停止播放
- **自動繼續 (Auto-continue)** — 啟用時，當目前片段播放完畢後，會自動前進到下一行播放

### 重新生成片段

您可以針對任何個別行重新生成音訊：

1. 在網格中選擇該行
2. 從下拉選單中選擇所需的引擎、語音、語言、模型或樣式
3. 點擊 **重新生成 (Regenerate)** 或按 **Ctrl+R**

新的片段會被裁切掉靜音部分，並自動調整速度以符合字幕時間。重新生成後，新的片段會立即播放以供審核。

對於 ElevenLabs，當選擇該引擎時，會有額外的微調參數可用：**穩定性 (Stability)**、**相似度 (Similarity)**、**語者增強 (Speaker Boost)**、**速度 (Speed)** 以及 **風格誇飾 (Style Exaggeration)**。**重設 (Reset)** 按鈕可以將所有 ElevenLabs 參數恢復為預設值。

### 重新生成歷史紀錄

每次重新生成片段時，都會儲存先前的版本。要審核某一行的歷史紀錄，點擊該列的 **歷史紀錄 (History)** 按鈕。歷史紀錄對話方塊會顯示所有生成版本及其語音名稱和速度，並讓您播放每一個版本。選擇一個版本並點擊 **確定 (OK)** 可將其還原為該行的作用中片段。

### 包含 / 排除行

取消勾選任何一列的 **包含 (Include)** 核取方塊，可將該行的音訊從最終輸出中排除。被排除的行在組合影片檔案時會被跳過。

### 匯出片段

點擊 **匯出 (Export)** 將所有音訊片段和一個 `SubtitleEditTts.json` 中繼資料檔案儲存到您選擇的資料夾。JSON 檔案記錄了每一行的音訊檔案名稱、字幕時間、語音名稱、引擎名稱、速度係數和文字，這讓重新匯入或在外部對片段進行後製變得很容易。

### 鍵盤快捷鍵

| 按鍵 | 動作 |
|-----|--------|
| Ctrl+R | 重新生成所選行 |
| Escape | 關閉 / 取消 |
| F1 | 開啟說明 |

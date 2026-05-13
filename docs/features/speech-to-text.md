# 語音轉文字 (Speech to Text)

Subtitle Edit 可以使用基於 Whisper 及其他現代語音辨識引擎，自動將音訊轉錄為文字。

- **選單:** 影片 (Video) → 語音轉文字 (Speech to text)...

<!-- Screenshot: Speech to text window -->
![Speech to Text](../screenshots/speech-to-text.png)

## 支援的引擎

| 引擎 | 平台 | 備註 |
|--------|----------|-------|
| Whisper.cpp | Windows, Linux, macOS | 本機 CPU 引擎 |
| Whisper.cpp (cuBLAS) | Windows | NVIDIA CUDA 版本 |
| Whisper.cpp (Vulkan) | Windows | Vulkan GPU 版本 |
| Purfview's Faster Whisper XXL | Windows, Linux | 快速的本機引擎，通常搭配 NVIDIA CUDA 使用 |
| Whisper CTranslate2 | Windows, Linux, macOS | CPU / NVIDIA CUDA，取決於安裝方式；CUDA 需要 [CUDA 12.x](https://developer.nvidia.com/cuda-12-0-0-download-archive) |
| Const-me's Whisper | Windows | 基於 DirectX 的引擎 |
| OpenAI Whisper | 全部 | 基於 Python 的 OpenAI Whisper 工作流程 |
| Chat LLM.cpp | Windows, Linux, macOS | 本機 LLM 轉錄工作流程；macOS 下載適用於 Apple Silicon |
| Qwen3 ASR CPP | Windows, Linux, macOS | 本機 Qwen3 ASR 引擎，附帶可下載的 GGUF 模型 |
| Parakeet.cpp | Windows, Linux, macOS | 本機 Parakeet 引擎；部分模型僅限英文，較大的模型則支援多語言 |
| Crisp ASR GLM | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Qwen3 | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Granite | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Omni | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Parakeet | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Canary | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Cohere | Windows, Linux, macOS | Crisp ASR 後端 |
| Crisp ASR Fire Red | Windows, Linux, macOS | Crisp ASR 後端 |

引擎和模型會在首次使用時自動下載。

## SE5 引擎備註

- **Qwen3 ASR CPP** 包含 0.6B 和 1.7B 模型選項，加上用於時間軸工作流程的強制對齊 (forced-aligner) 模型。
- **Parakeet.cpp** 會將每個模型存放在獨立的資料夾中，因為模型需要權重與詞彙 (vocabulary) 檔案。
- **Crisp ASR** 引擎共用相同的後端工作流程，並公開不同的模型系列，例如 GLM、Qwen3、Granite、Omni、Parakeet、Canary、Cohere 和 Fire Red。
- 幾個較新的引擎支援自動語言選擇。
- 每個引擎都可以有獨立的進階命令列參數。

## 如何使用

1. 在 Subtitle Edit 中開啟影片檔案
2. 前往 **影片 (Video) → 語音轉文字 (Speech to text)...**
3. 從下拉選單中選擇一個 **引擎 (Engine)**
4. 選擇一個 **模型 (Model)** (較大的模型通常準確度較高，但需要更多時間與磁碟空間)
5. 選擇音訊的 **語言 (Language)**，或在所選引擎支援時使用自動語言
6. 選擇性啟用：
   - **翻譯成英文 (Translate to English)** — 將非英文音訊翻譯成英文
   - **調整時間 (Adjust timings)** — 使用波形資料進行時間後處理
   - **後處理 (Post-processing)** — 修復大小寫、合併行、加上句號等
7. 點擊 **轉錄 (Transcribe)**

## 模型

每個引擎都有自己專屬的一組模型。常見的模型大小有：
- **tiny** — 最快，準確度最低
- **base** — 在快速處理與準確度間取得良好平衡
- **small** — 更好的準確度
- **medium** — 高準確度
- **large** / **large-v2** / **large-v3** — 最高準確度，速度最慢

以 `.en` 結尾的模型僅限英文，且對英文音訊的表現較好。

## 批次模式

一次轉錄多個影片檔案：
1. 點擊 **批次模式 (Batch mode)**
2. 新增影片檔案
3. 點擊 **轉錄 (Transcribe)**
4. 結果將會儲存為 `.srt` 檔案，並與影片檔案放在同一個目錄下

## 進階設定

點擊 **進階 (Advanced)** 按鈕來為 Whisper 引擎設定自訂命令列參數：
- 使用 VAD (語音活動偵測) 以獲得更好的時間軸
- 在轉錄文字中標示說出的單字 (Highlight spoken words)
- 調整溫度 (temperature) 或其他模型參數

進階設定是每個引擎獨立儲存的，因此您可以為 Whisper.cpp、Qwen3 ASR、Parakeet.cpp、Crisp ASR 等其他引擎保留各自獨立的參數。

## 後處理設定

點擊 **後處理 (Post-processing)** 按鈕以設定：
- 調整時間 (使用波形峰值資料)
- 修復過短的持續時間
- 修復大小寫
- 新增句號
- 合併短行
- 分割長行
- 將底線變更為顏色 (適用於標示說出的單字)

## 主控台記錄 (Console Log)

底部的控制台記錄會顯示來自 Whisper 程序的即時輸出，對於偵錯問題很有幫助。

## 提示

- 對於 NVIDIA GPU 使用者，使用 **Whisper.cpp (cuBLAS)** 或 **Purfview's Faster Whisper XXL** 可獲得最快的轉錄速度
- 如果您遇到 "CUDA out of memory" (CUDA 記憶體不足) 錯誤，請嘗試使用較小的模型
- `--standard` 參數會自動加到 Purfview's Faster Whisper XXL 中
- 您可以對引擎區域按右鍵來重新下載引擎
- 如果新的引擎尚未安裝任何模型，請先讓 Subtitle Edit 下載引擎和所選的模型，然後再開始轉錄

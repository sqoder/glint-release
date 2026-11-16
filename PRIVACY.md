# Glint Privacy Policy / Glint 隐私政策

Last updated / 最后更新：2026-11-16

---

## 中文说明

Glint 是一款本地优先（Offline-First）的 macOS 原生生产力工具，不收集用户行为遥测、不上传分析日志，也不设自有云端账号或后台服务器。

### 1. 本地处理的数据
- **截图、录屏、OCR、剪贴板历史、生词本与便签**：默认全部在您的 Mac 本机完成处理与存储，绝不静默上传。
- **可选项目符号提取（默认关闭）**：启用后仅在本地扫描当前工作区代码标识符以提升语音专有词识别准确度。
- **应用内密钥存储**：您配置的第三方服务 API Key 加密保存于 macOS 系统钥匙串（Login Keychain）。
- **本地性能与诊断记录**：系统级 MetricKit 性能与崩溃诊断仅保存在本机 `~/Library/Application Support/Glint/Diagnostics`，绝不自动上传；仅当您手动点击「导出诊断包」时生成本地 `.zip` 压缩包供自行排查。

### 2. 系统权限使用范围
- **屏幕录制**：仅在您主动触发截图、长截图、录屏或屏幕取词翻译时采集指定屏幕画面。
- **麦克风与语音识别**：仅在您启用语音听写或录屏麦克风收录时采集音频。
- **辅助功能**：仅用于全局快捷键响应、长截图滚动及语音听写结果回填。
- **日历与定位（可选）**：仅在您启用顶部日程或本地天气组件时读取日历日程，或通过系统 `CoreLocation` 获取所在城市坐标（未授予位置权限时仅在本机按系统时区推断城市坐标兜底，不使用 `ipapi.co`）。

### 3. 可选第三方网络服务（均由用户主动触发）
- **翻译与云端语音（BYOK）**：仅当您主动启用并填写 Google Cloud Translation、DeepL、百度翻译、网易有道或 OpenAI 兼容接口的 API Key，并在首次使用弹窗中明确点击同意后，对应选中文本或音频片段才会直连您选定的服务商。
- **天气预报**：开启天气组件时，会向 [Open-Meteo](https://open-meteo.com) 请求天气预报数据。
- **专辑封面补全**：播放音乐且播放器未直接提供封面图片时，会向 Apple iTunes Search API 查询公开的专辑封面。
- **手动版本检查**：仅当您主动点击「检查更新…」时，向 GitHub Releases（`api.github.com/repos/sqoder/glint-release/releases/latest`）查询最新公开版本号，不上传任何设备标识或个人数据。

---

## English

Glint is an offline-first native macOS productivity workstation. It collects **zero telemetry, analytics, or crash reports** and operates without proprietary cloud accounts or backend servers.

### 1. Local-Only Data Processing
- **Screenshots, recordings, OCR text, clipboard history, vocabulary, and notes** are processed and stored locally on your Mac by default.
- **Optional Project Symbol Extraction (Off by Default)**: When enabled, scans local workspace identifiers purely on-device to improve dictation accuracy.
- **API Credentials**: Any third-party API keys you enter are stored in the macOS Login Keychain.
- **Local Diagnostics**: System MetricKit performance and crash metrics are stored strictly locally under `~/Library/Application Support/Glint/Diagnostics` and never uploaded automatically; a local `.zip` diagnostic bundle is generated only when you explicitly click "Export Diagnostics".

### 2. macOS Permissions
- **Screen Recording**: Used strictly when you initiate capture, scrolling capture, recording, or screen OCR translation.
- **Microphone & Speech Recognition**: Used strictly when you trigger voice dictation or enable microphone recording.
- **Accessibility**: Used for global hotkeys, scrolling capture automation, and cursor text insertion.
- **Calendars & Location (Optional)**: Used only when Calendar or Weather widgets are enabled; Weather uses Apple CoreLocation when authorized and falls back to local system timezone city coordinates on-device (without calling `ipapi.co`).

### 3. Optional External Services (User-Initiated Only)
- **Translation & Cloud Speech (BYOK)**: Only when you explicitly configure your own API key (Google Cloud Translation, DeepL, Baidu, Youdao, or OpenAI-compatible endpoints) and confirm the explicit first-use consent prompt are selected text or audio clips sent directly to that chosen provider.
- **Weather Widget**: Queries [Open-Meteo](https://open-meteo.com) when enabled.
- **Album Artwork Lookup**: Queries Apple's public iTunes Search API when a supported media player does not supply artwork directly.
- **Manual Update Check**: Queries GitHub Releases (`api.github.com/repos/sqoder/glint-release/releases/latest`) only when you explicitly click "Check for Updates…", without sending device identifiers or user data.

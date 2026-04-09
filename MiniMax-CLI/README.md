---
title: "MiniMax AI CLI｜官方命令行工具"
date: 2026-04-09
source: "https://github.com/MiniMax-AI/cli"
source_type: webpage
tags: [MiniMax, AI, CLI, TTS, Image-Gen, Video-Gen, Music-Gen, Vision, Search, 文字生成, 圖片生成, 影片生成, 語音合成, 音樂生成]
---

# MiniMax AI CLI｜官方命令行工具

> 官方 CLI for the MiniMax AI Platform。為 AI Agent 打造，從終端機生成文字、圖片、影片、語音和音樂。

---

## 基本資訊

| 項目 | 內容 |
|------|------|
| **Repo** | [MiniMax-AI/cli](https://github.com/MiniMax-AI/cli) |
| **官方檔** | npm: [`mmx-cli`](https://www.npmjs.com/package/mmx-cli) |
| **語言** | TypeScript |
| **授權** | MIT |
| **Node.js** | >= 18 |
| **平台** | Global (`api.minimax.io`) / CN (`api.minimaxi.com`) |

---

## 核心功能

### 1. Text（文字生成）
- 多輪對話、Streaming 輸出
- System Prompt 自訂
- JSON 格式輸出
- 支援模型切換（`MiniMax-M2.7-highspeed` 等）

### 2. Image（圖片生成）
- Text-to-Image
- 可指定長寬比（aspect ratio）
- 批次生成（`--n 3`）

### 3. Video（影片生成）
- 非同步影片生成，可追進度
- 直接下載完成品

### 4. Speech / TTS（語音合成）
- 30+ 種音色（voices）
- 語速控制
- Streaming 即時播放
- 支援從檔案或 stdin 讀取文字

### 5. Music（音樂生成）
- Text-to-Music
- 可搭配 Lyrics（填詞）
- Instrumental 純音樂模式

### 6. Vision（視覺理解）
- 圖片理解與描述
- 支援本地檔案或 URL

### 7. Search（網路搜尋）
- MiniMax 驅動的網路搜尋

---

## 安裝方式

```bash
# 方式一：為 AI Agent 安裝（推薦 OpenClaw / Cursor / Claude Code 用）
npx skills add MiniMax-AI/cli -y -g

# 方式二：終端機全域安裝
npm install -g mmx-cli
```

> ⚠️ 需要 MiniMax Token Plan：Global / CN

---

## 快速開始

```bash
# 登入認證
mmx auth login --api-key sk-xxxxx

# 文字對話
mmx text chat --message "What is MiniMax?"

# 圖片生成
mmx image "A cat in a spacesuit"

# 語音合成
mmx speech synthesize --text "Hello!" --out hello.mp3

# 影片生成（非同步）
mmx video generate --prompt "Ocean waves at sunset" --async

# 音樂生成
mmx music generate --prompt "Upbeat pop" --lyrics "[verse] La da dee"

# 網路搜尋
mmx search "MiniMax AI latest news"

# 查看圖片
mmx vision photo.jpg

# 查看配額
mmx quota
```

---

## 主要指令一覽

| 指令 | 功能 |
|------|------|
| `mmx text chat` | 多輪文字對話 |
| `mmx image generate` | 圖片生成 |
| `mmx video generate` | 影片生成 |
| `mmx speech synthesize` | 語音合成 |
| `mmx music generate` | 音樂生成 |
| `mmx vision` | 圖片理解 |
| `mmx search` | 網路搜尋 |
| `mmx auth login` | 登入驗證 |
| `mmx quota` | 查看 API 配額 |
| `mmx config show` | 查看設定 |
| `mmx update` | 更新 CLI |

---

## 音色（Voices）參考

可用音色包含：
- `English_magnetic_voiced_man`
- `English_female_cool_yooung`
- 以及 30+ 其他音色

可用指令查詢完整清單：
```bash
mmx speech voices
```

---

## 與龍蝦騎士團的連結

### OpenClaw 整合
```bash
# 為 OpenClaw 安裝 MiniMax CLI skill
npx skills add MiniMax-AI/cli -y -g
```

### 應用場景
- **MoltBook YouTube Pipeline**：可用 `mmx speech synthesize` 替代現有 TTS 方案
- **content-to-obsidian**：可用 MiniMax TTS 產生語音版本的文章
- **影片生成**：結合 `mmx image` + `mmx video` + `mmx speech` 打造完整影片 pipeline

---

## 與其他 TTS 方案的比較

| 方案 | 語音品質 | 速度 | 成本 | 離線 |
|------|---------|------|------|------|
| **MiniMax TTS** | ⭐⭐⭐⭐⭐ | 快 | Token 計費 | ❌ |
| OpenAI TTS | ⭐⭐⭐⭐ | 快 | 收費 | ❌ |
| Kokoro TTS | ⭐⭐⭐⭐ | 本地很快 | 免費 | ✅ |

---

*原始 Repo：[github.com/MiniMax-AI/cli](https://github.com/MiniMax-AI/cli)｜MIT License*

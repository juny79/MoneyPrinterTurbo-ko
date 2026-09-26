# MoneyPrinterTurbo 💸

> **올인원 AI 숏폼 영상 자동 생성 도구**  
> 주제나 키워드만 입력하면 AI가 영상 스크립트 작성부터 화면 매칭, 자막 생성, 음성 합성(TTS), 배경음악 삽입까지 자동으로 진행하여 고화질 쇼츠/릴스/틱톡 영상을 합성합니다.

[简体中文](README.md) | [English](README-en.md) | [日本語](README-ja.md) | [한국어](README-ko.md)

---

## 🎯 주요 기능

- **다양한 실행 환경**: WebUI, REST API, CLI, AI Agent 지원
- **스크립트 자동 생성**: OpenAI, Claude, Google Gemini, DeepSeek, Ollama 등 다양한 LLM 연동 지원
- **고화질 영상/이미지 소재 자동 수집**: Pexels, Pixabay, Coverr 무료 스톡 영상 및 AI 비디오 생성 모델 연동
- **음성 합성(TTS)**: Edge TTS(무료, API Key 불필요), Azure Speech, ElevenLabs, MiniMax, Fish Audio 등 지원 (한국어 음성 완벽 지원)
- **자막 자동 생성**: 폰트, 위치, 크기, 외곽선, 배경 스타일 커스텀 지원
- **다양한 화면 비율**: 세로형 9:16 (1080×1920), 가로형 16:9 (1920×1080), 정방형 1:1 (1080×1080)
- **멀티 플랫폼 자동 업로드**: TikTok, YouTube Shorts, Instagram 릴스 자동 배포 지원

---

## 📦 시스템 요구 사항

| 항목 | 최소 사양 | 권장 사양 | 이상적인 사양 |
| :--- | :--- | :--- | :--- |
| **운영체제** | Windows 10, macOS 11.0+, Linux | Windows 10+, macOS, Linux | 최신 Linux / Windows |
| **CPU** | 4 코어 | 6 ~ 8 코어 | 8 코어 이상 |
| **RAM** | 4 GB | 8 GB | 16 GB 이상 |
| **GPU** | 필수가 아님 | VRAM 4 GB 이상 | VRAM 8 GB 이상 |

* 클라우드 LLM 및 온라인 스톡 영상 소스를 주로 사용할 경우 GPU 없이도 원활하게 구동됩니다.
* 로컬 Faster-Whisper 자막 추출이나 로컬 모델 실행 시 외장 GPU가 권장됩니다.

---

## 🚀 빠른 시작 (설치 및 배포)

### 사전 준비 사항
- Python 3.11 이상 설치 권장
- 시스템에 FFmpeg 설치 필요

---

### 방법 1: uv를 사용한 로컬 설치 (권장)

```bash
# 1. 저장소 클론
git clone [https://github.com/](https://github.com/)<사용자_아이디>/MoneyPrinterTurbo-ko.git
cd MoneyPrinterTurbo-ko

# 2. uv를 통한 Python 3.11 환경 구축 및 의존성 설치
uv python install 3.11
uv sync --frozen

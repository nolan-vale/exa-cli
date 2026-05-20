<div align="center">

← [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md) · [Português](README.pt-BR.md) · [Español](README.es.md) · [日本語](README.ja.md)

# exa-cli

**개발자를 위한 뉴럴 웹 검색. 터미널에서 바로.**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

키워드 검색은 단어를 찾습니다. **Exa는 의미를 검색합니다.** `exa-cli`는 그 능력을 터미널로 직접 가져옵니다 — 개념을 검색하고, 페이지를 크롤링하고, 깔끔한 JSON을 스크립트, AI 에이전트, 연구 파이프라인으로 전달하세요.

## 왜 exa-cli인가?

**키워드 검색이 찾지 못하는 것을 찾아드립니다.**  
뉴럴 검색은 입력한 단어뿐만 아니라 의도를 이해합니다.

**처음부터 자동화를 위해 설계되었습니다.**  
모든 명령은 `--json` 출력을 지원합니다. `jq`, 에이전트, 스크립트에 바로 전달하세요.

**검색 그 이상.**  
어떤 URL과도 유사한 페이지를 찾고, 콘텐츠 유형·날짜·도메인으로 필터링하고, 한 명령으로 전체 페이지 텍스트를 가져오세요.

## 설치

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=당신의-키   # exa.ai에서 발급
```

## 예시

```bash
# 어떤 URL과 유사한 페이지 찾기
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# 2025년 최신 AI 연구 논문
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# GitHub 저장소만, JSON 출력
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# 어떤 페이지든 깔끔한 텍스트 추출
exa-crawl https://example.com -c 8000

# AI 심층 연구
exa-research "2025년 비전 언어 모델 현황"
```

## 전체 문서

→ **[USAGE.md](USAGE.md)**（영어）— 모든 명령어, 옵션, 스크립트 예시.

---

<div align="center">
<sub><a href="https://exa.ai">Exa API</a> 기반 · MIT 라이선스</sub>
</div>

<div align="center">

← [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md) · [Português](README.pt-BR.md) · [Español](README.es.md) · [한국어](README.ko.md)

# exa-cli

**開発者のためのニューラル Web 検索。ターミナルから直接。**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

キーワード検索は言葉を探します。**Exa は意味を検索します。** `exa-cli` はその力をシェルに直接もたらします — コンセプトを検索し、ページをクロールし、クリーンな JSON をスクリプト、AI エージェント、研究パイプラインに渡せます。

## なぜ exa-cli？

**キーワード検索では見つけられないものを見つける。**  
ニューラル検索は入力した単語だけでなく、意図を理解します。

**最初から自動化のために設計。**  
すべてのコマンドは `--json` 出力をサポート。`jq`、エージェント、スクリプトにそのまま渡せます。

**検索以上のこと。**  
任意の URL に似たページを見つけ、コンテンツタイプ・日付・ドメインでフィルタリングし、1 コマンドでページ全文を取得できます。

## インストール

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=あなたのキー   # exa.ai で取得
```

## 使用例

```bash
# 任意の URL に似たページを検索
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# 2025 年の最新 AI 研究論文
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# GitHub リポジトリのみ、JSON 出力
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# 任意のページのクリーンなテキストを取得
exa-crawl https://example.com -c 8000

# AI による深い調査
exa-research "2025年のビジョン言語モデルの現状"
```

## 完全なドキュメント

→ **[USAGE.md](USAGE.md)**（英語）— すべてのコマンド、オプション、スクリプト例。

---

<div align="center">
<sub><a href="https://exa.ai">Exa API</a> を使用 · MIT ライセンス</sub>
</div>

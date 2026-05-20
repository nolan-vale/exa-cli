<div align="center">

[中文](docs/README.zh-CN.md) · [Русский](docs/README.ru.md) · [Português](docs/README.pt-BR.md) · [Español](docs/README.es.md) · [日本語](docs/README.ja.md) · [한국어](docs/README.ko.md)

<!--
  COVER IMAGE — generate with this prompt, save as docs/cover.png, then uncomment the line below.

  Prompt (Midjourney / DALL-E 3 / Stable Diffusion):
  "A sleek dark terminal window filled with glowing cyan and blue search results streaming
  in real-time, abstract neural network nodes forming a luminous web in the background,
  minimalist developer aesthetic, pure black background, neon accent colors,
  wide cinematic banner, 2:1 aspect ratio, no text, no UI chrome"

  <img src="docs/cover.png" alt="exa-cli" width="100%">
-->

# exa-cli

**Neural web search for developers. From your terminal.**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/davidparker7966-design/exa-cli?style=social)](https://github.com/davidparker7966-design/exa-cli)

</div>

---

Keyword search matches words. **Exa searches by meaning.** `exa-cli` puts that power directly in your shell — find concepts, crawl pages, and pipe clean JSON into your scripts, AI agents, and research pipelines.

## Why exa-cli?

**Find what keyword search misses.**  
Neural search understands what you're looking for, not just the words you typed. Ask for concepts, topics, or vibes — Exa gets it.

**Built for automation from day one.**  
Every command outputs clean `--json`. Pipe into `jq`, pass to agents, feed into scripts. No scraping, no parsing HTML — just structured data.

**More than search.**  
Find pages similar to any URL. Filter by content type (`news`, `github`, `research paper`, `tweet`…), date range, or domain. Crawl full page text in one command.

## Install

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=your-key   # get yours at exa.ai
```

## See it in action

```bash
# Find pages similar to any URL
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# Latest AI research papers, structured output
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# Only GitHub repos, pipe to jq
exa-search "async rust runtime" --include-domain github.com --json | jq '.[].url'

# Crawl any page, get clean text
exa-crawl https://example.com -c 8000

# Deep AI research on a topic
exa-research "state of vision language models 2025"
```

## Full documentation

→ **[docs/USAGE.md](docs/USAGE.md)** — all commands, flags, piping recipes, and scripting examples.

---

<div align="center">
<sub>Built on the <a href="https://exa.ai">Exa API</a> · MIT License · <a href="https://github.com/davidparker7966-design/exa-cli/issues">Report an issue</a></sub>
</div>

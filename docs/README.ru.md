<div align="center">

← [English](../README.md) · [中文](README.zh-CN.md) · [Português](README.pt-BR.md) · [Español](README.es.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

# exa-cli

**Нейронный поиск для разработчиков. Прямо из терминала.**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

Ключевые слова ищут буквы. **Exa ищет смысл.** `exa-cli` переносит эту возможность прямо в терминал — ищи концепции, сканируй страницы, передавай чистый JSON в скрипты, AI-агенты и исследовательские пайплайны.

## Зачем exa-cli?

**Находит то, что ключевые слова не найдут.**  
Нейронный поиск понимает смысл запроса, а не просто слова. Ищи по концепциям — Exa поймёт.

**Создан для автоматизации с первого дня.**  
Каждая команда поддерживает `--json`. Передавай в `jq`, агентов или скрипты напрямую.

**Больше чем поиск.**  
Находи похожие страницы по URL, фильтруй по типу контента, датам и доменам, получай полный текст страницы одной командой.

## Установка

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=твой-ключ   # получить на exa.ai
```

## Примеры

```bash
# Найти похожие страницы по URL
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# Последние AI-статьи 2025 года
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# Только GitHub-репозитории, вывод JSON
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# Получить чистый текст любой страницы
exa-crawl https://example.com -c 8000

# Глубокое AI-исследование темы
exa-research "состояние vision language models 2025"
```

## Полная документация

→ **[USAGE.md](USAGE.md)**（EN）— все команды, флаги и примеры.

---

<div align="center">
<sub>Работает на <a href="https://exa.ai">Exa API</a> · MIT License</sub>
</div>

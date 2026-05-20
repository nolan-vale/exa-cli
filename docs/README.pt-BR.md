<div align="center">

← [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md) · [Español](README.es.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

# exa-cli

**Busca web neural para desenvolvedores. Direto do terminal.**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

Busca por palavras-chave encontra palavras. **Exa busca por significado.** `exa-cli` traz esse poder direto para o seu shell — busque conceitos, extraia páginas e direcione JSON limpo para seus scripts, agentes de IA e pipelines de pesquisa.

## Por que exa-cli?

**Encontre o que a busca por palavras-chave não encontra.**  
A busca neural entende o que você quer dizer, não apenas o que você digitou.

**Construído para automação desde o primeiro dia.**  
Todos os comandos têm `--json`. Redirecione para `jq`, agentes ou scripts diretamente.

**Mais do que busca.**  
Encontre páginas similares a qualquer URL, filtre por tipo de conteúdo, data e domínio, extraia texto completo com um único comando.

## Instalação

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=sua-chave   # obtenha em exa.ai
```

## Exemplos

```bash
# Encontrar páginas similares a uma URL
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# Artigos de pesquisa sobre IA em 2025
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# Apenas repositórios GitHub, saída JSON
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# Extrair texto limpo de qualquer página
exa-crawl https://example.com -c 8000

# Pesquisa profunda com IA
exa-research "estado dos modelos de linguagem visual em 2025"
```

## Documentação completa

→ **[USAGE.md](USAGE.md)**（EN）— todos os comandos, opções e exemplos de scripts.

---

<div align="center">
<sub>Construído sobre a <a href="https://exa.ai">Exa API</a> · Licença MIT</sub>
</div>

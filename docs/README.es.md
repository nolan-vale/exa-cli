<div align="center">

← [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md) · [Português](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

# exa-cli

**Búsqueda web neural para desarrolladores. Desde tu terminal.**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

La búsqueda por palabras clave encuentra palabras. **Exa busca por significado.** `exa-cli` lleva ese poder directamente a tu shell — busca conceptos, extrae páginas y envía JSON limpio a tus scripts, agentes de IA y pipelines de investigación.

## ¿Por qué exa-cli?

**Encuentra lo que la búsqueda por palabras clave no puede.**  
La búsqueda neural entiende lo que buscas, no solo las palabras que escribiste.

**Diseñado para la automatización desde el primer día.**  
Cada comando soporta `--json`. Redirige a `jq`, agentes o scripts directamente.

**Más que búsqueda.**  
Encuentra páginas similares a cualquier URL, filtra por tipo de contenido, fecha y dominio, extrae texto completo con un solo comando.

## Instalación

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=tu-clave   # obtén una en exa.ai
```

## Ejemplos

```bash
# Encontrar páginas similares a una URL
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# Artículos de investigación sobre IA en 2025
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# Solo repositorios de GitHub, salida JSON
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# Extraer texto limpio de cualquier página
exa-crawl https://example.com -c 8000

# Investigación profunda con IA
exa-research "estado de los modelos de lenguaje visual en 2025"
```

## Documentación completa

→ **[USAGE.md](USAGE.md)**（EN）— todos los comandos, opciones y ejemplos de scripts.

---

<div align="center">
<sub>Construido sobre la <a href="https://exa.ai">Exa API</a> · Licencia MIT</sub>
</div>

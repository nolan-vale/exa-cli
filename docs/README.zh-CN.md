<div align="center">

← [English](../README.md) · [Русский](README.ru.md) · [Português](README.pt-BR.md) · [Español](README.es.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

# exa-cli

**为开发者打造的神经网络搜索。直接在终端使用。**

[![PyPI](https://img.shields.io/pypi/v/exa-cli?color=0ea5e9&label=PyPI)](https://pypi.org/project/exa-cli/)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-0ea5e9.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-0ea5e9.svg)](../LICENSE)

</div>

---

关键词搜索匹配文字，**Exa 按语义搜索。** `exa-cli` 将这种能力带到你的终端——搜索概念、抓取页面，并将干净的 JSON 输出传入你的脚本、AI 智能体和研究流水线。

## 为什么选择 exa-cli？

**找到关键词搜索找不到的内容。**  
神经网络搜索理解你想找什么，而不仅仅是你输入的词语。

**从第一天起就为自动化而设计。**  
每个命令都支持 `--json` 输出。可直接传入 `jq`、AI 智能体或脚本。

**不只是搜索。**  
查找与任何 URL 相似的页面，按内容类型、日期范围、域名过滤，一条命令抓取完整页面文本。

## 安装

```bash
uv tool install exa-cli
```

```bash
export EXA_API_KEY=你的密钥   # 在 exa.ai 获取
```

## 示例

```bash
# 查找与任何 URL 相似的页面
exa-search --similar https://docs.anthropic.com/en/api/getting-started

# 2025 年最新 AI 研究论文
exa-search "transformer attention" --category "research paper" --start-date 2025-01-01

# 只搜索 GitHub 仓库，输出 JSON
exa-search "async rust runtime" --include-domain github.com --json | jq '.'

# 抓取任意页面，获取干净文本
exa-crawl https://example.com -c 8000

# AI 深度研究
exa-research "2025年视觉语言模型现状"
```

## 完整文档

→ **[USAGE.md](USAGE.md)**（英文）— 所有命令、参数和脚本示例。

---

<div align="center">
<sub>基于 <a href="https://exa.ai">Exa API</a> · MIT 许可证</sub>
</div>

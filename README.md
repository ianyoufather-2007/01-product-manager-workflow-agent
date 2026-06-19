# 01 Product Manager Workflow Agent

[![Release](https://img.shields.io/github/v/release/ianyoufather-2007/01-product-manager-workflow-agent?display_name=tag)](https://github.com/ianyoufather-2007/01-product-manager-workflow-agent/releases)
[![License](https://img.shields.io/github/license/ianyoufather-2007/01-product-manager-workflow-agent)](LICENSE)
[![Issues](https://img.shields.io/github/issues/ianyoufather-2007/01-product-manager-workflow-agent)](https://github.com/ianyoufather-2007/01-product-manager-workflow-agent/issues)

A standalone agent package for Amazon marketplace product decisions. It wraps the `amazon-product-manager` Codex skill with an agent entrypoint, skill index, examples, and documentation for market screening, product selection, launch planning, profit repair, growth review, inventory risk, and stop-loss calls.

中文说明: [docs/README.zh-CN.md](docs/README.zh-CN.md)

Core skill repository: [amazon-product-manager-skill](https://github.com/ianyoufather-2007/amazon-product-manager-skill)

Recommended for new users: [amazon-pm-integrated-agent](https://github.com/ianyoufather-2007/amazon-pm-integrated-agent)

This repository remains useful as a lightweight agent wrapper around the core skill. If you want the newer integrated routing layer that combines PM triage with a structured stage-gate workflow, start with `amazon-pm-integrated-agent`.

This project is designed for small Amazon sellers and lean product teams that need product-manager discipline without large-company overhead. It helps an AI agent convert incomplete marketplace evidence into explicit decisions, metrics, next actions, and risks.

If you only want the reusable Codex skill, see the core skill in `skills/amazon-product-manager/`. If you want an agent-level workflow wrapper, start from `agents/product-manager-workflow-agent/AGENT.md`.

## Relationship To The Core Skill

This repository is the agent-level wrapper. It includes:

- `agents/product-manager-workflow-agent/AGENT.md` as the workflow entrypoint.
- `agents/product-manager-workflow-agent/SKILL_INDEX.md` as the routing index.
- A bundled copy of `skills/amazon-product-manager/` so the agent can work as a standalone package.

The core skill continues to live in the separate repository: [amazon-product-manager-skill](https://github.com/ianyoufather-2007/amazon-product-manager-skill).

For new public examples and stage-gate routing, see [amazon-pm-integrated-agent](https://github.com/ianyoufather-2007/amazon-pm-integrated-agent).

## What It Does

- Screens markets, categories, niches, price bands, and product lines before choosing a SKU.
- Evaluates demand, competition, economics, differentiation, operations, capital pressure, and compliance risk.
- Produces decisions such as `Enter Market`, `Watch Market`, `Avoid Market`, `Go`, `No-Go`, `Test First`, `Rework Offer`, and `Kill or Liquidate`.
- Creates structured artifacts: market screening memos, product selection memos, launch plans, profit rescue plans, inventory reviews, weekly business reviews, and stop-loss memos.
- Keeps assumptions visible when data is missing.

## Repository Structure

```text
agents/
  product-manager-workflow-agent/
    AGENT.md
    agent.yaml
    SKILL_INDEX.md
skills/
  amazon-product-manager/
    SKILL.md
    agents/openai.yaml
    references/
      amazon-decision-framework.md
      amazon-pm-templates.md
      market-screening-framework.md
examples/
docs/
```

## Agent Entry

Use `agents/product-manager-workflow-agent/AGENT.md` when you want an agent-level workflow wrapper around the core skill. It routes requests across market screening, product selection, competitor response, launch planning, profit rescue, growth review, inventory risk, and stop-loss decisions.

## Installation

Copy the skill folder into your Codex skills directory.

Windows PowerShell:

```powershell
$src = ".\skills\amazon-product-manager"
$dst = "$env:USERPROFILE\.codex\skills\amazon-product-manager"
New-Item -ItemType Directory -Force -Path (Split-Path $dst) | Out-Null
Copy-Item -Recurse -Force $src $dst
```

macOS/Linux:

```bash
mkdir -p ~/.codex/skills
cp -R skills/amazon-product-manager ~/.codex/skills/amazon-product-manager
```

Restart Codex after installing the skill.

## Example Prompt

```text
Use $amazon-product-manager to evaluate whether I should enter the coffee capsule holder market on Amazon US. I have a small brand, limited launch budget, and can source metal or bamboo products. Give me an Enter/Watch/Avoid decision, evidence needed, first wedge, risks, and next actions.
```

More examples are in `examples/`, including [examples/agent-quick-start.md](examples/agent-quick-start.md).

## Data And Privacy

This skill does not require bundled private data. Bring your own marketplace evidence: keywords, ASINs, price bands, review summaries, cost assumptions, FBA estimates, PPC metrics, or inventory data.

Do not commit account credentials, browser session folders, raw customer data, supplier quotes, proprietary exports, or paid-tool datasets unless you have permission to publish them.

## License

MIT

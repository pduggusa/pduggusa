# Patrick Duggan · DugganUSA

[![npm](https://img.shields.io/npm/v/dugganusa-cli?label=npm%20dugganusa-cli)](https://www.npmjs.com/package/dugganusa-cli)
[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code%20Marketplace-published-007ACC)](https://marketplace.visualstudio.com/items?itemName=DugganUSALLC.dugganusa-threat-intel)
[![MCP Registry](https://img.shields.io/badge/MCP%20Registry-listed-blue)](https://registry.modelcontextprotocol.io/v0/servers?search=io.github.pduggusa)
[![IETF Hackathon](https://img.shields.io/badge/IETF%20Hackathon-contributor-lightgrey)](https://github.com/pduggusa/dugganusa-ietf)
[![Free API](https://img.shields.io/badge/free%20API-get%20a%20key-brightgreen)](https://analytics.dugganusa.com/stix/register)

**Threat intelligence you can check.** I build and run [DugganUSA](https://www.dugganusa.com), AI security you can check, built with AI as a working partner: the DugganUSA Feed (free STIX/TAXII/MISP, [live counts](https://analytics.dugganusa.com/api/v1/search/stats)), and research on MCP and AI-agent security. Every claim links to its source, confidence is capped at 95%, and mistakes are corrected in public.

Before this: lead architect for Dell EMC's Azure Stack hybrid cloud, then cloud security architecture at Check Point and Palo Alto Networks.

## For agent builders: add a second opinion in one line

Keep the tools and vendors you already use. These sit beside them, read-only, and need no key, no signup and none of your data.

- **Before your agent installs a package or calls an MCP server**, give it our checks. Claude Code:
  `claude mcp add --transport http dugganusa https://analytics.dugganusa.com/api/v1/mcp`
  Any other MCP client: point it at `https://analytics.dugganusa.com/api/v1/mcp`. The `check-package` tool answers allow, review or block for npm, PyPI, RubyGems and GitHub Actions, with the reason and the source.
- **Before a pull request merges a new dependency or MCP server**, add [dugganusa-checks-action](https://github.com/pduggusa/dugganusa-checks-action) to the workflow. It runs without a key at anonymous limits.
- **Before your agent obeys an instruction file**, run `npx github:pduggusa/dugganusa-agent-guard` in the repo to find hidden Unicode in CLAUDE.md, .cursorrules and AGENTS.md ([source](https://github.com/pduggusa/dugganusa-agent-guard)).

### Support matrix

What each check covers, and what it asks of you.

| Check | Runs where | Covers | Needs a key? | What leaves your machine |
|---|---|---|---|---|
| `check-package` (MCP tool) | Your agent, via `https://analytics.dugganusa.com/api/v1/mcp` | npm, PyPI, RubyGems, GitHub Actions; exact version adds an OSV vulnerability check | No | The package name and version you ask about |
| Dredd `check_mcp_server` (MCP tool) | Your agent, via `https://analytics.dugganusa.com/api/v1/dredd/mcp` | MCP servers, including their full npm/PyPI dependency graph | No | The server name you ask about |
| [dugganusa-checks-action](https://github.com/pduggusa/dugganusa-checks-action) | GitHub Actions, on pull requests | package-lock, npm-shrinkwrap, requirements*.txt, pyproject, poetry.lock, Gemfile(.lock), MCP config files, workflow `uses:` lines | No (anonymous limits); a free key raises them | Package, server and action identities from the diff |
| [dugganusa-agent-guard](https://github.com/pduggusa/dugganusa-agent-guard) | Locally or in CI, zero dependencies | Hidden Unicode in CLAUDE.md, .cursorrules, AGENTS.md and similar files | No | Nothing |
| [dugganusa-cli](https://github.com/pduggusa/dugganusa-cli) | Terminal, CI, or as a local MCP server | IPs, domains, hashes, CVEs, and known-bad packages in lockfiles | Yes, a [free key](https://analytics.dugganusa.com/stix/register) | The indicators it extracts, never the file |

All of them are read-only: they give a verdict and change nothing. Anything that could not be checked is reported as unknown, never as clean.

Every verdict cites where it came from: OSV, abuse.ch, CISA, the researchers who found the thing, and our own hunting. If one is wrong, tell us and we will fix it in public.

## Use it free

- **API key in 30 seconds:** [analytics.dugganusa.com/stix/register](https://analytics.dugganusa.com/stix/register)
- **Feeds:** STIX 2.1 / TAXII 2.1 / MISP, CSV blocklists for firewalls and SIEMs
- **CLI:** `npx dugganusa-cli` · **MCP server:** listed in the official MCP Registry as `io.github.pduggusa/dugganusa-threat-intel`

## Tools

| Repo | What it does |
|---|---|
| [dredd-mcp](https://github.com/pduggusa/dredd-mcp) | Pre-flight security check for MCP servers before an agent calls them |
| [dugganusa-agent-guard](https://github.com/pduggusa/dugganusa-agent-guard) | Finds invisible Unicode prompt injection in CLAUDE.md, .cursorrules, AGENTS.md |
| [dugganusa-edge-shield](https://github.com/pduggusa/dugganusa-edge-shield) | Cloudflare Worker that blocks known-bad traffic at the edge |
| [dugganusa-sentinel](https://github.com/pduggusa/dugganusa-sentinel) | Microsoft Sentinel data connector for the free feed |
| [dugganusa-action](https://github.com/pduggusa/dugganusa-action) | GitHub Action that flags known-bad indicators in pull requests |
| [dugganusa-vscode](https://github.com/pduggusa/dugganusa-vscode) | VS Code extension: threat lookups inside your editor |
| [dugganusa-ietf](https://github.com/pduggusa/dugganusa-ietf) | IETF Hackathon contributions on agentic-attack vectors and MCP verification |

## Read the work

[dugganusa.com](https://www.dugganusa.com) · [LinkedIn](https://www.linkedin.com/in/patrickdugganmn/)

# Patrick Duggan · DugganUSA

[![npm](https://img.shields.io/npm/v/dugganusa-cli?label=npm%20dugganusa-cli)](https://www.npmjs.com/package/dugganusa-cli)
[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code%20Marketplace-published-007ACC)](https://marketplace.visualstudio.com/items?itemName=DugganUSALLC.dugganusa-threat-intel)
[![MCP Registry](https://img.shields.io/badge/MCP%20Registry-listed-blue)](https://registry.modelcontextprotocol.io/v0/servers?search=io.github.pduggusa)
[![IETF Hackathon](https://img.shields.io/badge/IETF%20Hackathon-contributor-lightgrey)](https://github.com/pduggusa/dugganusa-ietf)
[![Free API](https://img.shields.io/badge/free%20API-get%20a%20key-brightgreen)](https://analytics.dugganusa.com/stix/register)

**Threat intelligence you can check.** I build and run [DugganUSA](https://www.dugganusa.com), a threat-intelligence platform built with AI as a working partner: 69M searchable documents across 70 indexes, 1.9M indicator records, a free STIX/TAXII/MISP feed, and research on MCP and AI-agent security. Every claim links to its source, confidence is capped at 95%, and mistakes are corrected in public.

Before this: lead architect for Dell EMC's Azure Stack hybrid cloud, then cloud security architecture at Check Point and Palo Alto Networks.

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

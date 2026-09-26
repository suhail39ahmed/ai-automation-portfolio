# AI & Automations Portfolio Program

**Owner:** Suhail Ahmed — Solution Architect, AI & Automations (Singapore)  
**Goal:** Interview-grade, reusable AI skills / MCP tools / CLIs with honest demos — not empty README marketing.

## Why star these repos / who they're for

Star (and fork) if you are:

- An **Azure AI / DevOps Solution Architect** who needs agent-usable tools, not slideware
- Building **Cursor / MCP / skill** workflows that must stay **offline-demoable** and auditable
- Tired of READMEs that claim "production" without a `make demo` path

Each project is designed so a stranger can clone → `pip install -e .` → `make demo` in under a minute. No fabricated star counts, no secret-filled `.env`, no "trust me it works in prod" claims.

| If you care about… | Start here | Why it's star-worthy |
|--------------------|------------|----------------------|
| Agents citing **your** teaching content | [kc-mcp](https://github.com/suhail39ahmed/kc-mcp) | MCP-shaped Knowledge Center; TF-IDF offline; Cursor `mcp.json` example |
| Red CI → RCA without auto-heal | [ado-pipeline-doctor](https://github.com/suhail39ahmed/ado-pipeline-doctor) | ADO + GHA fixtures → JSON with `human_approval_required` |
| Blocking bad agent traces in CI | [foundry-eval-gate](https://github.com/suhail39ahmed/foundry-eval-gate) | Faithfulness / tool_success / pii_leak → HTML report + non-zero exit |
| Auditable Azure ops tools for agents | [azure-ops-mcp](https://github.com/suhail39ahmed/azure-ops-mcp) | KV compare, ADO diagnose, cost stub; dry-run + audit log |
| Metrics-governed SQL proposals | [lakehouse-insights-skill](https://github.com/suhail39ahmed/lakehouse-insights-skill) | Catalog → SQL; execute only with `--execute` |
| IaC review inside agent loops | [iac-guard-mcp](https://github.com/suhail39ahmed/iac-guard-mcp) | Terraform/Bicep `review_diff`; Checkov optional; MCP server |
| Teaching reel → lab pack | [clip2lab](https://github.com/suhail39ahmed/clip2lab) | Transcript → README + quiz + skill stub, no LLM required |

## Positioning

Enterprise SA who ships **agent-usable tools** on Azure + data platforms: Knowledge Center, pipeline diagnosis, eval gates, ops MCP, lakehouse skills, IaC guardrails, and content→lab automation.

## Projects (build order)

| Phase | Repo | Outcome | Demo |
|------:|------|---------|------|
| 0 | `ai-automation-portfolio` | This roadmap + checklist | Link from profile |
| 1 | `kc-mcp` | MCP over teaching corpus with citations | Tool-call video 60–90s |
| 1 | `ado-pipeline-doctor` | Failed log → RCA + guarded remediations | Red→RCA video |
| 2 | `foundry-eval-gate` | CI eval gate (fixture + optional Foundry) | CI badge + HTML report |
| 2 | `azure-ops-mcp` | KV/ADO/cost tools, dry-run + audit | Terminal GIF |
| 3 | `lakehouse-insights-skill` | Metrics catalog → proposed SQL | GIF + YAML |
| 3 | `iac-guard-mcp` | Diff → policy findings + explain | PR comment shot |
| 3 | `clip2lab` | Transcript → lab pack | Timelapse tree |

## Rules

1. Every repo runs offline with fixtures.  
2. No fabricated production metrics.  
3. Secrets only via env / Key Vault.  
4. README must include what it is **not**.  
5. Ship `assets/architecture.svg` + `docs/DEMO.md` + `make demo`.  
6. MCP repos document Cursor `mcp.json` and optional `mcp` SDK extra.

## Resume narrative (use after demos exist)

- Built a Knowledge Center MCP so coding agents search and cite personal teaching content.  
- Shipped a pipeline doctor skill that turns failed CI/ADO logs into RCA + human-approved remediations.  
- Added an eval gate for AI apps (faithfulness / tool success / PII) runnable in GitHub Actions.  
- Packaged Azure ops workflows as MCP tools with dry-run and audit logging.  
- Published governed lakehouse and IaC guard skills for enterprise AI copilots.  
- Automated teaching→lab generation (`clip2lab`) to scale enablement content.

## Timeline (suggested)

- **Week 1:** Phase 1 (`kc-mcp`, `ado-pipeline-doctor`) + record Loom demos + LinkedIn launch  
- **Week 2:** Phase 2 (`foundry-eval-gate`, `azure-ops-mcp`)  
- **Week 3:** Phase 3 + pin repos + feature on savvysuhail.com  
- **Ongoing:** Replace sample corpus with real Instagram transcripts

## Non-goals

- README-only "agentic swarm" repositories  
- Unverifiable MTTR / "in production" claims  
- ChatGPT-clone UIs without tools

## Repos

| Repo | Description | First command |
|------|-------------|---------------|
| [kc-mcp](https://github.com/suhail39ahmed/kc-mcp) | Knowledge Center MCP tools | `make demo` |
| [ado-pipeline-doctor](https://github.com/suhail39ahmed/ado-pipeline-doctor) | Failed logs → RCA JSON | `make demo` |
| [foundry-eval-gate](https://github.com/suhail39ahmed/foundry-eval-gate) | CI eval gate on traces | `make demo` |
| [azure-ops-mcp](https://github.com/suhail39ahmed/azure-ops-mcp) | KV/ADO/cost tools dry-run | `make demo` |
| [lakehouse-insights-skill](https://github.com/suhail39ahmed/lakehouse-insights-skill) | Catalog → SQL propose | `make demo` |
| [iac-guard-mcp](https://github.com/suhail39ahmed/iac-guard-mcp) | IaC review_diff | `make demo` |
| [clip2lab](https://github.com/suhail39ahmed/clip2lab) | Transcript → lab pack | `make demo` |

## Demo checklist (portfolio)

- [ ] Record Looms for phase-1 repos (scripts in each `docs/DEMO.md`)
- [ ] Pin top 4 repos on GitHub profile
- [ ] Link this roadmap from profile README
- [ ] Feature on savvysuhail.com /projects
- [ ] Publish week-1 LinkedIn post (`docs/linkedin-week1-kc-mcp.md`)

## Profile README suggestion

Add a short section to `suhail39ahmed/suhail39ahmed` (profile README):

```markdown
## AI & Automations Portfolio Program
Interview-grade MCP tools / skills / CLIs with offline fixtures — see [ai-automation-portfolio](https://github.com/suhail39ahmed/ai-automation-portfolio).
```

## Notes

- `foundry-eval-gate`: GitHub Actions YAML lives at `docs/examples/eval-gate.yml` because the OAuth token lacked `workflow` scope to push `.github/workflows/`. Copy into `.github/workflows/` when available.
- All seven project repos run offline with fixtures; no secrets committed.
- MCP servers (`kc-mcp`, `azure-ops-mcp`, `iac-guard-mcp`) use optional `mcp` extra + FastMCP stdio.

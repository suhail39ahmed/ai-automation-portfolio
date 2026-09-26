# AI & Automations Portfolio Program

**Owner:** Suhail Ahmed — Solution Architect, AI & Automations (Singapore)  
**Goal:** Interview-grade, reusable AI skills / MCP tools / CLIs with honest demos — not empty README marketing.

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
5. Ship `assets/` placeholders + DEMO.md for GIF/video.

## Resume narrative (use after demos exist)

- Built a Knowledge Center MCP so coding agents search and cite personal teaching content.  
- Shipped a pipeline doctor skill that turns failed CI/ADO logs into RCA + human-approved remediations.  
- Added an eval gate for AI apps (faithfulness / tool success / PII) runnable in GitHub Actions.  
- Packaged Azure ops workflows as MCP tools with dry-run and audit logging.  
- Published governed lakehouse and IaC guard skills for enterprise AI copilots.  
- Automated teaching→lab generation (`clip2lab`) to scale enablement content.

## Timeline (suggested)

- **Week 1:** Phase 1 (`kc-mcp`, `ado-pipeline-doctor`) + record demos  
- **Week 2:** Phase 2 (`foundry-eval-gate`, `azure-ops-mcp`)  
- **Week 3:** Phase 3 + pin repos + feature on savvysuhail.com  
- **Ongoing:** Replace sample corpus with real Instagram transcripts

## Non-goals

- README-only “agentic swarm” repositories  
- Unverifiable MTTR / “in production” claims  
- ChatGPT-clone UIs without tools


## Repos

| Repo | Description | First command |
|------|-------------|---------------|
| [kc-mcp](https://github.com/suhail39ahmed/kc-mcp) | Knowledge Center MCP-style tools | `python -m kc_mcp.cli topics` |
| [ado-pipeline-doctor](https://github.com/suhail39ahmed/ado-pipeline-doctor) | Failed logs → RCA JSON | `python -m pipeline_doctor.cli fixtures/azure-pipelines/nuget-auth-fail.log` |
| [foundry-eval-gate](https://github.com/suhail39ahmed/foundry-eval-gate) | CI eval gate on traces | `python -m eval_gate.cli` |
| [azure-ops-mcp](https://github.com/suhail39ahmed/azure-ops-mcp) | KV/ADO/cost tools dry-run | `python -m azure_ops_mcp.cli kv-compare fixtures/vaults/dev-vault.json fixtures/vaults/prod-vault.json` |
| [lakehouse-insights-skill](https://github.com/suhail39ahmed/lakehouse-insights-skill) | Catalog → SQL propose | `python -m lakehouse_insights.cli "revenue by region"` |
| [iac-guard-mcp](https://github.com/suhail39ahmed/iac-guard-mcp) | IaC review_diff | `python -m iac_guard.cli fixtures/bad_nsg.tf` |
| [clip2lab](https://github.com/suhail39ahmed/clip2lab) | Transcript → lab pack | `python -m clip2lab.cli examples/one-reel/transcript.txt` |

## Demo checklist (portfolio)

- [ ] Record GIFs for phase-1 repos
- [ ] Pin top 4 repos on GitHub profile
- [ ] Link this roadmap from profile README
- [ ] Feature on savvysuhail.com /projects

## Profile README suggestion

Add a short section to `suhail39ahmed/suhail39ahmed` (profile README):

```markdown
## AI & Automations Portfolio Program
Interview-grade MCP tools / skills / CLIs with offline fixtures — see [ai-automation-portfolio](https://github.com/suhail39ahmed/ai-automation-portfolio).
```

(Parent agent / owner wires the profile README — this repo only suggests the blurb.)

## Notes from scaffolding (2026-09-26)

- `foundry-eval-gate`: GitHub Actions YAML lives at `docs/examples/eval-gate.yml` because the OAuth token lacked `workflow` scope to push `.github/workflows/`. Copy into `.github/workflows/` when available.
- All seven project repos run offline with fixtures; no secrets committed.

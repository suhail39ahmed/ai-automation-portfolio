# LinkedIn post draft — Week 1 launch (`kc-mcp`)

**Status:** Draft only — do not auto-post. Review tone, then publish manually.  
**Suggested media:** 60–90s Loom (script in `kc-mcp/docs/DEMO.md`) + repo link.

---

## Post body (copy/paste)

Most "AI agent" repos I see are either a chat UI or a README with no runnable path.

I wanted the opposite: tools a Solution Architect can hand to Cursor / an MCP host and demo offline in under a minute.

So I open-sourced **kc-mcp** — a Knowledge Center shaped like MCP tools over teaching lesson notes:

- `search_lessons` — keyword / TF-IDF with file citations  
- `get_clip_notes` / `list_topics` / `quiz_me`  
- Optional FastMCP stdio server + Cursor `mcp.json` example  
- `make demo` — no cloud keys, no vector DB bill for the happy path  

It is intentionally **not** a hosted RAG platform. It is the pattern I use when agents need to cite *my* enablement content (Azure AI Foundry, Key Vault ops, Databricks RAG, pipeline failures, MCP secure use).

If you build Azure AI / DevOps platforms and care about adoptable agent tooling:

→ https://github.com/suhail39ahmed/kc-mcp  

Full portfolio roadmap (7 repos, same fixture-first rules):  
https://github.com/suhail39ahmed/ai-automation-portfolio  

Clone it. Run `make demo`. Tell me what corpus you'd plug in first.

#Azure #AI #MCP #DevOps #SolutionArchitecture #OpenSource

---

## Alternate shorter version

Shipped **kc-mcp**: MCP-shaped Knowledge Center tools so coding agents can search and cite teaching notes offline.

`pip install -e .` → `make demo` → Cursor `mcp.json` example in the repo.

Built for Azure AI / DevOps SAs — not a RAG SaaS claim, just a clean pattern.

https://github.com/suhail39ahmed/kc-mcp

---

## Notes for Suhail

- Lead with the problem (unrunnable agent repos), not "excited to announce"
- Pin `kc-mcp` + portfolio on GitHub the same day
- Reply to comments with the next repo (`ado-pipeline-doctor`) rather than soft CTAs
- Do not invent engagement metrics in comments

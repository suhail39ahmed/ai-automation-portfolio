# Video ideas — all 7 product repos

Record on Loom (or similar), 60–90s each. Fixture-only. No fake metrics on screen.

For each repo: Loom outline, **3 screenshot frames**, and a **LinkedIn first-comment** with `make demo`.

---

## 1) kc-mcp (flagship)

**Outline:** problem (agents forget teaching notes) → `--format text topics` → search with cite → quiz → outro repo URL.  
Full timed script: [kc-mcp/docs/DEMO.md](https://github.com/suhail39ahmed/kc-mcp/blob/main/docs/DEMO.md).

**3 frames**

1. Topics list (5 fixture lessons)  
2. Search hit with `cite: key-vault-ops.md` + score  
3. Quiz prompts for MCP secure use  

**LinkedIn first-comment**

```
Clone + demo (offline fixtures):

git clone https://github.com/suhail39ahmed/kc-mcp.git
cd kc-mcp && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo

Screenshot-friendly: python -m kc_mcp --format text topics
```

---

## 2) ado-pipeline-doctor

**Outline:** red build pain → NuGet 401 fixture text RCA → call out `human_approval_required` → GHA pytest fixture → outro.  
Script: [ado-pipeline-doctor/docs/DEMO.md](https://github.com/suhail39ahmed/ado-pipeline-doctor/blob/main/docs/DEMO.md).

**3 frames**

1. Category `auth` + NuGet 401 summary  
2. Remediations with approval flags  
3. GHA pytest fixture summary  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/ado-pipeline-doctor.git
cd ado-pipeline-doctor && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo

Try: python -m pipeline_doctor --format text fixtures/azure-pipelines/nuget-auth-fail.log
```

---

## 3) foundry-eval-gate

**Outline:** why CI should fail bad agent traces → `make demo` → open `reports/report.html` → point at intentional fixture fails → outro.

**3 frames**

1. Terminal running `make demo` / report paths  
2. HTML report summary (faithfulness / tool_success / pii_leak)  
3. Non-zero exit or failing fixture row  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/foundry-eval-gate.git
cd foundry-eval-gate && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo
# open reports/report.html
```

---

## 4) azure-ops-mcp

**Outline:** agent ops need audit trails → kv-compare fixtures → ado-diagnose → show `audit.log` append → outro.

**3 frames**

1. kv-compare JSON/text output  
2. ado-diagnose result  
3. `audit.log` lines (dry-run)  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/azure-ops-mcp.git
cd azure-ops-mcp && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo
# then: cat audit.log
```

---

## 5) lakehouse-insights-skill

**Outline:** unconstrained SQL is scary → propose from metrics catalog → show SQL only → `--execute` sandbox → outro.

**3 frames**

1. Propose SQL for "revenue by region"  
2. Catalog / metric names visible  
3. `--execute` sandbox result  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/lakehouse-insights-skill.git
cd lakehouse-insights-skill && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo
```

---

## 6) iac-guard-mcp

**Outline:** agents editing IaC need review_diff → bad NSG Terraform findings → Bicep fixture → structured JSON → outro.

**3 frames**

1. Terraform findings list  
2. Bicep findings  
3. JSON snippet with rule ids  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/iac-guard-mcp.git
cd iac-guard-mcp && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo
```

---

## 7) clip2lab

**Outline:** reel transcript → lab pack without an LLM → show `labs/one-reel/` tree (README, quiz, skill) → outro.

**3 frames**

1. Input transcript snippet  
2. Generated `labs/one-reel/README.md`  
3. `quiz.md` / directory tree  

**LinkedIn first-comment**

```
git clone https://github.com/suhail39ahmed/clip2lab.git
cd clip2lab && python -m venv .venv && source .venv/bin/activate
pip install -e . && make demo
# then: ls labs/one-reel/
```

---

## Production tips (all videos)

- Dark terminal, 16–18pt font, no secrets  
- State "offline fixtures" verbally once  
- End card: `github.com/suhail39ahmed/<repo>`  
- Do **not** auto-post — review drafts manually (see LinkedIn week1 note)

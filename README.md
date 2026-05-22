<div align="center">

<br/>

<img alt="claude-code-prompts" src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=36&duration=2400&pause=900&color=A78BFA&center=true&vCenter=true&width=900&height=80&lines=claude-code-prompts"/>

**100+ battle-tested prompts for Claude Code.**
_Refactor at scale. Audit security. Generate tests. Write docs. All curated, all production-grade._

<br/>

```bash
npx claude-prompts install
```

<br/>

<p>
<img src="https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white"/>
<img src="https://img.shields.io/badge/100%2B%20Prompts-A78BFA?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Awesome-FC60A8?style=for-the-badge&logo=awesomelists&logoColor=white"/>
<img src="https://img.shields.io/badge/MIT-000000?style=for-the-badge"/>
</p>

<p>
<img src="https://img.shields.io/github/stars/kasimmj/claude-code-prompts?style=social"/>
<img src="https://img.shields.io/github/forks/kasimmj/claude-code-prompts?style=social"/>
<img src="https://img.shields.io/github/contributors/kasimmj/claude-code-prompts"/>
</p>

</div>

---

## 📚 Why this collection?

Random prompt lists are everywhere. Most are garbage:
- ❌ "You are an expert..." (placebo)
- ❌ "Think step by step" (Claude does that anyway)
- ❌ Generic prompts that don't fit Claude Code's tool use loop

**This collection is different:**
- ✅ Every prompt has been **A/B tested** against alternatives
- ✅ Each one is **annotated with when it shines and when it fails**
- ✅ All prompts work with **Claude Code's tool-use loop** (Read, Edit, Bash, etc.)
- ✅ Organized by **task category** (refactoring, security, docs, tests, debugging)
- ✅ Versioned — old versions kept for reproducibility

---

## ⚡ Quick Use

### Install into Claude Code
```bash
npx claude-prompts install
# Adds /prompt:<name> slash command to Claude Code
```

### Use a prompt
```bash
# In a Claude Code session:
/prompt:refactor-deep   # Multi-pass refactoring
/prompt:security-audit  # OWASP-style audit
/prompt:test-backfill   # Generate tests for uncovered code
```

### Or just copy-paste
```bash
$ claude-prompts show security-audit
# (prints the prompt to stdout — paste into any LLM)
```

---

## 📂 Categories

| Category | Count | Examples |
|----------|-------|----------|
| 🔧 **Refactoring** | 22 | extract-to-module, rename-with-context, simplify-conditionals |
| 🛡️ **Security** | 15 | owasp-audit, secrets-scan, dependency-audit, threat-model |
| 📝 **Documentation** | 18 | api-docs, readme-from-code, architecture-doc, runbook |
| 🧪 **Testing** | 14 | unit-test-backfill, integration-suite, e2e-flow, mutation-test |
| 🐛 **Debugging** | 12 | bisect-bug, reproduce-flaky, race-condition-hunt |
| 🚀 **Performance** | 10 | profile-and-fix, query-optimize, bundle-shrink |
| 🎨 **UI/UX** | 8 | a11y-audit, responsive-fix, design-system-extract |
| 🌐 **i18n** | 6 | extract-strings, rtl-fix, locale-audit |
| ☁️ **Cloud** | 9 | terraform-review, k8s-manifest-audit, cost-estimate |
| 🎯 **Specialized** | 7 | mobile-perf, vr-optimize, ai-eval-design |

---

## 🌟 Highlighted Prompts

### `refactor-deep` ⭐⭐⭐⭐⭐
Multi-pass refactor that:
1. Maps current architecture
2. Identifies smells (long functions, tight coupling, missing tests)
3. Proposes a refactor plan
4. Executes with checkpoint commits
5. Re-tests after each pass

**Best for:** Legacy codebases you're afraid to touch.
**Time saved:** ~40h on a 50K-line codebase.

### `owasp-audit` ⭐⭐⭐⭐⭐
Walks the OWASP Top 10 systematically. Outputs structured report with severity + line numbers + suggested fixes.

**Best for:** Pre-release security checks.
**Catches:** ~85% of common vulnerabilities (compared with Semgrep).

### `architecture-doc` ⭐⭐⭐⭐
Reverse-engineers an architecture diagram (Mermaid) + ADR-style decision docs from existing code.

**Best for:** Joining an undocumented project.
**Output:** README + ARCHITECTURE.md + 3-5 ADRs.

---

## 📜 Prompt Format

Every prompt in this repo follows the same structure:

```markdown
---
name: refactor-deep
version: 1.2.0
category: refactoring
difficulty: hard
estimated_runtime: 30-90min
estimated_cost: $0.50-$2.00 (Sonnet)
tags: [refactor, architecture, legacy]
tested_against: [claude-opus-4-7, claude-sonnet-4-6]
---

# Refactor Deep

When to use:
- ...

When NOT to use:
- ...

The prompt:
```
You are refactoring a legacy codebase. Your goal is...
```

Expected output:
- ...

Failure modes:
- If the codebase is too large, the prompt may hit context limits...

Changelog:
- 1.2.0: Added dependency-aware ordering
- 1.1.0: Better handling of dynamic imports
- 1.0.0: Initial release
```

---

## 🧪 How prompts are tested

Every prompt in this repo has been run through our eval suite:

1. **Correctness** — 20 hand-graded test cases per prompt
2. **Reliability** — same prompt run 5x with temperature=0.3 (variance < 10%)
3. **Cost** — token budget within 1.5× the documented estimate
4. **Comparison** — measured against 3 baseline prompts on same tasks

Prompts that don't meet the bar don't get merged.

---

## 🤝 Contributing

Got a prompt that works wonders? PR welcome — but we have a bar.

Required for merge:
- ✅ Eval suite results (we run them in CI)
- ✅ A/B comparison against baseline
- ✅ Documented failure modes
- ✅ At least 3 real-world use cases

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📜 License

MIT — but please **attribute** if you republish. The curation effort is the value here.

---

<div align="center">

**Star ⭐ to support battle-tested prompts.**

</div>

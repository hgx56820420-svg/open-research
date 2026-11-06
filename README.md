# Open Research (`open-research`)

English | [简体中文](./README.zh-CN.md)

A **self-contained, domain-agnostic, cross-lingual, and date-aware** Agent Skill for deep research.

`open-research` unifies **broad multi-platform retrieval**, **GitHub & industry investigation**, and **rigorous source-freshness auditing** into a single workflow—built for academic literature reviews, global market intelligence, open-source evaluations, and everyday complex fact-checking.

---

## Why `open-research`?

Standard AI web search often suffers from four blind spots:
1. **Single-language echo chambers** — searching only in the prompt's phrasing and missing primary sources in other languages.
2. **Confirmation bias** — retrieving top SEO results without actively hunting for retractions, breaking changes, or criticisms.
3. **Syndication illusions** — treating five blogs summarizing the same press release as "five independent sources".
4. **Time blindness** — citing outdated API docs, abandoned GitHub repos, or superseded studies as current truth.

`open-research` enforces a structured discipline to eliminate all four.

---

## Key Capabilities

- **Any Domain, Four Core Modes**:
  - **Academic & Paper Writing**: Trace primary papers, replications, retractions, benchmark drift, and methodological debates.
  - **Industry & Policy Intelligence**: Cross-regional comparisons (North America, Europe, Asia/China, etc.), regulatory filings, and market metrics.
  - **GitHub & Technical Auditing**: Look beyond stars and last commit—inspect releases, dependency manifests, issue responsiveness, compatibility, and licenses.
  - **Everyday Deep Search**: Multi-angle verification for practical decisions, historical questions, and public controversies.
- **Three Proportional Depth Tiers**:
  - `Quick` (3–5 searches, 2+ source types)
  - `Standard` *(default)* (8–15 searches, 4+ source types, bilingual/multilingual pass)
  - `Deep` (6+ source types, sub-question decomposition, parallel subagents, atomic claim check)
- **4-Way Query Expansion**: Multilingual/bilingual terminology, domain jargon synonyms, perspective shifts, and mandatory adversarial counter-queries (`limitations`, `criticism`, `retractions`, `archived`).
- **Built-in Source Freshness Engine**: Separates *Event Date*, *Published/Updated Date*, and *Access Date*, assigning explicit `[Current]`, `[Aging]`, `[Stale]`, or `[Unknown]` labels using domain-specific validity windows.
- **Epistemic Hygiene**: Separates `[Fact]`, `[Interpretation]`, and `[Recommendation / Forecast]`, flags `[Single Source]` and `[Vendor/Commercial Interest]`, and quarantines unconfirmed social media posts under **Unverified Leads**.
- **Prompt-Injection Resilient & Scannable**: Treats all web/repo content as untrusted data and delivers Bottom-Line-Up-Front (BLUF) summaries in the user's language while preserving original-language source titles.

---

## Workflow Overview

```text
User Query
   │
   ▼
1. Frame & Tier Selection (Quick / Standard / Deep)
   │
   ▼
2. Multi-Source & Multilingual Retrieval (8 Source Categories + Multi-Region)
   │
   ├──► Adversarial Pass (Criticism / Retractions / Breaking Changes)
   └──► GitHub Audit (Releases / Dependencies / Maintenance / License)
   │
   ▼
3. Source Freshness Audit (Event vs. Update vs. Access Date → Current/Aging/Stale/Unknown)
   │
   ▼
4. Cross-Verification (De-duplicate Syndication + Separate Fact / Interpretation / Recommendation)
   │
   ▼
5. Scannable Deliverable ("As of YYYY-MM-DD" + Findings + Blind Spots + Source Register)
```

---

## Installation

`open-research` follows the open `SKILL.md` standard and has **zero external skill dependencies**.

### Codex / Claude Code / Comate / Cursor Skills Directory

Clone this repository or copy `SKILL.md` into your agent's skills folder:

```bash
# Personal skill (Codex example)
mkdir -p ~/.codex/skills/open-research
cp SKILL.md ~/.codex/skills/open-research/SKILL.md

# Or Comate personal skill
mkdir -p ~/.comate/skills/open-research
cp SKILL.md ~/.comate/skills/open-research/SKILL.md

# Or Claude Code personal skill
mkdir -p ~/.claude/skills/open-research
cp SKILL.md ~/.claude/skills/open-research/SKILL.md
```

---

## Example Prompts

- **Academic / Literature Review**:
  > *"I'm writing a review paper on microplastics and human cardiovascular risk. Survey the key clinical findings from 2024–2026, areas of consensus, and major methodological critiques."*
- **Global Industry Research**:
  > *"Compare commercialization progress, government subsidies, and cost bottlenecks for sodium-ion grid storage across the US, EU, China, and Japan."*
- **Open-Source & Everyday Tooling**:
  > *"I want to self-host 50,000 family photos locally with facial recognition and zero cloud uploads. Compare the most actively maintained open-source options on GitHub, including recent breaking changes and hardware needs."*
- **Quick Fact-Check**:
  > *"Quick check: what is the current visa-free transit window in China for European travelers, and when was the policy last updated?"*

---

## Repository Structure

```text
open-research/
├── SKILL.md          # Complete self-contained skill specification
├── README.md         # English documentation
├── README.zh-CN.md   # Chinese documentation
└── LICENSE           # MIT License
```

---

## License

Released under the [MIT License](./LICENSE).

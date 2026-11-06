# Open Research (`open-research`)

English | [简体中文](./README.zh-CN.md)

**A specialized Agent Skill that teaches AI how to search the web, verify sources, and synthesize structured findings.**

Instead of letting your AI assistant do a shallow one-shot search and summarize whatever shows up first, `open-research` turns your AI (Claude Code, Codex, Comate, Cursor, etc.) into a disciplined researcher—capable of **searching across platforms and languages, auditing GitHub projects and time-sensitivity, cross-checking claims, and organizing complex information into clean, decision-ready briefs**.

---

## What Is This?

`open-research` is an **AI Search & Synthesis Skill (`SKILL.md`)**. Once installed in your AI coding or research agent, the AI automatically follows a rigorous workflow whenever you ask it to search, investigate, or organize information on any topic:

- **Write Academic Papers & Literature Reviews**: Directs the AI to search academic databases, trace primary citations, check for retractions or failed replications, and organize consensus vs. methodological debates.
- **Conduct Industry & Market Research**: Guides the AI to gather and structure policies, filings, and market data across multiple regions (North America, Europe, Asia/China, etc.).
- **Evaluate GitHub Repos & Tech Tools**: Stops the AI from blindly trusting GitHub star counts—forcing it to inspect latest releases, dependency compatibility, issue maintenance, and licenses.
- **Everyday Deep Search & Fact-Checking**: Helps the AI search multiple angles and languages for daily questions, product/tool comparisons, and public controversies, then organize the pros, cons, and blind spots clearly.

---

## Why Does AI Need a Search & Synthesis Skill?

Left on its own, default AI web search usually makes four mistakes:
1. **Single-language echo chambers** — searching only in the phrasing you typed and missing crucial primary sources in English or local languages.
2. **Confirmation bias** — summarizing the top 3 SEO results without actively searching for criticisms, limitations, retractions, or breaking changes.
3. **Syndication illusions** — treating five blogs that copied the same press release as "five independent sources".
4. **Time blindness** — citing outdated API docs, abandoned GitHub repos, or superseded studies as if they were still true today.

`open-research` fuses **broad multi-platform retrieval**, **GitHub & industry investigation**, and **source-freshness auditing** into one self-contained ruleset so the AI searches deeper and organizes cleaner.

---

## How It Teaches AI to Search & Organize

### 1. Proportional Search Depth (3 Tiers)
The AI automatically picks (and announces) the right search intensity:
- **`Quick`** (`3–5 searches`, `2+ source types`): Fast lookup and structured summary for simple questions.
- **`Standard` [Default]** (`8–15 searches`, `4+ source types`): Bilingual/multilingual search + independent cross-verification.
- **`Deep`** (`6+ source types`, parallel sub-agents): Decomposes big topics into sub-questions, searches in parallel, and verifies every atomic claim.

### 2. 4-Way Query Expansion
For every topic, the AI expands its search queries across four dimensions:
- **Bilingual / Multilingual**: Native English domain terms + the user's or target region's language.
- **Synonyms & Jargon**: Everyday phrasing paired with technical, academic, or legal terms.
- **Perspective Shifts**: Definitions, how-to implementations, case studies, and quantitative data.
- **Adversarial Counter-Search**: Actively searches `limitations`, `criticism`, `retractions`, `breaking changes`, `archived`, and `vs`.

### 3. Built-in Time & Freshness Auditing
The AI tracks **Event Date**, **Published/Updated Date**, and **Access Date** separately, tagging every finding as:
- `[Current]` — Up-to-date and within the domain's validity window.
- `[Aging]` — Approaching expiration; usable with date caveats.
- `[Stale]` — Outdated or superseded by newer releases/policies/studies.
- `[Unknown]` — Missing dates or unverified compatibility.

### 4. Structured, High-Readability Organization
The AI organizes raw search results into a clean, scannable report:
- **Bottom-Line Up Front (`As of YYYY-MM-DD`)**: Direct conclusion first.
- **Tagged Takeaways**: Every point is clearly labeled as `[Fact]`, `[Interpretation]`, or `[Recommendation]`, plus flags for `[Single Source]` or `[Vendor/Commercial Interest]`.
- **Controversies & Blind Spots**: Explicitly lists conflicting views, unsearched regions, and uncorroborated social media leads (**Unverified Leads**).
- **Scannable Formatting**: Short paragraphs, compact tables (max 4–5 rows per table), and preserved original-language titles with direct links.

---

## Workflow Overview

```text
Your Question
   │
   ▼
1. AI Selects Search Tier (Quick / Standard / Deep)
   │
   ▼
2. AI Searches Across Platforms & Languages (8 Source Categories + Multi-Region)
   │
   ├──► Adversarial Search (Criticism / Retractions / Breaking Changes)
   └──► GitHub Audit (Releases / Dependencies / Maintenance / License)
   │
   ▼
3. AI Audits Source Freshness (Event vs. Update vs. Access Date → Current/Aging/Stale/Unknown)
   │
   ▼
4. AI Cross-Verifies & De-duplicates (Trace Primary Sources + Tag Fact / Interpretation / Recommendation)
   │
   ▼
5. AI Organizes Final Brief ("As of YYYY-MM-DD" + Structured Findings + Blind Spots + Source Register)
```

---

## Installation

`open-research` uses the standard `SKILL.md` format and has **zero external dependencies**. Copy `SKILL.md` into your AI agent's skills directory:

```bash
# Codex
mkdir -p ~/.codex/skills/open-research
cp SKILL.md ~/.codex/skills/open-research/SKILL.md

# Comate
mkdir -p ~/.comate/skills/open-research
cp SKILL.md ~/.comate/skills/open-research/SKILL.md

# Claude Code
mkdir -p ~/.claude/skills/open-research
cp SKILL.md ~/.claude/skills/open-research/SKILL.md
```

---

## Example Prompts

- **Academic / Paper Writing**:
  > *"I'm writing a review paper on microplastics and human cardiovascular risk. Search and organize the key clinical findings from 2024–2026, areas of consensus, and major methodological critiques."*
- **Global Industry Research**:
  > *"Search and compare commercialization progress, government subsidies, and cost bottlenecks for sodium-ion grid storage across the US, EU, China, and Japan."*
- **Open-Source & Everyday Tooling**:
  > *"I want to self-host 50,000 family photos locally with facial recognition and zero cloud uploads. Search and organize a comparison of the most actively maintained open-source options on GitHub, including recent breaking changes and hardware needs."*
- **Quick Fact-Check**:
  > *"Quick check: what is the current visa-free transit window in China for European travelers, and when was the policy last updated?"*

---

## License

Released under the [MIT License](./LICENSE).

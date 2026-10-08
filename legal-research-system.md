---
name: legal-research-system
description: Evidence-first Iranian legal research workflow: question framing, primary-source hierarchy, legislative history, case law, doctrine, claim-evidence mapping, adversarial review, and final citation audit.
version: "1.0.0"
platforms:
  - hermes-cli
metadata:
  tags:
    - iranian-law
    - legal-research
    - evidence
    - citations
    - legislative-history
  category: research
---

# Iranian Legal Research System

## Purpose
Run a reproducible, evidence-first workflow for Iranian legal research. Do not jump directly to substantive conclusions.

## Mandatory pipeline
1. **Question lock** — write one precise main question and numbered subquestions.
2. **Scope lock** — identify date/version, jurisdiction, legal domain, and disputed terms.
3. **Source hierarchy**
   - Primary: official law/regulation text, official parliamentary proceedings, official court decisions.
   - Secondary authoritative: Supreme Court precedents, official advisory opinions, recognized legal databases.
   - Tertiary: doctrine, books/articles, reputable secondary sources.
   - Web pages are discovery aids unless they reproduce a verifiable primary source.
4. **Source acquisition** — search broadly, then verify the original/primary source and exact locator.
5. **Evidence extraction** — record exact article/section/page/session/date and distinguish quotation from paraphrase.
6. **Claim ledger** — every material claim gets an ID and one of: LAW, LEGISLATIVE_INTENT, CASE_LAW, DOCTRINE, FACT, INFERENCE.
7. **Evidence matrix** — map each claim to sources, locator, confidence, and unresolved questions.
8. **Adversarial analysis** — construct the strongest argument against the provisional conclusion before accepting it.
9. **Synthesis** — separate: what the text says; what the legislature intended; what courts held; what doctrine argues; what is inferred.
10. **Final audit** — no important claim without a source; no inference presented as law; conflicts are logged; dates and amendments are checked.

## Iranian-law special rules
- Never equate «حق کسب و پیشه و تجارت» with «سرقفلی» without source-specific support.
- For legislation, distinguish تصویب، ابلاغ، انتشار، اصلاح، نسخ and آیین‌نامه پیشنهادی versus آیین‌نامه مصوب.
- For parliamentary history, identify مجلس، دوره، جلسه، تاریخ، شور اول/دوم and the exact report or debate.
- For case law, identify court/branch, decision number/date, and whether the decision is binding, advisory, or merely persuasive.
- For doctrine, name the author/work/edition/page where possible.
- If evidence is incomplete, say «نیازمند بررسی بیشتر» rather than filling the gap.

## Required project artifacts
Create/update:
- research_question.md
- source_manifest.csv
- claims.csv
- evidence_matrix.csv
- search_ledger.md
- analysis.md
- final_review.md

## Completion gate
Research is NOT complete until:
- the main question is answered with an evidence-backed provisional conclusion;
- all major claims are mapped to sources;
- contrary evidence has been searched;
- primary-source gaps are explicitly listed;
- final_review.md records PASS or OPEN ITEMS.

## Default answer format
1. What was checked.
2. What is established.
3. What remains uncertain.
4. One clear next action.

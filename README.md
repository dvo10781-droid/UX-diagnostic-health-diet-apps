# UX Diagnostic — Diet Apps & Asian Caregivers
**Noom + BetterMe · Bias Audit from a Vietnamese Night-Shift Mother**
Clinical AI Quality Portfolio · Võ Ngọc Dung (DixieV) · 2026

**Live case study →** [dvo10781-droid.github.io/UX-diagnostic-health-diet-apps](https://dvo10781-droid.github.io/UX-diagnostic-health-diet-apps)

> **v2 — March 23, 2026:** Added Failure 06 (The Unencumbered Individual Assumption / Implicit Bias). Marketing vs. Reality table. Restructured into 7 sections. 4 bias types now documented. New title block, methods section, next steps, and version history.

---

## Summary

I used to think I was just "failing" every diet app I tried. Then I learned enough about UX and Responsible AI to ask a different question: **what if the system is failing users like me?**

This case study is a UX and bias diagnostic of two commercial diet apps (Noom and BetterMe) based on my own use as a Vietnamese woman in her 40s, working night shifts and cooking warm food for a family on a tight budget. Using Google-style fairness and bias concepts, I identify six systemic failures — including selection bias, reporting bias, group attribution bias, and one critical implicit bias I call the **"Unencumbered Individual Assumption."**

I am not building an app here. I am treating existing apps as "black-box" AI-adjacent systems: testing their assumptions, documenting where they misread caregiver lives as non-compliance, and translating those findings into design principles and clinical AI quality engineering skills.

---

## Document Structure

| Section | Content |
|---------|---------|
| 01 — Context & Methods | Who I am, what this is and is not, method in 5 steps |
| 02 — Bias Framework | Four bias types from Google Responsible AI for Developers |
| 03 — UX Diagnosis | Six failure categories with screenshots and root cause analysis |
| 04 — Marketing vs. Reality | App claims measured against observed behavior |
| 05 — Design Principles | Seven principles derived from the failures |
| 06 — Clinical AI QE Skill Map | Work done here → QE skill → clinical AI context |
| 07 — Reflection & Next Steps | Personal reflection + v3/v4 roadmap + version history |

---

## What This Is — and Is Not

**This is:**
- A personal but structured UX diagnostic of two live apps, from the perspective of a non-default user
- A bias audit using Google Responsible AI fairness and bias concepts
- A first portfolio project to build skills toward AI quality and safety roles in healthcare

**This is not:**
- A new app concept or redesign proposal
- A randomized study with outcomes data
- A claim that Noom or BetterMe are "bad" products overall
- A peer-reviewed study — personal observational audit, honestly stated

---

## Four Bias Types Identified

Using the Google Responsible AI for Developers framework:

**Selection Bias** — Apps were optimized for users who succeeded with Western eating patterns, conventional schedules, and standard household structures. The non-default user is invisible in the training data.

**Reporting Bias** — Daily streaks, precise individual logging, and standard sleep patterns are rewarded. Night-shift schedules and shared dishes appear as "no data" or compliance failures.

**Group Attribution Bias** — Even when cultural preferences are collected (Vietnamese, Thai, Japanese cuisines), the same Western defaults are delivered. Collecting data is not the same as using it.

**Implicit Bias** *(added v2)* — The system encodes who the "normal" user is through default choices, visual language, and what needs no explanation. No rule says "not for caregivers." The bias lives in who was never in the room when the model was built.

---

## Six Failure Categories

| # | Failure | Bias Type | Severity |
|---|---------|-----------|----------|
| 01 | Individual Portion Assumption — meal plans ignore stated cuisine preferences | Group Attribution + Selection | Critical |
| 02 | Privileged Resource Assumption — stacked payments, $270 plans, GLP-1 drug questions | Selection + Reporting | High |
| 03 | Precision-as-Virtue + Schedule Universality — 8h sleep goal for a night shift worker | Selection + Reporting | High |
| 04 | Food Classification vs. Nutrition Science — rice is "yellow" but USDA puts whole grains at its base | Selection + Group Attribution | High |
| 05 | Single-Person Cooking + Western Visual Defaults | Selection + Group Attribution | Medium |
| 06 | The Unencumbered Individual Assumption ★ v2 | **Implicit Bias** + Selection | Critical |

---

## Failure 06 — The Deepest Finding

The apps behave as if the user is one person managing her own time, body, and food choices.

A mother is not that person. She is a system.

Her food is the family's food. Her time is the family's time. Her meal decisions are not personal preferences — they are how the household runs.

*"Love yourself first"* is good advice. But it assumes the self is available to be loved first. For a mother running a household system, the self comes last — not from low self-worth, but because the system she runs has no pause button.

That absence — the fact that she was never in the room when the model was built — is Implicit Bias. Not a rule. Not a decision. Just: she didn't exist in the design.

**The clinical AI connection:** Mental health AI tools trained on individualist behavioral markers misread caregiver lives as pathology. Waking at 2am is a depression signal in the training data. For a Vietnamese mother on night shift, it is Tuesday. The system reads her life as disorder because it was built to read a different life as normal.

---

## Key Evidence

**The core Group Attribution Bias argument:**
Noom onboarding → I select Vietnamese, Thai, Japanese → Week 1 meal plan: Pita Party Pizzas, Mango Chicken Salad with Couscous, Turkey Cheddar Tacos.

**The food pyramid contradiction:**
Noom classifies rice as a yellow (caution) food. The USDA Food Pyramid places whole grains at its base. The food I cook at home from scratch is penalized by a classification system built for a different kitchen.

**The stacked payment problem:**
BetterMe charges a subscription fee plus $14.99 + $7.99 + $9.99 as separate in-app challenge purchases. I track cancellation dates on Google Calendar. That cognitive and financial burden is a design choice.

**The sleep tracking failure:**
BetterMe default sleep goal: 8 hours. Saturday March 21: 0% of goal. "We need more data." The data is: I was working a night shift. Reporting Bias reads my schedule as failure.

**The marketing vs. reality gap:**
Every public review describes these apps as "personalized," "customized," and "adapts to your needs." The audit documents the gap between those claims and what the system actually delivered to a non-default user. The non-default user who drops out is not in the review data — she is the selection bias.

---

## Apps Audited

- **Noom** — trial account, March 2026
- **BetterMe** — trial account, March 2026
- **Simple** — excluded. Requires payment before any trial access. This is itself a Failure 02 finding.

---

## Clinical AI QE Skills Demonstrated

| Work Done Here | Clinical AI QE Skill | In a Clinical Context |
|---|---|---|
| Classified 6 failures using 4 bias types including implicit bias | Bias taxonomy, issue labeling, implicit bias detection | Categorizing model issues as data imbalance, label noise, or structural bias |
| Named "Unencumbered Individual Assumption" as Failure 06 | Structural bias identification for caregivers and minorities | Reviewing models so caregiver behavior is not misread as depression or non-adherence |
| Compared Noom food categories to USDA dietary guidance | Ground-truth validation against established standards | Checking AI recommendations against clinical guidelines or lab reference ranges |
| Built marketing vs. reality table — claims tested against observed behavior | Specification and requirements compliance testing | Verifying SaMD outputs against labeling, indications, and IFU |
| Flagged uncited statistics — separated observation from claims requiring citation | Evidence integrity and audit-ready documentation | Writing bias reports regulators can trace from claim → data → evidence |
| Derived 7 design principles from six failure patterns | Risk-informed mitigation and requirement feedback | Translating failure patterns into new test cases and design requirements |

---

## Why This Matters Beyond UX

The same bias types that make a diet app unfriendly to Asian caregivers make clinical AI systems unreliable for patients who don't match the training population.

When a clinical AI system produces different outputs for Asian patients because its training data was predominantly Western, that is selection bias. When it measures adherence by metrics that don't account for cultural dietary patterns, that is reporting bias. When it collects demographic data but doesn't change its recommendations, that is group attribution bias. When it assumes every user is an unencumbered individual with an autonomous self — and misreads a caregiver's life as disorder — that is implicit bias.

**The stakes in clinical AI are higher. The methodology is the same.**

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1 | March 22, 2026 | Initial publication. 5 failure categories. 3 bias types. |
| v2 | March 23, 2026 | Failure 06: Unencumbered Individual Assumption (Implicit Bias). Marketing vs. Reality table. Restructured into 7 sections. New title block, methods, next steps, version history. 4 bias types. P7 principle added. |
| v3 — planned | Upcoming | NIH/PubMed citations. Peer-reviewed sources for implicit bias in wellness AI. Second user observation. |
| v4 — planned | Upcoming | Clinical AI tool audit applying same framework. AlterMe DNA-based platform analysis. |

---

## About the Author

I'm **Võ Ngọc Dung (DixieV)** — medical interpreter (5 years), former Chevron/SLB energy professional (10 years), Geoscience MSc from the University of Adelaide, and frontend developer in training.

I hold a certificate in Generative AI in Healthcare (University of Illinois / Coursera) and have completed Google's Responsible AI for Developers course. I'm transitioning into **Clinical AI Quality Engineering** — the role that evaluates whether AI systems are safe, fair, and accurate before they reach patients.

**Connect:**
[LinkedIn](https://www.linkedin.com/in/dung-vo-25963376/) · [GitHub](https://github.com/dvo10781-droid) · [Live Case Study](https://dvo10781-droid.github.io/UX-diagnostic-health-diet-apps)

---

## Project Status

- [x] Diagnostic framework complete — 7 sections
- [x] Six failure categories with bias classification
- [x] Four bias types documented including Implicit Bias (v2)
- [x] Live screenshots — Noom and BetterMe (March 2026)
- [x] Food pyramid comparison — documentable factual claim
- [x] Marketing vs. reality comparison table (v2)
- [x] Mothers as Systems reflection (v2)
- [x] Clinical AI QE skill map — 6 rows with clinical context
- [x] Google Responsible AI framework applied
- [x] Version history and next steps documented
- [ ] Lactase intolerance citation (NIH/NCBI) — v3
- [ ] Peer-reviewed implicit bias sources — v3
- [ ] Second user observation — v3
- [ ] Clinical AI tool audit — v4
- [ ] AlterMe DNA-based platform analysis — v4

---

*v2 · March 2026 · Screenshots used for educational and analytical purposes.*

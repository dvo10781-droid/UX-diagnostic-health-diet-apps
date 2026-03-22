# UX Diagnostic: Why Diet & Cooking Apps Feel Unfriendly to Asian Users
 
**Live case study →** [View the full audit](https://dvo10781-droid.github.io/UX-diagnostic-health-diet-apps)
> **This is a portfolio case study, not a code repository.**  
> GitHub is used here as a professional documentation platform — the same way  
> designers, researchers, and clinical AI practitioners publish structured work.  
> No coding background needed to read this.
---

> **v2 — March 2026:** Added Failure 06 (The Unencumbered Individual Assumption / Implicit Bias), Marketing vs. Reality comparison table, and Mothers as Systems reflection. Four bias types now documented.

---

## The Origin

I've tried every major diet app. I always dropped out.

For a long time I thought it was a discipline problem. Then I started asking a different question: *what if the apps are the problem?*

I'm a Vietnamese woman in my forties. I work from home. I cook warm food — rice, soups, shared dishes — for my whole family on a tight budget. I enjoy all kinds of food. But eating a cold salad as a main meal? It is cold, it is dry, and it does not fill a family.

Every app I tried kept asking me to track food that wasn't in its database, follow meal plans that ignored my stated cuisine preferences, and log portions from a pot that four people ate from. Noom asked me which cuisines I eat. I said Vietnamese, Thai, Japanese. It served me Pita Party Pizzas and Mango Chicken Salad with Couscous on Day 1.

That's not a localization gap. That's Group Attribution Bias — the system collected my preference data and then ignored it completely.

---

## What This Is

A structured **UX bias audit** of Noom and BetterMe — two leading health apps — using the **Google Responsible AI for Developers** bias classification framework.

This is not a redesign proposal. It is a diagnostic: six failure categories, each classified by bias type, traced to a root system assumption, and documented with live screenshots from my own trial sessions (March 2026).

---

## Bias Types Identified

**Selection Bias** — Apps were optimized for users who succeeded with Western eating patterns, conventional schedules, and standard household structures. The non-default user is invisible in the training data.

**Reporting Bias** — Daily streaks, precise individual logging, and standard sleep patterns are rewarded. Night-shift schedules and shared dishes appear as "no data" or compliance failures.

**Group Attribution Bias** — Even when cultural preferences are collected (Vietnamese, Thai, Japanese cuisines), the same Western defaults are delivered. Collecting data is not the same as using it.

**Implicit Bias** *(added v2)* — The system encodes assumptions about who the user is through default choices, visual language, and what needs no explanation. No rule says "Western users only." The bias lives in what the system treats as normal — and who was never in the room when the model was built.

---

## The Six Failure Categories

| # | Failure | Bias Type | Severity |
|---|---------|-----------|----------|
| 01 | Individual portion assumption — meal plans ignore stated cuisine preferences | Group Attribution + Selection | Critical |
| 02 | Privileged resource assumption — stacked payments, $270 plans, GLP-1 drug questions | Selection + Reporting | High |
| 03 | Precision-as-virtue + schedule universality — 8h sleep goal for a night shift worker | Selection + Reporting | High |
| 04 | Food classification contradicts nutrition science — rice is "yellow" but USDA puts whole grains at its base | Selection + Group Attribution | High |
| 05 | Single-person cooking model + Western visual defaults | Selection + Group Attribution | Medium |
| 06 | The Unencumbered Individual Assumption — the app has no model for a mother as a household system | **Implicit Bias** + Selection | Critical |

---

## The Core Finding — Failure 06 (v2)

The deepest finding came last — and it came from living, not from analysis.

These apps keep saying "find time for yourself," "love yourself first," "you deserve this." That advice is not wrong. But it assumes the self is separable from its context. For a mother, it is not.

My food is my family's food. My time is the family's time. My relationship with food is actually a relationship between me, my children, my budget, my culture, and the clock. I am not one person making choices for myself. **I am a system — a logistics operation.** My meal decisions are not personal preferences. They are the household running.

The behavioral psychology research underlying these apps was conducted on a population where the individual self is assumed to be the primary unit of change. No rule excludes mothers. The bias lives in who was never in the room when the model was built.

**The clinical AI connection:** Mental health AI tools trained on individualist behavioral markers misread caregiver lives as pathology. Waking at 2am is a depression signal in the training data. For a Vietnamese mother on night shift, it is Tuesday. The system reads her life as disorder because it was built to read a different life as normal.

---

## Key Evidence

**The core Group Attribution Bias argument:**
Noom onboarding → I select Vietnamese, Thai, Japanese → My "personalized" Week 1 meal plan: Pita Party Pizzas, Mango Chicken Salad with Couscous, Turkey Cheddar Tacos.

**The food pyramid contradiction:**
Noom classifies rice as a yellow (caution) food. The USDA Food Pyramid places whole grains at its base. The food I cook at home from scratch is being penalized by a classification system built for a different kitchen.

**The stacked payment problem:**
BetterMe charges a subscription fee, then adds $14.99 + $7.99 + $9.99 as separate in-app challenge purchases. I track cancellation dates on Google Calendar. That cognitive and financial burden is a design choice.

**The sleep tracking failure:**
BetterMe default sleep goal: 8 hours. Saturday March 21: 0% of goal. "We need more data." The data is: I was working a night shift. Reporting Bias reads my schedule as failure.

**The marketing vs. reality gap (v2):**
Every public review describes the apps as "personalized," "customized," and "adapts to your needs." The audit documents the gap between those claims and what the system actually delivered to a non-default user.

---

## Apps Audited

- **Noom** — trial account, March 2026
- **BetterMe** — trial account, March 2026
- **Simple** — excluded. Requires payment before any trial access. This is itself a Failure 02 finding.

---

## Honest Scope

This is a personal observational audit — not a peer-reviewed study. Evidence is drawn from one user's trial sessions. Population-level statistics (e.g. lactase intolerance rates by region) are flagged in the document where independent citation is needed before final publication.

---

## Why This Matters Beyond UX

The same bias types that make a diet app unfriendly to Asian users make clinical AI systems unreliable for patients who don't match the training population.

When a clinical AI system produces different diagnostic outputs for Asian patients because its training data was predominantly Western, that is selection bias. When it measures adherence by metrics that don't account for cultural dietary patterns, that is reporting bias. When it collects demographic data but doesn't change its recommendations, that is group attribution bias. When it assumes every patient is an unencumbered individual with an autonomous self — and misreads a caregiver's life as disorder — that is implicit bias.

**The stakes in clinical AI are higher. The methodology is the same.**

---

## Clinical AI QE Skills Demonstrated

- Default user bias detection
- Bias type classification (Google Responsible AI framework — 4 types)
- Implicit bias identification in UX and AI systems
- Failure mode categorization by root assumption
- Ground truth validation (comparing outputs against USDA food pyramid)
- Marketing claim vs. observed behavior gap analysis
- Evidence integrity — separating personal observation from statistical claims
- Structured audit documentation: failure → bias type → evidence → root cause → principle

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1 | March 22, 2026 | Initial publication. 5 failure categories. 3 bias types (Selection, Reporting, Group Attribution). |
| v2 | March 23, 2026 | Added Failure 06: The Unencumbered Individual Assumption (Implicit Bias). Added Marketing vs. Reality comparison table. Updated reflection with Mothers as Systems insight. 4 bias types now documented. |
| v3 | Planned | NIH/PubMed citations. Peer-reviewed sources for implicit bias in wellness AI. |
| v4 | Planned | Second user observation. Clinical AI tool audit applying same framework. |

---

## About the Author

I'm **Võ Ngọc Dung (DixieV)** — medical interpreter (5 years), former Chevron/SLB energy professional (10 years), Geoscience MSc from the University of Adelaide, and frontend developer in training. I hold a certificate in Generative AI in Healthcare (University of Illinois / Coursera) and have completed Google's Responsible AI for Developers course.

I'm transitioning into **Clinical AI Quality Engineering** — the role that evaluates whether AI systems are safe, fair, and accurate before they reach patients.

**Connect:** [LinkedIn](https://www.linkedin.com/in/dung-vo-25963376/) | [Portfolio](https://github.com/dvo10781-droid)

---

## Project Status

- [x] Diagnostic framework complete
- [x] Six failure categories with bias classification
- [x] Four bias types documented including Implicit Bias (v2)
- [x] Live screenshots — Noom and BetterMe (March 2026)
- [x] Food pyramid comparison — documented factual claim
- [x] Marketing vs. reality comparison table (v2)
- [x] Mothers as Systems reflection (v2)
- [x] Clinical AI QE skill mapping
- [x] Google Responsible AI framework applied
- [ ] Lactase intolerance citation (NIH/NCBI) — v3
- [ ] Peer-reviewed implicit bias sources — v3
- [ ] Second user observation — v4
- [ ] Clinical AI tool audit — v4

---

*v2 · March 2026 · Screenshots used for educational and analytical purposes.*

**Connect:** www.linkedin.com/in/ngoc-dung-vo-25963376 | [Portfolio](https://github.com/dvo10781-droid)

---


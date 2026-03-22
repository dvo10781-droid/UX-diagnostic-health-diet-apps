# UX Diagnostic: Why Diet & Cooking Apps Feel Unfriendly to Asian Users
 
**Live case study →** [View the full audit](https://dvo10781-droid.github.io/UX-diagnostic-health-diet-apps)
> **This is a portfolio case study, not a code repository.**  
> GitHub is used here as a professional documentation platform — the same way  
> designers, researchers, and clinical AI practitioners publish structured work.  
> No coding background needed to read this.
---

## The Origin

I've tried every major diet app. I always dropped out.

For a long time I thought it was a discipline problem. Then I started asking a different question: *what if the apps are the problem?*

I'm a Vietnamese woman in my forties. I work from home. I cook warm food — rice, soups, shared dishes — for my whole family on a tight budget. I enjoy all kinds of food. But eating a cold salad as a main meal? It is cold, it is dry, and it does not fill a family.

Every app I tried kept asking me to track food that wasn't in its database, follow meal plans that ignored my stated cuisine preferences, and log portions from a pot that four people ate from. Noom asked me which cuisines I eat. I said Vietnamese, Thai, Japanese. It served me Pita Party Pizzas and Mango Chicken Salad with Couscous on Day 1.

That's not a localization gap. That's a system assumption problem. And it has a name.

---

## What You're Looking At

A structured bias audit of two leading health apps — Noom and BetterMe —  conducted by a Vietnamese woman who tried them, failed to stay, and then asked  a better question: *what if the apps are the problem?*

This is not a redesign proposal. It is a **diagnostic** — five failure categories,  each classified by bias type, traced to a root system assumption, and documented  with live screenshots from real trial sessions (March 2026).

The analytical framework used here is the same one applied in  **Clinical AI Quality Engineering** — identifying default user assumptions,  classifying bias, and documenting failures before they reach patients.

---
## The Origin

I've tried every major diet app. I always dropped out.

For a long time I thought it was a discipline problem. Then I started asking  a different question: *what if the apps are the problem?*

I'm a Vietnamese woman in my forties. I work night shifts. I cook warm food —  rice, soups, shared dishes — for my whole family on a tight budget.  
But eating a cold salad as a main meal? It is cold. It is dry. It does not fill a family.

Noom asked me which cuisines I eat. I said: Vietnamese, Thai, Japanese and Chinese.  It served me **Pita Party Pizzas** and **Mango Chicken Salad with Couscous** on Day 1.

That's not a localization gap. That's a system assumption problem. And it has a name.

## Bias Types Identified

Using Google's Responsible AI for Developers framework:

**Selection Bias** — These apps were optimized for users who succeeded with Western eating patterns, conventional schedules, and standard household structures. The non-default user is invisible in the training data.

**Reporting Bias** — The apps surface and reward behaviors that fit their model: daily streaks, precise individual logging, standard sleep patterns. Behaviors that don't fit — shared dishes, night-shift schedules, family cooking — are penalized as "no data" or compliance failures.

**Group Attribution Bias** — Even when cultural preference data is collected (Vietnamese, Thai, Japanese cuisines), the same Western defaults are delivered to the whole user group. Collecting data is not the same as using it.

---

## The Five Failure Categories

| # | Failure | Bias Type | Severity |
|---|---------|-----------|----------|
| 01 | Individual portion assumption — meal plans ignore stated cuisine preferences | Group Attribution + Selection | Critical |
| 02 | Privileged resource assumption — stacked payments, $270 plans, GLP-1 drug questions | Selection + Reporting | High |
| 03 | Precision-as-virtue + schedule universality — 8h sleep goal for a night shift worker | Selection + Reporting | High |
| 04 | Food classification contradicts nutrition science — rice is "yellow" but the food pyramid puts whole grains at its base | Selection + Group Attribution | High |
| 05 | Single-person cooking model + Western visual defaults — challenge marketing uses no Asian faces | Selection + Group Attribution | Medium |

---

## Key Evidence

**The core argument in three screenshots:**
Noom onboarding → I select Vietnamese, Thai, Japanese as my cuisine preferences → My "personalized" Week 1 meal plan: Pita Party Pizzas, Mango Chicken Salad with Couscous, Turkey Cheddar Tacos.

**The food pyramid contradiction:**
Noom classifies rice as a yellow (caution) food. The USDA Food Pyramid places whole grains at its base — the foundation of a healthy diet. The food I cook at home from scratch is being penalized by a classification system built for a different kitchen.

**The stacked payment problem:**
BetterMe charges a subscription fee, then adds $14.99 (Flatter Belly), $7.99 (Clean Eating), and $9.99 (Better Sleep) as separate in-app purchases. I now track cancellation dates on Google Calendar so I don't get charged. That cognitive and financial burden is a design choice.

**The sleep tracking failure:**
BetterMe sets a default sleep goal of 8 hours. Saturday, March 21: 0% of sleep goal reached. "We need more data." The data is: I was working a night shift. Reporting Bias means the system reads this as failure rather than as a valid user pattern.

---

## Apps Audited

- **Noom** — trial account, March 2026
- **BetterMe** — trial account, March 2026
- **Simple** — excluded. Requires payment before any trial access. This is itself a Failure 02 finding.

---

## Honest Scope

This is a personal observational audit — not a peer-reviewed study. Evidence is drawn from one user's trial sessions. Population-level statistics (e.g. lactase intolerance rates by region) are flagged in the document where independent citation is needed before final publication. The bias classifications and food pyramid comparison are documentable factual claims that stand independently.

---

## Why This Matters Beyond UX

The analytical methodology here — identifying default user assumptions, classifying bias types, tracing failures to root causes, documenting with structured evidence — is the same methodology used in **Clinical AI Quality Engineering**.

When a clinical AI system produces different diagnostic outputs for Asian patients because its training data was predominantly Western, that is selection bias. When it measures adherence by metrics that don't account for cultural dietary patterns, that is reporting bias. When it collects demographic data but doesn't change its recommendations, that is group attribution bias.

The stakes in clinical AI are higher. The framework is the same.

---

## Clinical AI QE Skills Demonstrated

- Default user bias detection
- Bias type classification (Google Responsible AI framework)
- Failure mode categorization by root assumption
- Ground truth validation (comparing outputs against USDA food pyramid)
- Evidence integrity — separating personal observation from statistical claims requiring citation
- Structured audit documentation: failure → bias type → evidence → root cause → principle

---
## Project Status

- [x] Diagnostic framework complete  
- [x] Five failure categories with bias classification  
- [x] Live screenshots — Noom and BetterMe (March 2026)  
- [x] Food pyramid comparison — documented factual claim  
- [x] Clinical AI QE skill mapping  
- [x] Google Responsible AI framework applied  
- [ ] Lactase intolerance citation (NIH/NCBI) — in progress for v2  
- [ ] Peer review from clinical informatics contact — planned  

---
## About the Author

I'm **Võ Ngọc Dung (DixieV)** — medical interpreter (5 years), former Chevron/SLB energy professional (10 years), Geoscience MSc from the University of Adelaide, and frontend developer in training. I hold a certificate in Generative AI in Healthcare (University of Illinois / Coursera) and have completed Google's Responsible AI for Developers course.

I'm transitioning into **Clinical AI Quality Engineering** — the role that sits between engineering and clinical teams to evaluate whether AI systems are safe, fair, and accurate before they reach patients.

This case study is one of several portfolio projects demonstrating the bias detection and audit methodology at the core of that work.

**Connect:** www.linkedin.com/in/ngoc-dung-vo-25963376 | [Portfolio](https://github.com/dvo10781-droid)

---



*Draft v1 · March 2026 · Screenshots used for educational and analytical purposes.*

# EU Health Intelligence Suite

> Ten production-ready web applications mapping the structural crises facing European health systems — built for WHO and EU health policy analysis roles.

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Recharts](https://img.shields.io/badge/Charts-Recharts-22b5bf?style=flat-square)](https://recharts.org/)
[![Data: Eurostat](https://img.shields.io/badge/Data-Eurostat-003399?style=flat-square)](https://ec.europa.eu/eurostat)
[![Data: WHO EURO](https://img.shields.io/badge/Data-WHO%20EURO-009688?style=flat-square)](https://www.who.int/europe)
[![Data: ECDC](https://img.shields.io/badge/Data-ECDC-E91E63?style=flat-square)](https://www.ecdc.europa.eu)
[![Data: OECD](https://img.shields.io/badge/Data-OECD-CC0000?style=flat-square)](https://stats.oecd.org/)

## What This Is

A suite of ten interactive health intelligence dashboards covering the most pressing structural challenges in European public health — physician workforce shortages, antimicrobial resistance, health inequality, pandemic preparedness, the Long COVID burden, and more.

Every application uses **real, sourced epidemiological data** from Eurostat, WHO, ECDC, OECD, and EU-SILC. Every composite score, tier classification, and benchmark threshold is methodologically grounded and documented. Every interface is designed for a specific audience — because a biohazard surveillance dashboard should not look like a health equity research tool.

**26+ countries. 18+ official data sources. 10 completely different visual aesthetics.**

## The Applications

| # | Application | Domain | Primary Data | Aesthetic |
|---|-------------|--------|-------------|-----------|
| 01 | [ Workforce Crisis Monitor](https://github.com/YOUR-ORG/workforce-crisis-monitor) | Physician supply gaps | Eurostat `hlth_rs_physd` | Dark terminal |
| 02 | [ Avoidable Mortality Atlas](https://github.com/YOUR-ORG/avoidable-mortality-atlas) | Preventable & amenable deaths | Eurostat `hlth_cd_asdr2` | White editorial |
| 03 | [ AMR Surveillance Dashboard](https://github.com/YOUR-ORG/amr-surveillance-dashboard) | Antimicrobial resistance | ECDC EARS-Net 2022 | Biohazard green |
| 04 | [ Austerity Impact Analyzer](https://github.com/YOUR-ORG/austerity-impact-analyzer) | Spending cuts & mortality | Eurostat `gov_10a_exp` | Data-journalism |
| 05 | [ Mental Health Gap](https://github.com/YOUR-ORG/mental-health-gap) | MH infrastructure deficit | WHO Mental Health Atlas 2020 | Soft lavender |
| 06 | [ Pandemic Preparedness Scorecard](https://github.com/YOUR-ORG/pandemic-preparedness-scorecard) | Health security capacity | GHS Index 2021 + WHO SPAR | Navy emergency ops |
| 07 | [ Nurse Ratio Crisis Map](https://github.com/YOUR-ORG/nurse-ratio-crisis) | Nursing workforce & safety | Eurostat `hlth_rs_nurs` + EFN | Industrial red |
| 08 | [ Health Inequality Atlas](https://github.com/YOUR-ORG/health-inequality) | Socioeconomic disparities | EU-SILC + OECD | Warm sepia academic |
| 09 | [ Cross-Border Patient Flow](https://github.com/YOUR-ORG/cross-border-patient-flow) | EU patient mobility | EU Directive 2011/24/EU | Slate policy |
| 10 | [🫁 Long COVID Burden Dashboard](https://github.com/YOUR-ORG/long-covid-burden) | Post-COVID health burden | ONS + ECDC + WHO EURO | Deep purple |

> Replace `YOUR-ORG` with your GitHub organisation name throughout.

## Quick Start

Every application is fully self-contained. No database. No environment variables. No external API calls.

```bash
git clone https://github.com/YOUR-ORG/[app-name]
cd [app-name]
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — works offline immediately.

## Application Summaries

### 01 · Workforce Crisis Monitor

**The question:** Which European countries face physician shortages right now — and is the trajectory getting worse?

The WHO minimum for universal health coverage is **250 physicians per 100,000 population**. Countries below this threshold cannot meet population demand without workforce importation or emergency policy measures. By 2030, WHO EURO projects a **4.1 million health worker shortfall** across the European region. This dashboard maps every EU/EEA country against the benchmark, calculates the absolute headcount shortfall, and tracks whether each country is recovering or declining across 2015–2022.

**What makes it distinctive:** Shortage tier classification is defined against WHO UHC thresholds — not arbitrary percentiles. When a country is labelled CRITICAL, it means the WHO benchmark says so, not a design choice.

| Feature | Detail |
|---------|--------|
| Tiers | CRITICAL / HIGH / MODERATE / ADEQUATE against WHO 250/100k benchmark |
| Trend data | 2015–2022 trajectory — direction matters as much as position |
| Pipeline metric | Medical graduates per 100k — is the future supply shrinking? |
| Shortfall calculator | Absolute headcount needed to reach benchmark |

**Data:** `Eurostat hlth_rs_physd` · `OECD Health Statistics 2023` · `WHO EURO HRH Observatory`
**Reference year:** 2022

→ [workforce-crisis-monitor](https://github.com/YOUR-ORG/workforce-crisis-monitor)

### 02 · Avoidable Mortality Atlas

**The question:** Where are health systems failing to prevent deaths that should not be happening?

Avoidable mortality is the headline indicator in EU State of Health country profiles and WHO system performance assessments — the most direct measure of whether a health system is actually saving the lives it should save. This atlas uses the **joint Eurostat/OECD avoidable mortality methodology (2019)** to separate **preventable mortality** (public health failures: tobacco, vaccination, road safety) from **amenable mortality** (healthcare delivery failures: cardiac care, cancer treatment, diabetes). The split is analytically essential — each type implicates different ministries, budgets, and interventions.

**What makes it distinctive:** Most dashboards show total avoidable mortality. This one separates preventable from amenable. Collapsing them is technically incorrect and leads to misdiagnosed policy responses.

| Feature | Detail |
|---------|--------|
| Split methodology | Eurostat/OECD 2019 joint classification — same as EU State of Health profiles |
| Time series | 2005–2022 trend per country |
| Cause breakdown | Leading preventable and amenable causes per country |
| EU benchmark | Country ranking against EU-27 average |

**Data:** `Eurostat hlth_cd_asdr2` · Joint Eurostat/OECD avoidable mortality cause list (2019)
**Reference year:** 2020–2022

→ [avoidable-mortality-atlas](https://github.com/YOUR-ORG/avoidable-mortality-atlas)

### 03 · AMR Surveillance Dashboard

**The question:** Which pathogens are winning the resistance arms race — in which countries, and is the crisis accelerating?

Antimicrobial resistance is projected to cause more deaths than cancer by 2050. ECDC's EARS-Net surveillance network produces nationally representative resistance data every year — but it lives in technical reports most policymakers never read. This dashboard surfaces EARS-Net 2022 data for the **six WHO ESKAPE priority pathogens** across 30 countries, layers in antibiotic consumption (ESAC-Net) as the mechanistic driver, and scores each country with a composite **AMR Vulnerability Index** weighted by clinical threat severity.

**What makes it distinctive:** The Vulnerability Score weights pathogens by their relative threat to seriously ill patients. *A. baumannii* and *K. pneumoniae* are weighted highest because resistance in these organisms eliminates ICU treatment options entirely. This is clinical reasoning embedded in the scoring logic.

| Feature | Detail |
|---------|--------|
| Pathogens | *E. coli, K. pneumoniae, S. aureus/MRSA, E. faecium/VRE, P. aeruginosa, A. baumannii* |
| Vulnerability Score | Clinically weighted composite — documented in source code |
| Consumption layer | ESAC-Net DDD per 1,000 inhabitants per day |
| Tiers | CRITICAL / HIGH / MODERATE / LOW |

**Data:** `ECDC EARS-Net 2022` · `ECDC ESAC-Net`
**Reference year:** 2022

→ [amr-surveillance-dashboard](https://github.com/YOUR-ORG/amr-surveillance-dashboard)

### 04 · Healthcare Austerity Impact Analyzer

**The question:** What did post-2008 health spending cuts cost in lives — measured through the documented three-year mortality lag?

The 2008–2014 fiscal consolidation produced the largest natural experiment in European health financing history. Ten countries cut health expenditure significantly. The mortality consequences — documented with a **2–4 year lag** in the health economics literature (Stuckler & Basu 2013, and multiple subsequent replications) — are now visible in the data. This app computes lag correlations and excess death estimates for each country using the same methodology as peer-reviewed health economics research.

**What makes it distinctive:** The 3-year lag is not an assumption. It is a finding from the literature. The mechanism is documented: spending cuts → service quality degradation → workforce reduction → prevention programme elimination → excess deaths. The correlation appears in year T+3, not year T. This distinction separates rigorous analysis from advocacy.

| Feature | Detail |
|---------|--------|
| Lag analysis | Spending change in year T vs mortality in year T+3 |
| Excess deaths | Observed vs counterfactual trend projection |
| Austerity severity | IMF Fiscal Monitor primary balance classification |
| Period | 2005–2022 full time series |

**Data:** `Eurostat gov_10a_exp (GF07)` · `Eurostat hlth_cd_asdr` · `IMF Fiscal Monitor`
**Reference year:** 2005–2022

→ [austerity-impact-analyzer](https://github.com/YOUR-ORG/austerity-impact-analyzer)

### 05 · Mental Health Gap

**The question:** How large is the structural deficit in mental health workforce — and what does unmet need look like across Europe?

Mental health accounts for approximately **20% of disability-adjusted life years** in Europe but receives less than 10% of health budgets in even well-funded systems, and under 4% in some Eastern European countries. This app constructs a composite **Mental Health Gap Index** — weighted across psychiatrists, psychologists, budget share, unmet need, and psychiatric beds — and calculates for every country exactly how many additional psychiatrists are needed to reach the EU median. Bulgaria has a waiting time of 44 weeks for a first psychiatrist appointment. The app makes numbers like that visible and comparable.

**What makes it distinctive:** The psychiatric beds indicator is contextualised alongside community workforce capacity — because low bed counts sometimes reflect deliberate deinstitutionalisation (Italy, post-Basaglia reform) and sometimes reflect neglect. The app is designed to show the difference.

| Feature | Detail |
|---------|--------|
| Gap Index | Weighted: psychiatrists 25%, psychologists 20%, budget 20%, unmet need 20%, beds 15% |
| Investment target | "Psychiatrists needed" — absolute headcount to reach EU median |
| Unmet need | EU-SILC self-reported unmet mental health care need |
| Waiting times | Weeks to first psychiatrist appointment |

**Data:** `WHO Mental Health Atlas 2020` · `Eurostat hlth_rs_bds` · `EU-SILC hlth_silc_08` · `OECD Health Statistics 2023`
**Reference year:** 2020–2022

→ [mental-health-gap](https://github.com/YOUR-ORG/mental-health-gap)

### 06 · Pandemic Preparedness Scorecard

**The question:** How prepared were European countries — and did preparedness scores actually predict COVID-19 performance?

This app does two things existing preparedness tools do not do together: scores countries across the **six WHO JEE domains**, and validates those scores against real **COVID-19 excess mortality** (WHO estimates). The preparedness vs performance scatter is the central analytical contribution. The correlation is real but imperfect — Belgium's high GHS Index score alongside high excess mortality is the pivotal case study for the limits of tabletop preparedness assessment. The app makes that nuance visible rather than hiding it.

**What makes it distinctive:** The COVID-19 excess mortality validation uses WHO estimates rather than reported COVID deaths — because reported deaths are affected by testing capacity and reporting conventions. WHO excess mortality estimates are comparable across countries. Countries cannot game this metric.

| Feature | Detail |
|---------|--------|
| Framework | Six WHO JEE domains: Detection, Response, Health System, Governance, Communication, Countermeasures |
| IHR compliance | WHO SPAR 2022 self-assessment scores |
| Validation | WHO all-cause excess mortality per 100k vs preparedness score |
| COVID grade | A (< 80 excess deaths/100k) through F (> 300/100k) |

**Data:** `GHS Index 2021` · `WHO SPAR 2022` · `WHO excess mortality estimates 2021–2022`
**Reference year:** 2021–2022

→ [pandemic-preparedness-scorecard](https://github.com/YOUR-ORG/pandemic-preparedness-scorecard)

### 07 · Nurse-to-Patient Ratio Crisis Map

**The question:** Which countries have fallen below the ICN safe-staffing minimum — and what are the patient safety consequences?

The International Council of Nurses minimum is **1 nurse per occupied acute bed** — a clinically derived threshold, not a bureaucratic target. Below this ratio, peer-reviewed evidence shows increased 30-day patient mortality, higher hospital-acquired infection rates, more medication errors, and accelerating workforce exit through burnout. Greece at 0.5 nurses per bed, Italy at 0.8, Romania at 0.7 are not statistical outliers. They are health systems in which preventable patient harm is structurally embedded. The vacancy rate and burnout index track whether each country is recovering or accelerating toward further collapse.

**What makes it distinctive:** The burnout index is a forward indicator — it measures workforce sustainability, not just current capacity. A country can be above the ICN minimum today and heading for critical shortage within five years if the burnout index is high and the graduate rate is low.

| Feature | Detail |
|---------|--------|
| ICN benchmark | 1.0 nurses per occupied bed — displayed as reference line |
| Three views | Nurse:bed ratio · Vacancy rate · Burnout index |
| Pipeline | Graduate rate per 100k — future supply indicator |
| Workforce age | Average nursing workforce age — retirement risk signal |

**Data:** `Eurostat hlth_rs_nurs` · `OECD Health Statistics 2023` · `EFN Benchmarking Report 2023` · `ICN Safe Staffing standards`
**Reference year:** 2022–2023

→ [nurse-ratio-crisis](https://github.com/YOUR-ORG/nurse-ratio-crisis)

### 08 · Health Inequality Atlas

**The question:** How large is the gap between what European health systems promise and what they deliver to their poorest citizens?

Universal coverage does not mean equitable outcomes. France has universal coverage and a **9.2-year life expectancy gap** between its richest and poorest income quintiles. Bulgaria has a **15.8-year gap**. This atlas measures six inequality dimensions — all as the gap between Q5 (richest) and Q1 (poorest) — and makes the social epidemiology argument explicit through a Gini coefficient scatter: **income inequality and health inequality move together**. This is one of the most replicated findings in social epidemiology. The policy implication is equally replicated: you cannot close a 15-year life expectancy gap with healthcare interventions alone.

**What makes it distinctive:** The Gini–LE gap scatter is not decorative. It is the core argument: income redistribution is itself a health intervention. Countries in the top-right quadrant (high Gini, large LE gap) cannot solve their health inequality problem by reforming their health system alone.

| Feature | Detail |
|---------|--------|
| Inequality Index | Composite across six gap dimensions |
| Dimensions | Life expectancy · Unmet need · Screening access · Mental health · Smoking · Mortality ratio |
| Scatter | Gini coefficient vs life expectancy gap — with EU average reference lines |
| Tiers | HIGH EQUITY / MODERATE / HIGH INEQUALITY / SEVERE INEQUALITY |

**Data:** `EU-SILC hlth_silc_08` · `OECD Health at a Glance 2023` · `Eurostat hlth_cd_asdr2`
**Reference year:** 2021–2022

→ [health-inequality](https://github.com/YOUR-ORG/health-inequality)

### 09 · Cross-Border Patient Flow Tracker

**The question:** Where do EU patients go when their home system fails them — and what does the flow pattern reveal about which systems are failing?

The EU Cross-Border Healthcare Directive (2011/24/EU) is simultaneously a patient rights mechanism and a **live performance signal for health systems**. High outbound flows mean long waits, capacity gaps, or absent specialist services. Germany attracts **142,000 inbound patients annually** — the largest destination hub in Europe. Romania sends **32,400 patients abroad** with a net outflow of −29,600. The equity argument — that the Directive primarily benefits already-advantaged patients who can navigate reimbursement bureaucracy and pay upfront — is made explicit in the analysis.

**What makes it distinctive:** Emergency care (EHIC flows) is deliberately excluded. Only reimbursed planned care under the Directive is analysed — because that is the signal of deliberate system arbitrage by patients choosing to leave, not patients who happened to be abroad when they got sick.

| Feature | Detail |
|---------|--------|
| Net flow | Inbound minus outbound — positive = net receiver, negative = net sender |
| Top routes | 10 bilateral corridors with procedure type and weeks of wait saved |
| Wait-time driver | Scatter: average wait weeks vs outbound patients per million |
| Reimbursement | €M claimed per country annually |

**Data:** `EU Directive 2011/24/EU Annual Reports` · `EHIC Claims Data`
**Reference year:** 2022

→ [cross-border-patient-flow](https://github.com/YOUR-ORG/cross-border-patient-flow)

### 10 · Long COVID Burden Dashboard

**The question:** What is the actual scale of the Long COVID burden — and how adequately are health systems responding?

Long COVID is the largest new chronic disease burden created in Europe since the HIV epidemic. Conservative estimates: **17 million affected Europeans**, €100B+ in annual economic burden, an average of 9–14 weeks of workforce productivity lost per case per year. Only **6 of 15 countries** in this dataset have adopted a national strategy. This dashboard documents prevalence, the five-symptom profile aligned to the **WHO EURO Post-COVID Condition clinical case definition**, the economic burden split between direct costs and productivity loss, and rehabilitation access capacity.

**What makes it distinctive:** The symptom radar chart is not cosmetic — it shows whether a country's case mix is fatigue-dominant or cognitive-impairment-dominant, because these presentations have different rehabilitation pathways and different workforce requirements. A country with high brain fog prevalence needs neuropsychologists. A country with high breathlessness prevalence needs respiratory physiotherapists.

| Feature | Detail |
|---------|--------|
| Case definition | WHO EURO Post-COVID Condition (> 12 weeks, not explained by alternative diagnosis) |
| Symptom profile | Fatigue · Breathlessness · Brain fog · Muscle pain · Mental health |
| Economic burden | Direct healthcare + indirect productivity — stacked per country |
| Response gap | Rehabilitation access % vs prevalence — who is being left behind |

**Data:** `ONS COVID-19 Infection Survey` · `ECDC Long COVID Report 2023` · `WHO EURO Post-COVID Condition Guidelines`
**Reference year:** 2022–2023

→ [long-covid-burden](https://github.com/YOUR-ORG/long-covid-burden)

## Architecture

All ten applications share the same stack. The consistency is deliberate — it makes every codebase immediately navigable and lets design energy go into the domain, not the infrastructure.

```
Next.js 14 App Router    Server components process and score data before reaching the client
TypeScript               Every data entity is fully typed — no runtime surprises in health data
Tailwind CSS             Utility-first base; each app has custom globals.css for its own aesthetic
Recharts                 React-native charts — BarChart, RadarChart, ScatterChart, LineChart
Google Fonts             Different typeface pairing per app — see individual READMEs
```

### Why these choices

**Next.js 14 App Router** — server components mean composite scoring and data enrichment happen server-side. For 26-country datasets with multi-indicator weighted indices, this eliminates unnecessary client-side computation.

**TypeScript throughout** — in a health context, a runtime error caused by a data type mismatch is not a minor bug. Every indicator value, every country entity, every tier classification is typed. The compiler catches errors before they reach the interface.

**Data embedded in API routes, not a live database** — this is a deliberate architectural choice, not a limitation. Every number is auditable. Every source is traceable in code comments. Every deployment is zero-configuration. In a production WHO or EU environment these routes would connect to Eurostat SDMX, ECDC OpenData, and WHO data portal APIs — the architecture is identical, only the data source changes.

**Recharts over D3** — D3 requires direct DOM manipulation that conflicts with React's virtual DOM reconciliation. Recharts provides composable, React-native components that work correctly within the Next.js rendering model. For radar charts, scatter with click handlers, stacked bar, and reference lines — all used extensively here — Recharts provides exactly the right abstraction.

## Data Infrastructure

18+ official sources across the suite. Every source is cited in source code comments.

| Source | Used In | What It Provides |
|--------|---------|-----------------|
| **Eurostat `hlth_rs_physd`** | 01 | Practising physicians per 100k |
| **Eurostat `hlth_cd_asdr2`** | 02, 04 | Age-standardised avoidable mortality |
| **Eurostat `gov_10a_exp` (GF07)** | 04 | Government health expenditure % GDP |
| **Eurostat `hlth_rs_nurs`** | 07 | Practising nurses per 100k |
| **Eurostat `hlth_rs_bds`** | 05 | Psychiatric beds per 100k |
| **EU-SILC `hlth_silc_08`** | 05, 08 | Self-reported health by income quintile |
| **ECDC EARS-Net 2022** | 03 | Resistance rates, 30 countries, 6 pathogens |
| **ECDC ESAC-Net** | 03 | Antibiotic consumption DDD per 1,000/day |
| **ECDC Long COVID Report 2023** | 10 | European prevalence synthesis |
| **WHO Mental Health Atlas 2020** | 05 | MH workforce per 100k — 26 countries |
| **WHO SPAR 2022** | 06 | IHR core capacity self-assessment |
| **WHO excess mortality estimates** | 06 | COVID-19 all-cause excess mortality |
| **WHO EURO Post-COVID Guidelines** | 10 | Post-COVID Condition clinical case definition |
| **GHS Index 2021** | 06 | Global Health Security Index, 6 domains |
| **OECD Health Statistics 2023** | 01, 05, 07, 08 | Graduates, ratios, inequality gradients |
| **OECD Health at a Glance 2023** | 08 | Socioeconomic life expectancy gradients |
| **EFN Benchmarking Report 2023** | 07 | Nursing vacancy rates and sustainability |
| **EU Directive 2011/24/EU Reports** | 09 | Cross-border reimbursement flows |
| **ONS COVID-19 Infection Survey** | 10 | Long COVID prevalence methodology |
| **IMF Fiscal Monitor** | 04 | Austerity severity classification |

## Coverage

| Application | Countries | Reference Year |
|-------------|-----------|---------------|
| Workforce Crisis Monitor | 30 EU/EEA | 2022 |
| Avoidable Mortality Atlas | 27 EU | 2020–2022 |
| AMR Surveillance Dashboard | 30 EU/EEA | 2022 |
| Austerity Impact Analyzer | 10 austerity cases | 2005–2022 |
| Mental Health Gap | 26 | 2020–2022 |
| Pandemic Preparedness Scorecard | 26 | 2021–2022 |
| Nurse Ratio Crisis Map | 26 | 2022–2023 |
| Health Inequality Atlas | 22 | 2021–2022 |
| Cross-Border Patient Flow | 18 | 2022 |
| Long COVID Burden Dashboard | 15 | 2022–2023 |

## Who This Is For

Built to demonstrate applied health intelligence capability for roles at:

- **WHO Regional Office for Europe** — health system performance, workforce, health security
- **European Commission DG SANTE** — health system reviews, cross-border healthcare, equity
- **ECDC** — surveillance, AMR, pandemic preparedness
- **National health ministries** — evidence-based planning, international benchmarking
- **Health policy research institutions** — comparative health system analysis

The combination of real epidemiological data, methodologically defensible scoring, production-quality interactive applications, and audience-specific visual design across all ten tools represents the full analytical pipeline — from raw surveillance data to decision-ready intelligence — that health intelligence roles require.

## Licence

MIT — use freely. Cite original data sources when reproducing outputs.

Underlying data is from public sources (Eurostat, WHO, ECDC, OECD) and subject to their respective terms of use. All sources are cited in individual application READMEs and in source code comments.

*Next.js · TypeScript · Recharts · Tailwind CSS*
*Eurostat · WHO EURO · ECDC · OECD · EU-SILC · EFN · ONS · IMF*

# EU Health Intelligence Suite

> Eleven production-ready web applications mapping the structural crises facing European health systems — built for European public health and policy research contexts.

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Recharts](https://img.shields.io/badge/Charts-Recharts-22b5bf?style=flat-square)](https://recharts.org/)
[![Data: Eurostat](https://img.shields.io/badge/Data-Eurostat-003399?style=flat-square)](https://ec.europa.eu/eurostat)
[![Data: WHO EURO](https://img.shields.io/badge/Data-WHO%20EURO-009688?style=flat-square)](https://www.who.int/europe)
[![Data: ECDC](https://img.shields.io/badge/Data-ECDC-E91E63?style=flat-square)](https://www.ecdc.europa.eu)
[![Data: OECD](https://img.shields.io/badge/Data-OECD-CC0000?style=flat-square)](https://stats.oecd.org/)

## What This Is

A suite of eleven interactive health intelligence dashboards covering the most pressing structural challenges in European public health — physician workforce shortages, antimicrobial resistance, health inequality, pandemic preparedness, the Long COVID burden, and the full EU health legislative pipeline.

Every application uses **real, sourced epidemiological and policy data** from Eurostat, WHO, ECDC, OECD, EU-SILC, EUR-Lex, and the European Parliament. Every composite score, tier classification, and benchmark threshold is methodologically grounded and documented. Every interface is designed for a specific audience — because a biohazard surveillance dashboard should not look like a legislative intelligence tracker.

**26+ countries. 20+ official data sources. 11 completely different visual aesthetics.**

## The Applications

| # | Application | Domain | Primary Data | Aesthetic |
|---|-------------|--------|-------------|-----------|
| 01 | [Workforce Crisis Monitor](https://github.com/eu-health-intelligence/workforce-crisis-monitor) | Physician supply gaps | Eurostat `hlth_rs_physd` | Dark terminal |
| 02 | [Avoidable Mortality Atlas](https://github.com/eu-health-intelligence/avoidable-mortality-atlas) | Preventable & amenable deaths | Eurostat `hlth_cd_asdr2` | White editorial |
| 03 | [AMR Surveillance Dashboard](https://github.com/eu-health-intelligence/amr-surveillance-dashboard) | Antimicrobial resistance | ECDC EARS-Net 2022 | Biohazard green |
| 04 | [Austerity Impact Analyzer](https://github.com/eu-health-intelligence/austerity-impact-analyzer) | Spending cuts & mortality | Eurostat `gov_10a_exp` | Data-journalism |
| 05 | [Mental Health Gap](https://github.com/eu-health-intelligence/mental-health-gap) | MH infrastructure deficit | WHO Mental Health Atlas 2020 | Soft lavender |
| 06 | [Pandemic Preparedness Scorecard](https://github.com/eu-health-intelligence/pandemic-preparedness-scorecard) | Health security capacity | GHS Index 2021 + WHO SPAR | Navy emergency ops |
| 07 | [Nurse Ratio Crisis Map](https://github.com/eu-health-intelligence/nurse-ratio-crisis) | Nursing workforce & safety | Eurostat `hlth_rs_nurs` + EFN | Industrial red |
| 08 | [Health Inequality Atlas](https://github.com/eu-health-intelligence/health-inequality) | Socioeconomic disparities | EU-SILC + OECD | Warm sepia academic |
| 09 | [Cross-Border Patient Flow](https://github.com/eu-health-intelligence/cross-border-patient-flow) | EU patient mobility | EU Directive 2011/24/EU | Slate policy |
| 10 | [Long COVID Burden Dashboard](https://github.com/eu-health-intelligence/long-covid-burden) | Post-COVID health burden | ONS + ECDC + WHO EURO | Deep purple |
| 11 | [EU Health Policy Tracker](https://github.com/eu-health-intelligence/eu-health-policy-tracker) | Legislative pipeline & status | EUR-Lex + EP + Council of EU | Warm editorial |

## Quick Start

Every application is fully self-contained. No database. No environment variables. No external API calls.

```bash
git clone https://github.com/eu-health-intelligence/[app-name]
cd [app-name]
npm install
npm run dev
```

Open http://localhost:3000 — works offline immediately.

**Windows:**
```powershell
cd C:\Users\YourName\Downloads\[app-name]
npm install
npm run dev
```
## Application Summaries

<details>
<summary><strong>01 · Workforce Crisis Monitor</strong> — Physician supply gaps · Eurostat hlth_rs_physd · Dark terminal</summary>

**The question:** Which European countries face physician shortages right now — and is the trajectory getting worse?

The WHO minimum for universal health coverage is **250 physicians per 100,000 population**. By 2030, WHO EURO projects a **4.1 million health worker shortfall** across the European region. This dashboard maps every EU/EEA country against the benchmark, calculates the absolute headcount shortfall, and tracks whether each country is recovering or declining across 2015–2022.

| Feature | Detail |
|---------|--------|
| Tiers | CRITICAL / HIGH / MODERATE / ADEQUATE against WHO 250/100k benchmark |
| Trend data | 2015–2022 trajectory |
| Pipeline metric | Medical graduates per 100k |
| Shortfall calculator | Absolute headcount needed to reach benchmark |

**Data:** `Eurostat hlth_rs_physd` · `OECD Health Statistics 2023` · `WHO EURO HRH Observatory` · **Reference year:** 2022

→ [workforce-crisis-monitor](https://github.com/eu-health-intelligence/workforce-crisis-monitor)
</details>

<details>
<summary><strong>02 · Avoidable Mortality Atlas</strong> — Preventable & amenable deaths · Eurostat hlth_cd_asdr2 · White editorial</summary>

**The question:** Where are health systems failing to prevent deaths that should not be happening?

Uses the **joint Eurostat/OECD avoidable mortality methodology (2019)** to separate **preventable mortality** (public health failures) from **amenable mortality** (healthcare delivery failures). The split is analytically essential — each type implicates different ministries, budgets, and interventions.

| Feature | Detail |
|---------|--------|
| Split methodology | Eurostat/OECD 2019 joint classification |
| Time series | 2005–2022 trend per country |
| Cause breakdown | Leading preventable and amenable causes per country |
| EU benchmark | Country ranking against EU-27 average |

**Data:** `Eurostat hlth_cd_asdr2` · Joint Eurostat/OECD cause list (2019) · **Reference year:** 2020–2022

→ [avoidable-mortality-atlas](https://github.com/eu-health-intelligence/avoidable-mortality-atlas)
</details>

<details>
<summary><strong>03 · AMR Surveillance Dashboard</strong> — Antimicrobial resistance · ECDC EARS-Net 2022 · Biohazard green</summary>

**The question:** Which pathogens are winning the resistance arms race — in which countries, and is the crisis accelerating?

Surfaces EARS-Net 2022 data for the **six WHO ESKAPE priority pathogens** across 30 countries, layers in antibiotic consumption (ESAC-Net), and scores each country with a composite **AMR Vulnerability Index** weighted by clinical threat severity.

| Feature | Detail |
|---------|--------|
| Pathogens | *E. coli, K. pneumoniae, S. aureus/MRSA, E. faecium/VRE, P. aeruginosa, A. baumannii* |
| Vulnerability Score | Clinically weighted composite |
| Consumption layer | ESAC-Net DDD per 1,000 inhabitants per day |
| Tiers | CRITICAL / HIGH / MODERATE / LOW |

**Data:** `ECDC EARS-Net 2022` · `ECDC ESAC-Net` · **Reference year:** 2022

→ [amr-surveillance-dashboard](https://github.com/eu-health-intelligence/amr-surveillance-dashboard)
</details>

<details>
<summary><strong>04 · Healthcare Austerity Impact Analyzer</strong> — Spending cuts & mortality · Eurostat gov_10a_exp · Data-journalism</summary>

**The question:** What did post-2008 health spending cuts cost in lives?

Computes lag correlations and excess death estimates using the **2–4 year mortality lag** documented in health economics literature (Stuckler & Basu 2013 and replications). The mechanism: spending cuts → service degradation → workforce reduction → excess deaths, appearing at T+3.

| Feature | Detail |
|---------|--------|
| Lag analysis | Spending change year T vs mortality year T+3 |
| Excess deaths | Observed vs counterfactual trend projection |
| Austerity severity | IMF Fiscal Monitor classification |
| Period | 2005–2022 full time series |

**Data:** `Eurostat gov_10a_exp (GF07)` · `Eurostat hlth_cd_asdr` · `IMF Fiscal Monitor` · **Reference year:** 2005–2022

→ [austerity-impact-analyzer](https://github.com/eu-health-intelligence/austerity-impact-analyzer)
</details>

<details>
<summary><strong>05 · Mental Health Gap</strong> — MH infrastructure deficit · WHO Mental Health Atlas 2020 · Soft lavender</summary>

**The question:** How large is the structural deficit in mental health workforce across Europe?

Constructs a composite **Mental Health Gap Index** weighted across psychiatrists, psychologists, budget share, unmet need, and psychiatric beds. Calculates for every country exactly how many additional psychiatrists are needed to reach the EU median.

| Feature | Detail |
|---------|--------|
| Gap Index | Psychiatrists 25% · Psychologists 20% · Budget 20% · Unmet need 20% · Beds 15% |
| Investment target | Absolute headcount to reach EU median |
| Unmet need | EU-SILC self-reported unmet MH care need |
| Waiting times | Weeks to first psychiatrist appointment |

**Data:** `WHO Mental Health Atlas 2020` · `Eurostat hlth_rs_bds` · `EU-SILC hlth_silc_08` · `OECD Health Statistics 2023` · **Reference year:** 2020–2022

→ [mental-health-gap](https://github.com/eu-health-intelligence/mental-health-gap)
</details>

<details>
<summary><strong>06 · Pandemic Preparedness Scorecard</strong> — Health security capacity · GHS Index 2021 + WHO SPAR · Navy emergency ops</summary>

**The question:** How prepared were European countries — and did preparedness scores actually predict COVID-19 performance?

Scores countries across the **six WHO JEE domains** and validates those scores against real **COVID-19 excess mortality** (WHO estimates). The preparedness vs performance scatter is the central analytical contribution.

| Feature | Detail |
|---------|--------|
| Framework | Six WHO JEE domains |
| IHR compliance | WHO SPAR 2022 self-assessment scores |
| Validation | WHO all-cause excess mortality per 100k vs preparedness score |
| COVID grade | A (< 80 excess deaths/100k) through F (> 300/100k) |

**Data:** `GHS Index 2021` · `WHO SPAR 2022` · `WHO excess mortality estimates 2021–2022` · **Reference year:** 2021–2022

→ [pandemic-preparedness-scorecard](https://github.com/eu-health-intelligence/pandemic-preparedness-scorecard)
</details>

<details>
<summary><strong>07 · Nurse Ratio Crisis Map</strong> — Nursing workforce & safety · Eurostat hlth_rs_nurs + EFN · Industrial red</summary>

**The question:** Which countries have fallen below the ICN safe-staffing minimum?

The International Council of Nurses minimum is **1 nurse per occupied acute bed**. Greece at 0.5, Italy at 0.8, Romania at 0.7 are health systems in which preventable patient harm is structurally embedded. The burnout index tracks whether each country is recovering or accelerating toward further collapse.

| Feature | Detail |
|---------|--------|
| ICN benchmark | 1.0 nurses per occupied bed — reference line |
| Three views | Nurse:bed ratio · Vacancy rate · Burnout index |
| Pipeline | Graduate rate per 100k |
| Workforce age | Average nursing workforce age — retirement risk |

**Data:** `Eurostat hlth_rs_nurs` · `OECD Health Statistics 2023` · `EFN Benchmarking Report 2023` · **Reference year:** 2022–2023

→ [nurse-ratio-crisis](https://github.com/eu-health-intelligence/nurse-ratio-crisis)
</details>

<details>
<summary><strong>08 · Health Inequality Atlas</strong> — Socioeconomic disparities · EU-SILC + OECD · Warm sepia academic</summary>

**The question:** How large is the gap between what European health systems promise and what they deliver to their poorest citizens?

France has universal coverage and a **9.2-year life expectancy gap** between richest and poorest quintiles. Bulgaria has a **15.8-year gap**. The Gini–LE scatter makes the social epidemiology argument explicit: income inequality and health inequality move together.

| Feature | Detail |
|---------|--------|
| Inequality Index | Composite across six gap dimensions |
| Dimensions | Life expectancy · Unmet need · Screening · Mental health · Smoking · Mortality ratio |
| Scatter | Gini coefficient vs life expectancy gap |
| Tiers | HIGH EQUITY / MODERATE / HIGH INEQUALITY / SEVERE INEQUALITY |

**Data:** `EU-SILC hlth_silc_08` · `OECD Health at a Glance 2023` · `Eurostat hlth_cd_asdr2` · **Reference year:** 2021–2022

→ [health-inequality](https://github.com/eu-health-intelligence/health-inequality)
</details>

<details>
<summary><strong>09 · Cross-Border Patient Flow Tracker</strong> — EU patient mobility · EU Directive 2011/24/EU · Slate policy</summary>

**The question:** Where do EU patients go when their home system fails them?

Germany attracts **142,000 inbound patients annually**. Romania sends **32,400 abroad** with a net outflow of −29,600. Emergency EHIC flows are excluded — only reimbursed planned care under the Directive is analysed, the signal of deliberate system arbitrage.

| Feature | Detail |
|---------|--------|
| Net flow | Inbound minus outbound |
| Top routes | 10 bilateral corridors with procedure type and wait saved |
| Wait-time driver | Scatter: wait weeks vs outbound patients per million |
| Reimbursement | €M claimed per country annually |

**Data:** `EU Directive 2011/24/EU Annual Reports` · `EHIC Claims Data` · **Reference year:** 2022

→ [cross-border-patient-flow](https://github.com/eu-health-intelligence/cross-border-patient-flow)
</details>

<details>
<summary><strong>10 · Long COVID Burden Dashboard</strong> — Post-COVID health burden · ONS + ECDC + WHO EURO · Deep purple</summary>

**The question:** What is the actual scale of the Long COVID burden — and how adequately are health systems responding?

**17 million affected Europeans.** €100B+ annual economic burden. Only **6 of 15 countries** with a national strategy. The symptom radar shows whether each country's case mix is fatigue-dominant or cognitive-impairment-dominant — because these need different rehabilitation pathways.

| Feature | Detail |
|---------|--------|
| Case definition | WHO EURO Post-COVID Condition (> 12 weeks) |
| Symptom profile | Fatigue · Breathlessness · Brain fog · Muscle pain · Mental health |
| Economic burden | Direct healthcare + indirect productivity |
| Response gap | Rehabilitation access % vs prevalence |

**Data:** `ONS COVID-19 Infection Survey` · `ECDC Long COVID Report 2023` · `WHO EURO Post-COVID Guidelines` · **Reference year:** 2022–2023

→ [long-covid-burden](https://github.com/eu-health-intelligence/long-covid-burden)
</details>

<details>
<summary><strong>11 · EU Health Policy Intelligence Tracker</strong> — Legislative pipeline · EUR-Lex + EP + Council · Warm editorial</summary>

**The question:** What is happening right now in EU health legislation — and what does it mean for WHO, ECDC, and national health ministries?

WHO EURO and ECDC staff currently monitor the EU legislative calendar across four or more separate sources. There is no single dashboard that shows every active health dossier, its current procedural stage, what it means for public health institutions, and what is arriving next quarter. This tracker is that tool.

| Feature | Detail |
|---------|--------|
| Dossiers | 12 active EU health legislative dossiers |
| Stage tracking | Enacted · Agreed · Trilogue · Council Position · Proposed · Announced |
| Implications | WHO / ECDC / EMA / DG SANTE implications per dossier |
| Timeline | Full legislative journey — past, current, upcoming |
| Filter + search | By stage and full-text |
| Deadline calendar | 7 upcoming milestones through 2029 |

**Key dossiers:** EHDS Reg. 2025/327 · Pharma Package · Critical Medicines Act · Biotech Act · HERA · EU4Health · AMR Voucher · Safe Hearts Plan

**Data:** `EUR-Lex` · `EP Legislative Train` · `Council of the EU` · `Commission Work Programme 2025` · **Updated:** Feb 2026

→ [eu-health-policy-tracker](https://github.com/eu-health-intelligence/eu-health-policy-tracker)
</details>

## Architecture

All eleven applications share the same stack.

```
Next.js 14 App Router    Server components process and score data before reaching the client
TypeScript               Every data entity is fully typed — no runtime surprises in health data
Tailwind CSS             Utility-first base; each app has custom globals.css for its own aesthetic
Recharts                 React-native charts — BarChart, RadarChart, ScatterChart, LineChart
Google Fonts             Different typeface pairing per app — see individual READMEs
```

**Data embedded in API routes, not a live database** — every number is auditable, every source traceable in code comments, every deployment zero-configuration. In a production WHO or EU environment these routes would connect to Eurostat SDMX, ECDC OpenData, EUR-Lex SPARQL, and WHO data portal APIs — the architecture is identical, only the data source changes.

## Data Infrastructure

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
| **EUR-Lex** | 11 | Official legislative texts and references |
| **EP Legislative Train** | 11 | Procedural stage and trilogue status |
| **Council of the EU** | 11 | Council positions and General Approach dates |
| **Commission Work Programme 2025** | 11 | Upcoming proposals and strategic priorities |

## Coverage

| Application | Countries / Scope | Reference Year |
|-------------|-------------------|---------------|
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
| EU Health Policy Tracker | 12 active dossiers | Updated Feb 2026 |

## Who This Is For

- **WHO Regional Office for Europe** — health system performance, workforce, health security, legislative alignment
- **European Commission DG SANTE** — health system reviews, cross-border healthcare, equity, legislative tracking
- **ECDC** — surveillance, AMR, pandemic preparedness, policy implications monitoring
- **National health ministries** — evidence-based planning, benchmarking, EU legislation transposition
- **Health policy research institutions** — comparative health system analysis, legislative intelligence

## Author

**Ofile Mfetane** — Health systems data analyst and developer based in Botswana, building applied analytics tools for European public health and policy research contexts.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ofile%20Mfetane-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/ofile-mfetane)
[![Medium](https://img.shields.io/badge/Medium-%40ofilemfetane-000000?style=flat-square&logo=medium)](https://medium.com/@ofilemfetane)
[![GitHub](https://img.shields.io/badge/GitHub-eu--health--intelligence-181717?style=flat-square&logo=github)](https://github.com/eu-health-intelligence)

## Licence

MIT — use freely. Cite original data sources when reproducing outputs.

*Next.js · TypeScript · Recharts · Tailwind CSS*
*Eurostat · WHO EURO · ECDC · OECD · EU-SILC · EFN · ONS · IMF · EUR-Lex · EP · Council of EU*
*Built by [Ofile Mfetane](https://www.linkedin.com/in/ofile-mfetane) · [medium.com/@ofilemfetane](https://medium.com/@ofilemfetane)*

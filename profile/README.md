# EU Health Intelligence Suite  
## Application Summaries

This section provides a structured overview of all ten applications within the EU Health Intelligence Suite.  
Each application addresses a distinct structural challenge in European health systems and is grounded in official epidemiological, surveillance, or administrative datasets.

# 01 · Workforce Crisis Monitor

## The Question  
**Which European countries face physician shortages right now — and is the trajectory getting worse?**

The WHO minimum density threshold for universal health coverage is **250 physicians per 100,000 population**. Countries falling below this benchmark are unlikely to meet service demand without workforce importation or emergency policy measures.

This application:

- Maps all EU/EEA countries against the WHO UHC benchmark  
- Calculates the absolute headcount shortfall  
- Tracks workforce density trends from 2015–2022  
- Identifies whether countries are stabilising or declining  

WHO EURO projects a **4.1 million health worker shortfall by 2030** across the region.  
This dashboard makes that structural trajectory visible and comparable.

### Key Features
- Shortage tier classification against WHO UHC thresholds  
- Graduate pipeline trend modelling  
- Absolute physician shortfall calculator  
- Country detail panel with longitudinal trajectory  

**Repository:** `workforce-crisis-monitor`  
**Data Sources:** Eurostat `hlth_rs_physd` · OECD Health Statistics 2023 · WHO EURO HRH Observatory  

# 02 · Avoidable Mortality Atlas

## The Question  
**Where are health systems failing to prevent deaths that should not be happening?**

Avoidable mortality is the most direct outcome-based metric of health system performance used in EU State of Health Profiles.

The atlas separates:

- **Preventable mortality** — failures in public health policy  
- **Amenable mortality** — failures in healthcare delivery  

This distinction matters because each implicates different policy actors.

### Key Features
- Preventable vs amenable mortality split  
- EU benchmark ranking system  
- Cause-of-death breakdown  
- 2005–2022 trend visualisation  

**Repository:** `avoidable-mortality-atlas`  
**Data Source:** Eurostat `hlth_cd_asdr2`  

# 03 · AMR Surveillance Dashboard

## The Question  
**Which pathogens are winning the resistance arms race?**

Antimicrobial resistance is projected to exceed cancer mortality by 2050.

This dashboard surfaces:

- ECDC EARS-Net surveillance data  
- Six WHO ESKAPE priority pathogens  
- Antibiotic consumption pressure (DDD/1000/day)  
- Composite AMR Vulnerability Index  

The vulnerability score weights pathogens by clinical severity.

### Key Features
- Six ESKAPE pathogens  
- Composite AMR Vulnerability Score  
- Resistance vs consumption correlation  
- CRITICAL / HIGH / MODERATE / LOW classification tiers  

**Repository:** `amr-surveillance-dashboard`  
**Data Sources:** ECDC EARS-Net 2022 · ECDC ESAC-Net  

# 04 · Healthcare Austerity Impact Analyzer

## The Question  
**What did post-2008 health spending cuts cost in lives?**

The 2008–2014 fiscal consolidation period produced the largest natural experiment in European health financing history.

This application:

- Models health spending trajectories  
- Applies documented 2–4 year mortality lag methodology  
- Computes lag correlations  
- Estimates excess mortality associated with spending cuts  

Methodology aligns with peer-reviewed health economics literature.

### Key Features
- Pre/post austerity trajectory modelling  
- 3-year lag correlation analysis  
- Excess deaths estimation  
- IMF austerity severity classification  

**Repository:** `austerity-impact-analyzer`  
**Data Sources:** Eurostat `gov_10a_exp` · Eurostat mortality series · IMF Fiscal Monitor  

# 05 · Mental Health Gap

## The Question  
**How large is the structural mental health workforce deficit across Europe?**

Mental health accounts for ~20% of disability-adjusted life years in Europe but receives significantly less funding and workforce allocation.

This application constructs a **Mental Health Gap Index**, weighted across:

- Psychiatrists per 100k  
- Psychologists per 100k  
- Psychiatric beds  
- Budget allocation  
- Unmet care need  

### Key Features
- Composite Gap Index  
- “Psychiatrists needed” target calculator  
- EU-SILC unmet need integration  
- Radar comparison vs EU average  

**Repository:** `mental-health-gap`  
**Data Sources:** WHO Mental Health Atlas 2020 · Eurostat `hlth_rs_bds` · EU-SILC `hlth_silc_08`  

# 06 · Pandemic Preparedness Scorecard

## The Question  
**Did preparedness scores actually predict COVID-19 outcomes?**

This application combines:

- WHO JEE domain scoring  
- WHO SPAR IHR compliance metrics  
- COVID-19 excess mortality validation  

The central analytical contribution is the preparedness vs performance scatter.

### Key Features
- Six WHO JEE domain breakdown  
- IHR compliance mapping  
- Preparedness vs excess mortality correlation  
- A–F COVID performance grade  

**Repository:** `pandemic-preparedness-scorecard`  
**Data Sources:** GHS Index 2021 · WHO SPAR 2022 · WHO excess mortality estimates  

# 07 · Nurse-to-Patient Ratio Crisis Map

## The Question  
**Which countries fall below the ICN safe staffing minimum?**

The International Council of Nurses benchmark is **1 nurse per occupied acute bed**.

Below this threshold, evidence links to:

- Higher 30-day mortality  
- Increased hospital-acquired infections  
- Medication errors  

### Key Features
- ICN benchmark reference line  
- Nurse:bed ratio classification  
- Vacancy rate analysis  
- Burnout index indicators  

**Repository:** `nurse-ratio-crisis`  
**Data Sources:** Eurostat `hlth_rs_nurs` · OECD Health Statistics 2023 · EFN Benchmarking Report  

# 08 · Health Inequality Atlas

## The Question  
**How large is the socioeconomic health gradient in Europe?**

Universal coverage does not guarantee equitable outcomes.

This atlas measures inequality across:

- Life expectancy  
- Unmet need  
- Screening access  
- Mental health  
- Smoking prevalence  
- Mortality ratio  

All measured as Q5 (richest) minus Q1 (poorest).

### Key Features
- Composite Inequality Index  
- Gini vs life expectancy gap scatter  
- EU-SILC unmet need differential  
- Policy classification tiers  

**Repository:** `health-inequality`  
**Data Sources:** EU-SILC · OECD Health at a Glance 2023  

# 09 · Cross-Border Patient Flow Tracker

## The Question  
**Where do EU patients go when their home system fails them?**

Under Directive 2011/24/EU, patient mobility acts as a performance signal.

This application:

- Maps inbound/outbound patient flows  
- Identifies top bilateral routes  
- Measures wait-time savings  
- Tracks reimbursement flows  

### Key Features
- Net flow classification  
- Top 10 bilateral corridors  
- Wait-time vs outbound correlation  
- € reimbursement totals  

**Repository:** `cross-border-patient-flow`  
**Data Sources:** EU Directive 2011/24/EU Reports · EHIC Claims Data  

# 10 · Long COVID Burden Dashboard

## The Question  
**What is the scale of the Long COVID burden — and how adequate is the system response?**

Long COVID represents one of the largest new chronic disease burdens in Europe.

This application documents:

- Prevalence by country  
- WHO EURO symptom case definition alignment  
- Direct vs productivity economic burden  
- Rehabilitation access gaps  

### Key Features
- Prevalence modelling  
- Symptom radar chart  
- Direct vs indirect cost breakdown  
- Rehabilitation capacity vs prevalence scatter  

**Repository:** `long-covid-burden`  
**Data Sources:** ONS COVID-19 Infection Survey · ECDC Long COVID Report 2023 · WHO EURO Guidelines  

# Architecture

All ten applications share a unified technical stack.

- **Next.js 14 (App Router)** — server components for scoring & enrichment  
- **TypeScript** — strongly typed health data models  
- **Tailwind CSS** — utility-first styling with per-application theming  
- **Recharts** — composable, React-native data visualisation components  

Design consistency is deliberate.  
Domain-specific presentation is intentional.

# Data Infrastructure

18+ official data sources across the suite:

Eurostat · WHO · WHO EURO · ECDC · OECD · EU-SILC · EFN · ONS · IMF · GHS Index  

All datasets are:

- Publicly available  
- Cited in code comments  
- Referenced in individual application READMEs  
- Methodologically aligned with official documentation  

# ho This Is For

Designed to demonstrate applied health intelligence capability for:

- WHO Regional Office for Europe  
- European Commission DG SANTE  
- ECDC  
- National health ministries  
- Health policy research institutions  

This suite represents the full analytical pipeline —  
from raw surveillance data to decision-ready intelligence.

# Licence

MIT — use freely. Cite original data sources when reproducing outputs.

Next.js · TypeScript · Recharts · Tailwind CSS  
Eurostat · WHO EURO · ECDC · OECD · EU-SILC · EFN · ONS · IMF

---
title: Commonly Used Data Sources
description: Below are some of the Snowflake datasets that we use most frequently in our work as economists at BGI.
parent: index.md
max_lines: 250
source: slab
---

# Commonly Used Data Sources

Below are some of the Snowflake datasets that we use most frequently in our work as economists at BGI.

## Job Postings Data

- **Snowflake schema:** EMSI_BURNING_GLASS_INSTITUTE.US
- **Snowflake schema for backups:** BGI_POSTINGS_BACKUPS.NOV_25 (or more recent month + year)
- **Data source:** Lightcast (formerly EMSI Burning Glass Technologies)
  - Note: we're in the process of transition to using Revelio postings data
  - EMSI comes directly from Lightcast (you can see additions in real time) but is often very slow, consider using backups for large queries.

## Job Profiles Data

- **Snowflake schema for non-panel data:** PDL_CLEAN.V[current version number]
- **Snowflake schema for panel data:** PROJECT_DATA.JOB_PANELS
- **Data source:** People Data Labs (PDL)
- **What it is:** individual-level data from job profiles (i.e. LinkedIn)
  - Educational attainment
  - Career history
  - Skills listed on job profile
  - Panel data contains imputed wage from Glassdoor + OEWS and has one observation per job year

## OEWS Data

- **Snowflake schema:** OUTSIDE_DATA.OEWS
- **Data source:** Occupational Employment and Wage Statistics (OEWS) from the U.S. Bureau of Labor Statistics (BLS)
- **What it is:** annual employment and wage estimates by occupation; available for the country as a whole and by MSA, state, and industry/sector
- **Common BGI use cases:**
  - Identify total employment and mean/median wage by occupation
  - Determine mean wage for an occupation + MSA to benchmark individuals' wages against
- **Useful variables:** a_median = median annual income, a_mean = mean annual income
- **Coverage:** 2011 - 2024
- **Use with:** CROSSWALKS.CUSTOM.ONET_2019_OEWS_CROSSWALK to find an OEWS code for (almost) every ONET/SOC code

## BLS Data

- **Snowflake schema:** OUTSIDE_DATA.BLS
- **Data source:** U.S. Bureau of Labor Statistics (BLS)
- **Common BGI use cases:**
  - Determine minimum education level required for SOC 6-digit occupations (table: OCC_DEG_REQUIRE)
  - Get estimated education attainment across SOC 6-digit occupations (table: OCC_DEG_ATTAIN)

## CIP-SOC Crosswalks

We typically use CIP-SOC crosswalks to determine whether an individual's college major is aligned with their occupation. There are two different CIP-SOC crosswalks that we use: the federal one (NCES/BLS) and our BGI-generated one.

- Federal:
  - **Snowflake table:** OUTSIDE_DATA.BLS.CIP_SOC_CROSSWALK
  - **Data source:** National Center for Education Statistics (NCES) and BLS
- BGI's:
  - **Snowflake schema:** PROJECT_DATA.CIP_SOC_CROSSWALK
  - Uses profile data to link CIPs (majors) to SOCs (occupations) based on observed transitions.

## L2 Data

- **Snowflake schema:** L2.APR_25 (or whatever date is most recent)
  - Matched to PDL profiles data; matches in PDL_DATA_PRODUCTS.DATA_PRODUCTS
- **Data source:** L2
- **What it is:** voter data
- **Common BGI use cases:**
  - Estimate age and demographics of individuals in PDL data who also show up in L2 data

## Job Transitions Data

- **Snowflake schema:** PROJECT_DATA.JOB_TRANSITIONS
- **What it is:** tracks how workers move between occupations over time using PDL profiles data

## Credentials of Value Index (CVI) Data

- **Note:** this project was formerly known as the EQOS project
- **Snowflake schema:** EQOS.JUN_25 (or more recent month + year)
- **Common BGI use cases:**
  - Used to create the CVI tool
  - Pre-made intermediate analysis for cleaned credentials in profile data

## Skills Data

- **Snowflake schema:** PROJECT_DATA.SKILL_METRICS

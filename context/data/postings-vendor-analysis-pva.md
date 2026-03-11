---
title: Postings Vendor Analysis (PVA)
description: Exploring alternatives to the LightCast postings data as the contract is coming to an end in 2026.
parent: index.md
max_lines: 250
source: slab
---

# Postings Vendor Analysis (PVA)

## Introduction

Our contract with LightCast is coming to an end in 2026. Given this fact, we have begun exploring alternatives to the LightCast postings data. These could be to augment our dataset if we choose to continue with LC post-2026 or replace LC.

## Version 1

Version 1 included researching, reaching out to and analyzing posting data from several vendors across the globe.

### Phase 1: Found Vendors
* Linkup
* Text Kernel
* Talent Neuron
* CoreSignal
* Grepsr
* APIScrapy
* Censia
* ScrapeLabs
* PromptCloud
* OpenWebNinja
* ProxyCurl/Nubela
* Revelio (COSMOS)
* XVerum

### Phase 2: Contacted Vendors
The following vendors were contacted for discussions: Linkup, Talent Neuron, CoreSignal, Grepsr, APIScrapy, ScrapeLabs, PromptCloud, OpenWebNinja, ProxyCurl/Nubela, Revelio (COSMOS), and XVerum.

### Phase 3: Analysis
We received samples (Delaware only) and ran analysis comparing them to Lightcast. Based on this, we are continuing deeper dives into **LinkUp**, **Talent Neuron**, and **Revelio (Cosmos)**.

## Version 2: Deeper Analysis

Requirements sent to potential vendors:
* Job postings data posted in March 2024 and September 2024
* State of North Carolina
* Global Counts by Country-State-Year

### Phase 1: Key Questions

**Deduplication**
* **Revelio:** Yes, maps to occupation taxonomy, company tree, and location. Scores text similarity. Models expected hires per posting.
* **LinkUp:** No post-hoc deduplication. Unique `job_hash` based on URL.

**Historical Data**
* **Revelio:** Stable starting September 2021 (global LinkedIn). US/UK Indeed stable as of 2016.
* **LinkUp:** Since 2007.

**Expired Postings**
* **Revelio:** Largely observed close dates. Daily scrapes for most sources.
* **LinkUp:** Identified by absence during re-scrapes.

**Non-US Coverage**
* **Revelio:** 246 distinct countries, 3635 distinct country-state pairs.

### Phase 2: Data Gathering

* **Revelio Data (Snowflake):**
    * Mar 2024 NC: `TEMPORARY_DATA.ARATHI.PVA2_REVELIO_NC_03`
    * Sept 2024 NC: `TEMPORARY_DATA.ARATHI.PVA2_REVELIO_NC_09`
    * Global Counts: `TEMPORARY_DATA.ARATHI.PVA2_REVELIO_NC_03`
* **LinkUp Data (Snowflake):**
    * Mar 2024 NC: `TEMPORARY_DATA.ARATHI.PVA2_LINKUP_NC_03`
    * Global Counts: `TEMPORARY_DATA.ARATHI.PVA2_LINKUP_COUNTRY_COUNTS`
    * State Counts: `TEMPORARY_DATA.ARATHI.PVA2_LINKUP_COUNTRY_COUNTS`

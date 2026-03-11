---
title: Using weights with BGI data
description: Standard practices for weighting BGI data including postings and profiles data.
parent: index.md
max_lines: 250
source: slab
---

# Using weights with BGI data

As far as weighting, it is standard practice for us to do the following:

1. Postings: we weight using JOLTS
2. Profiles (education): we weight our counts by school x major using state or IPEDS data
3. Profiles (jobs): we weight using state employment data (using NAICS codes) — notably this never seems to dramatically change our results

Before each of our analyses, we also check how representative our education counts are in reference to state data and IPEDS data. This helps us determine when there are discrepancies, or if there are certain schools where (even after weighting) we might not feel confident with our estimates.

## Example using Revelio Lab data

- Without weights, for profiles, what we can say is going to be reflective of the population of people on LinkedIn.
- If we want to get trends/aggregates that are reflective of the broader population, we might use weights. But, we need to be careful that we are not creating an illusion of representativeness by conflating sampling bias with selection into our data.
- Up weighting individuals in profiles doesn't necessarily improve our estimates (and may in fact obfuscate them) if those individuals are unrepresentative of the relevant groups that we're seeking to inflate.
- There are going to be situations where using weights is preferable but we should also be thinking through how to apply them and what we think we're achieving with them.

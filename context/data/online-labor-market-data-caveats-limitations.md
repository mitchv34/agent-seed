---
title: Online labor market data - Caveats & limitations
description: Overview of caveats and limitations of LinkedIn profiles and job postings data used in labor market research.
parent: index.md
max_lines: 250
source: slab
---

# Online labor market data - Caveats & limitations

## LinkedIn Profiles Data

- **Cultural & social factors** - LinkedIn profiles data is drawn from aggregated profile information of LinkedIn's members around the world. It is influenced by how members choose to use the platform, which can vary based on professional, social, and regional culture, as well as overall site availability and accessibility.
- **Selection on observables** - The representativeness of LinkedIn profiles data can also vary based on the penetration of the LinkedIn professional network in each industry, region or country. For this reason, it may skew towards younger, more educated workers, employed in white-collar or more globalized industries.
- **Other biases:**
  - Accuracy of user-generated content (credentials are not checked)
  - Duplicates / fake or dormant profiles
  - Noise accumulation or spurious correlation in large datasets
  - Behaviors associated with LinkedIn business practices (e.g., advertising, new features rollout)
  - **Binary measurement** - For both posting and profile measurement, we only see if a skill is present or not, not the level of skill needed.
  - **Wage measurement** - In most cases, wages can only be estimated through linkage to Glassdoor data which has limited precision. Individual differences between workers in the same job cannot be identified.
  - Differences based on observables such as race, gender, educational background, etc. are not observed.
  - Individual changes in earnings can only be observed when the individual switches jobs or is promoted into a new title.

## Job Postings Data

- **Variability in data scraping ability** - In almost every postings dataset, there is huge time series volatility by source, as some sources become easier or more difficult over time to scrape.
- **Imperfect signal of labor demand:**
  - Postings can represent the intent to hire more than one worker. One post can represent 10 openings for baristas at a Starbucks.
  - Postings can be available when firms don't intend to hire at all ("ghost" postings).
  - Postings are likely skewed towards high-skill jobs.
- **Noise and non-economic changes in advertised salaries:**
  - Due to state/city-level policy changes and pay transparency pushes, the frequency of salary ranges in job postings has increased in many localities.
  - The mandates around salary reporting are loose, so companies can post extremely large salary ranges or hypothetically fake salary ranges.

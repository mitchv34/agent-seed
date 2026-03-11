---
title: Global Job Postings & Profiles Data 🌍
description: Let's explore how the Lightcast job postings and PDL profiles datasets look like outside of the US.
parent: index.md
max_lines: 250
source: slab
---

# Global Job Postings & Profiles Data 🌍

**POC**: Mariano Mamertino
**Last updated**: February 5, 2024

Let's explore how the Lightcast job postings and PDL profiles datasets look like outside of the US.

## LIGHTCAST JOB POSTINGS

We have data for 28 countries excluding the US.

* In 5 countries* (Brazil, Sweden, Poland, Denmark, and Portugal) more than 75% of job postings do not have a standardized job title (i.e., the ISCO classification is a missing value). For Hong Kong, than occupation information is missing for 24-29% of job postings
* For the other 22 countries, the data is quite complete, with less than 5% of job postings not having a standardized occupation.

*I suspect this has to do with the Lightcast models not being able to translate and standardize job titles from Portuguese, Swedish, Danish and Chinese.

### Table 1. % of jobs without standardized occupation information

| Country | 2022 | 2023 |
|---|---|---|
| Brazil | 94.4% | 97.0% |
| Sweden | 89.6% | 90.5% |
| Poland | 85.6% | 83.8% |
| Denmark | 79.2% | 78.1% |
| Portugal | 75.8% | 79.1% |
| Hong Kong | 24.3% | 29.4% |
| Spain | 3.1% | 4.1% |
| United Arab Emirates | 2.2% | 1.8% |
| Qatar | 1.7% | 1.1% |
| Ireland | 1.0% | 4.8% |
| Italy | 0.7% | 0.3% |
| India | 0.6% | 1.8% |
| Philippines | 0.6% | 0.2% |
| Switzerland | 0.2% | 0.1% |
| South Africa | 0.2% | 0.2% |
| Netherlands | 0.2% | 0.1% |
| Belgium | 0.1% | 0.1% |
| Colombia | 0.1% | 0.1% |
| Argentina | 0.1% | 0.1% |
| Austria | 0.1% | 0.1% |
| Germany | 0.1% | 0.1% |
| Great Britain | 0.1% | 0.1% |
| Mexico | 0.1% | 0.0% |
| France | 0.0% | 0.0% |
| Singapore | 0.0% | 0.0% |
| New Zealand | 0.0% | 0.0% |
| Canada | 0.0% | 0.0% |
| Australia | 0.0% | 0.0% |

For those 22 countries with enough standardized occupation information, emerging markets such as the Philippines, Mexico, India, and South Africa have a distribution of job postings that is much more concentrated at the 2-digit ISCO level. This likely reflects the skew in the type of jobs that are usually posted online in those countries (alongside the fact that those are all countries with large informal and agricultural/traditional sectors).

For example, in the Philippines, Mexico, and India the share of job postings classified as \"Business and Administration Professionals\" is 15% or above, while the equivalent figure is only 11% in the UK or Australia.

In table 2 below we benchmark the distribution of job postings data with an assigned ISCO-08 code with total employment (sourced from either Eurostat or ILO).

[Image: Table 2 - Benchmarking against employment data]

### Job title/ occupation standardization accuracy

Mariano Mamertino did some spot checking for Italian, French and Spanish. There are definitely some standardizations that look off but that seems to be the exception rather than the rule. By and large, for job postings the standardization looked reasonable for those languages.

## PDL PROFILES DATA

The profiles/resumes data coming from PDL seems to be much more comprehensive when it comes to geographic coverage. The datasets has at least 1000 unique profile records for 193 countries. Quality and coverage of such data however varies considerably.

### Table 3. Benchmarking PDL \"active\" positions data to employment

[Image: Table 3. Benchmarking PDL \"active\" positions data to employment]

In order to proxy the \"quality\" of a profile, we use a measure of profile's completeness. We look at whether the profile has at least:
* 1 work experience / job record
* 1 education record
* 1 start date associated with the work experience / job record

Table 3 below shows the results benchmarked against the total labor force size coming from public data sources.

* Outside of the US, English-speaking countries are among those with the best data quality. Anglophone markets such as Denmark, Norway and the Netherlands also come towards the top of the ranking.
* 5 out of the 6 largest European economies (namely, UK, France, Italy, Spain, and the Netherlands) have a coverage (using the most stringent quality thresholds) above 10%.
* Brazil and South Africa have a coverage of about 9%, by far the best in their respective regions and similar to that of Italy (and above that of Germany).
* Germany, Mexico, and India are three large economies with sub-par coverage.

### Table 4. Unique profiles counts as a share of total labor force size using different \"quality\" thresholds

| COUNTRY | No threshold | At least 1 work exp. | At least one work exp. & 1 edu. record | At least one work exp., 1 edu. record & 1 work start date |
|---|---|---|---|---|
| united states | 96.0% | 82.1% | 38.8% | 35.0% |
| netherlands | 69.1% | 63.3% | 36.2% | 34.7% |
| australia | 72.3% | 66.1% | 35.4% | 33.5% |
| canada | 71.2% | 63.2% | 33.4% | 31.3% |
| united kingdom | 67.7% | 58.1% | 28.3% | 26.5% |
| belgium | 57.5% | 52.9% | 25.4% | 23.7% |
| denmark | 40.8% | 35.3% | 21.7% | 20.8% |
| norway | 42.3% | 38.3% | 19.7% | 18.7% |
| france | 49.0% | 44.2% | 19.2% | 18.1% |
| switzerland | 44.0% | 38.1% | 18.8% | 18.0% |
| finland | 34.1% | 30.5% | 18.5% | 17.7% |
| new zealand | 34.9% | 29.1% | 16.4% | 15.7% |
| portugal | 40.7% | 34.7% | 16.1% | 14.9% |
| spain | 40.1% | 34.8% | 14.8% | 13.8% |
| sweden | 30.4% | 27.7% | 13.7% | 13.1% |
| italy | 39.5% | 35.3% | 13.5% | 12.3% |
| ireland | 29.4% | 24.1% | 12.4% | 11.9% |
| brazil | 33.8% | 29.1% | 9.5% | 8.8% |
| south africa | 28.6% | 24.4% | 9.4% | 8.5% |
| luxembourg | 20.5% | 14.3% | 7.8% | 7.7% |
| germany | 18.3% | 16.5% | 7.0% | 6.6% |
| czechia | 14.1% | 13.1% | 6.5% | 6.1% |
| chile | 23.0% | 18.9% | 6.2% | 5.7% |
| poland | 10.3% | 9.4% | 5.9% | 5.6% |
| malaysia | 17.3% | 14.3% | 5.8% | 5.4% |
| austria | 10.7% | 10.1% | 5.5% | 5.3% |
| estonia | 10.0% | 8.8% | 4.8% | 4.7% |
| hungary | 10.1% | 8.7% | 4.7% | 4.5% |
| romania | 10.6% | 9.0% | 4.5% | 4.3% |
| turkey | 8.9% | 7.8% | 4.6% | 4.2% |
| singapore | 13.0% | 9.9% | 3.9% | 3.7% |
| mexico | 15.7% | 13.0% | 4.2% | 3.7% |
| malta | 10.2% | 8.5% | 3.7% | 3.6% |
| qatar | 6.9% | 5.5% | 3.4% | 3.3% |
| iceland | 8.6% | 7.3% | 3.4% | 3.2% |
| israel | 7.3% | 6.2% | 3.4% | 3.1% |
| cyprus | 6.6% | 5.9% | 3.2% | 3.1% |
| tunisia | 11.1% | 9.7% | 3.7% | 3.1% |
| barbados | 11.9% | 9.8% | 3.1% | 2.9% |
| india | 9.9% | 7.8% | 3.2% | 2.8% |
| greece | 6.5% | 5.3% | 2.9% | 2.8% |
| lebanon | 4.8% | 4.1% | 2.8% | 2.6% |
| croatia | 6.7% | 5.5% | 2.6% | 2.5% |
| moldova | 8.9% | 7.4% | 2.7% | 2.5% |
| panama | 8.7% | 7.1% | 2.5% | 2.4% |
| maldives | 8.7% | 7.3% | 2.3% | 2.2% |
| uruguay | 9.2% | 7.1% | 2.3% | 2.1% |
| fiji | 8.5% | 7.0% | 2.3% | 2.1% |
| slovakia | 6.0% | 4.9% | 2.2% | 2.1% |
| morocco | 7.7% | 6.3% | 2.5% | 2.1% |
| philippines | 7.0% | 5.6% | 2.4% | 2.1% |
| costa rica | 7.2% | 5.8% | 2.1% | 2.1% |
| saudi arabia | 4.0% | 3.5% | 2.1% | 2.0% |
| serbia | 6.5% | 5.0% | 2.1% | 2.0% |
| trinidad and tobago | 7.2% | 5.6% | 2.0% | 1.9% |
| colombia | 7.2% | 5.6% | 2.0% | 1.8% |
| jamaica | 6.6% | 5.4% | 1.9% | 1.8% |
| guyana | 7.8% | 6.3% | 1.9% | 1.7% |
| slovenia | 5.1% | 4.0% | 1.8% | 1.7% |
| albania | 6.1% | 5.0% | 1.8% | 1.6% |
| namibia | 6.8% | 5.6% | 1.7% | 1.5% |
| ecuador | 8.3% | 6.1% | 1.7% | 1.5% |
| bulgaria | 3.8% | 3.3% | 1.6% | 1.5% |
| taiwan | 3.2% | 2.9% | 1.6% | 1.5% |
| latvia | 4.3% | 3.4% | 1.5% | 1.4% |
| united arab emirates | 4.3% | 3.6% | 1.4% | 1.4% |
| indonesia | 5.7% | 4.7% | 1.5% | 1.4% |
| bosnia and herzegovina | 4.7% | 3.7% | 1.4% | 1.2% |
| belize | 3.1% | 2.7% | 1.2% | 1.1% |
| sri lanka | 3.8% | 2.9% | 1.1% | 1.1% |
| belarus | 3.0% | 2.7% | 1.1% | 1.0% |
| guatemala | 3.6% | 2.8% | 1.1% | 0.9% |
| pakistan | 3.1% | 2.5% | 1.0% | 0.9% |
| gabon | 4.8% | 3.7% | 1.0% | 0.9% |
| argentina | 3.6% | 2.9% | 1.0% | 0.9% |

## SINGAPORE - Deep-dive

**Job postings**
* Global data has ISCO codes as opposed to SOC or ONET for the US
* In the November and August backups, the earliest job postings date to April 2020
* This is true also for the legacy table EMSI
* SG occupation distribution is slightly more concentrated compared to UK
* SG skill distribution is by and large similar to that of UK (with some technical skills over-indexed)
* We don’t have any standardized industry information
* Overall, SG job postings data skews more technical skills and white-collar jobs
* Teaching and health care are significantly under-indexed in the distribution when compared to the UK

**Profiles**
* For both legacy and PDL data, Singapore has a standardization coverage similar to that of the UK
* The distribution across ONET for primary position in PDL is much more skewed: the top 46 ONET broad occupations make up 81% of profiles in SG, but only 38% in the UK

[Images: Singapore deep-dive]

## UK - Deep-dive

[Image: UK deep-dive]

## CODE SNIPPETS

### Job postings counts
[Image: Job postings counts]

### Profiles counts
[Image: Profiles counts]

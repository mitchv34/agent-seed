---
title: LC Postings Data Overview
description: This page provides high-level background information on the Lightcast Postings data.
parent: index.md
max_lines: 250
source: slab
---

# LC Postings Data Overview

This page provides high-level background information on the Lightcast Postings data. For a more practitioner-oriented overview, please refer to the Postings Data section within the Onboarding document.

The Lightcast postings data comes from scraping various job posting websites. Lightcast cleans each post and separates it into two tables, one for general information and one for skills. This data is available for the US, UK, Canada, and Globally.

## Postings

In the table POSTINGS, you can find most of the post information. Each post has its own ID to link it across data sets. Lightcast extracts information from the entire body of the post. This raw data is available in our data set if needed, but because this field is much larger than the others, you should only download it if you absolutely need to.

Most of the time, you should be using pre-cleaned data. This includes:
* Posting company (and its industry)
* Job title
* Various measures of occupation
* Location (city, city longitude/lattitude, county, MSA, state, and country)
* Date posted and expired
* If the job is full- or part-time
* Range of experience needed
* If job is internship
* If job is remote (or hybrid)
* Advertised job salary
* Education levels requested and major (CIP) or certifications

Lightcast scrapes many different job sites and attempts to deduplicate unique posts. You can see the number of reported duplicates and the website sources.

## Postings Skills

In the table POSTINGS_SKILLS, you can see the skills extracted from each post. These are essentially keywords. Skills can be broad (Sales), narrow (Java), or not really skills (Federal Reserve System). They are classified as common, specialized, or certification. Some are also software skills.

## Meta Data

In the table POSTINGS_META, you will see details such as the last updated date and the version of classifiers being used for skills, industries, etc.

## Methodology Document and Data Dictionary

You can use the following Lightcast resources for more information:
* [Data Dictionary](https://docs.lightcast.dev/snowflake/us-postings): Contains all variables and is updated by Lightcast.
* [Job Postings Methodology](https://kb.lightcast.io/en/articles/6957446-job-posting-analytics-jpa-methodology): Describes steps of aggregation, enrichment, deduplication, etc.
* [Lightcast Knowledge Base](https://kb.lightcast.io/en/): FAQs and other documentation.

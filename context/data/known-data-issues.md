---
title: Known Data Issues
description: This is a universal document for known data issues, covering issues with underlying data sets and data cleaning.
parent: index.md
max_lines: 250
source: slab
---

# Known Data Issues

This is a universal document for known data issues. They could be due to issues with the underlying data sets, issues with how the data is cleaned, etc. Where possible, give instructions on what can be done about these issues.

## Lightcast Profiles Person

- People often do not update their personal location, even when it is clear they have moved. When job location exists, it is usually more reliable to trust this record, even for a person's current location.

## Lightcast Profiles Experience

- While experience location is usually more trustworthy than personal location (see above), people often leave out experience location. So companies, such as Deloitte, seem to leave this out systematically. In general, we use experience location when it exists, otherwise we use personal location. While this introduces some error, we think it is an accurate enough estimate to be worthwhile.

## Lightcast Profiles Education

- The algorithm Lightcast used to map SCHOOL_RAW to SCHOOL_NAME often matches to completely unrelated schools. For example, the same raw input "angelo state university" matched most students to the correct school, but some students to ESCP Europe, a school in France.
- Lightcast's major determining algorithm gives each entry at most one major, so double and triple majors are not allowed.
- Lightcast does not attempt to code high school diplomas.
- Lightcast only enters an EDULEVEL when it is explicitly named in the profile.
- Lightcast does not code associate degree/certificate majors well at all.

## Legacy Burning Glass Profiles

- The racial predictions in SENSITIVE.DEI_INPUT_COPY and PERSON_COPY are incorrectly calculated. Use instead: TEMPORARY_DATA.BGI_SOCIAL_PROFILE_IMPUTE_RACE_GENDER.PERSON_COPY_RACE_FINAL
- A person's skills includes skills inferred from occupational history, which are often strange and arbitrary. Filter on IS_INFERRED_FROM_EXPERIENCE equal to FALSE.
- The DEGREE_LEVEL "High school" is only coded for students who get a GED from a school with a valid IPEDS code.

## Lightcast Postings Salary

There are two ways salary may be reported in a job posting: as a range, or as a single level. If the salary is given as a range, the data reports the minimum and maximum salary. If only one salary is reported, then the minimum and maximum are set to that level.

Key notes:
- Most of the time (75-80%), if both the range and `SALARY` are populated, `SALARY` is equal to the midpoint of the range.
- There are instances where the salary range is populated but `SALARY` is not, but no instances of the reverse.
- The rate at which salary info appears in postings has steadily increased starting in 2018, likely due to state- and company-level policy changes.
- Outliers exist in the form of extremely large salary ranges or improbably large or small salaries.

### Salary Coverage by Year

| Year | No Salary Info | Salary Range Only | SALARY Only | Both | When Both, SALARY is Midpoint |
|------|---------------|-------------------|-------------|------|-------------------------------|
| 2010 | 0.84 | 0.02 | 0.00 | 0.14 | 0.76 |
| 2015 | 0.86 | 0.02 | 0.00 | 0.12 | 0.77 |
| 2018 | 0.82 | 0.02 | 0.00 | 0.16 | 0.77 |
| 2019 | 0.79 | 0.03 | 0.00 | 0.18 | 0.77 |
| 2020 | 0.73 | 0.03 | 0.00 | 0.24 | 0.78 |
| 2021 | 0.68 | 0.04 | 0.00 | 0.28 | 0.75 |
| 2022 | 0.65 | 0.04 | 0.00 | 0.31 | 0.80 |

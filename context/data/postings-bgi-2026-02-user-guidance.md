| title | description | parent | max_lines | source |
|---|---|---|---|---|
| Postings BGI_2026_02 User Guidance | User guidance for the cleaned Revelio data found in Snowflake at REVELIO_CLEAN.BGI_2026_02. | index.md | 250 | slab |

# Postings BGI_2026_02 User Guidance

This is the data documentation for the cleaned Revelio data found in Snowflake at `REVELIO_CLEAN.BGI_2026_02`. All of the tables found there have been filtered according to the sample description below and are based on the Dec 2025 sample.

## Quality Filters

1. Length of description >= 100 characters
2. COUNTRY in ('United States', 'United Kingdom', 'Hong Kong', 'Singapore')
3. Modeled language is English (The most common alphabet is Latin)
4. JOBTITLE_RAW is not missing
5. DESCRIPTION length (after removing HTML) is at least 100 characters.

## Data Elements

### Postings Table

All columns with the prefix \"BGI\" have been created by the Data team. These are the columns that should be used for analysis.

| Data Element | Description |
|---|---|
| BGI_CITY | Location Model Output |
| BGI_STATE | Location Model Output |
| BGI_COUNTRY | Location Model Output |
| BGI_HYBRID_FLAG | Location Model Output |
| BGI_REMOTE_FLAG | Location Model Output |
| BGI_MULTILOCATION_FLAG | If the posting listed multiple locations |
| BGI_ONET_CODE, BGI_ONET_NAME | Main ONET code and name from BGI classifier. |
| BGI_TITLE_NAME | Classification of the raw Revelio title into Lightcast title taxonomy |
| BGI_EMPLOYER_ID | This is an ID created from the deduplication of PDL and Revelio employers |
| BGI_EMPLOYER_NAME | This is the name associated with the BGI_EMPLOYER_ID |
| BGI_SALARY_MIN_ANNUALIZED | Annualized figures of BGI_SALARY_MIN. |
| BGI_FULL_TIME | Classification of whether the job advertised is for full time or part time. |

### Skills Table

| Data Element | Description |
|---|---|
| RAW_SKILL_NAME | Raw skill extracted by BGI skill extractor |
| SKILL_NAME | SKILL_NAME from Lightcast skills taxonomy. |
| BGI_SKILL_TYPE | One of \"soft_skill\", \"hard_skill\", \"certification\" |
| BGI_IS_SOFTWARE_OR_TECHNOLOGY | Boolean software or technology flag |

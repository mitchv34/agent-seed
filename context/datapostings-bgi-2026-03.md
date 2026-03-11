| title | description | parent | max_lines | source |
|---|---|---|---|---|
| Postings BGI_2026_03 User Guidance | Model update user guidance for BGI_2026_03, using same data as BGI_2026_02 | | 5000 | |

# Postings BGI_2026_03 User Guidance

Profiles BGI_2026_03 is a **model** update! We are using the same data as in [BGI 2026 02](postings-bgi-2026-02).

## Key Updates

1. **Salary Outlier Fixes**: Used GPT-5 Mini as the consensus model for extracting minimum/maximum salary spans and status.
2. **Company Ticker**: Addition of ultimate parent ticker and exchange information using PDL data, `yfinance`, and `gpt-5-mini` verification.
3. **Occupation Improvements**: Semantic search on Revelio raw titles against Lightcast standard titles; Binary Encoder rerun on a larger training set.
4. **Skills**:
   - BGI Ontology Database on Snowflake.
   - Basic Skill Metrics.
   - BGI Skill Descriptions generated using GPT-5.2 with web search grounding.
5. **Majors**: New CIP classification (CIP6, CIP4, CIP2) using OpenAI `text-embedding-3-large` for semantic mapping.

## Data Elements

### Postings Table additions/changes

| Data Element | Description |
|---|---|
| BGI_CIP6_2020 | CIP6 classification for majors |
| BGI_CIP6_2020_NAME | CIP6 name |
| BGI_ULTIMATE_PARENT_TICKER | Ticker for ultimate parent company |
| BGI_ULTIMATE_PARENT_EXCHANGE | Exchange for ultimate parent company |

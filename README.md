# Who Votes? U.S. Voter Turnout by Age, Race and Sex, 2004 to 2024

Data files for my INFO 5602 (Information Visualization, CU Boulder) individual dashboard project. A Grafana Cloud dashboard reads these CSV files through the Infinity data source.

## Source

U.S. Census Bureau, Current Population Survey, Voting and Registration Supplement. Table A-1, "Reported Voting and Registration by Race, Hispanic Origin, Sex and Age Groups: November 1964 to 2024" (historical voting tables, https://www.census.gov/topics/public-sector/voting.html).

Cross-checked against Tables A-4, A-6, A-7 and A-9 from the same series.

## Definitions

- **Turnout:** percent of U.S. citizens aged 18 and over who reported voting in the November election.
- **Exception:** the women and men comparison uses the total voting-age population, because Table A-1 gives rates by sex only on that basis.
- **Gaps** are in percentage points: the higher group's rate minus the lower group's rate.
- **Presidential years:** 2004, 2008, 2012, 2016, 2020, 2024. **Midterm years:** 2006, 2010, 2014, 2018, 2022.

## Files in `data/`

| File | Contents |
|---|---|
| `turnout_by_age.csv` | Turnout (%) by age group: 18 to 24, 25 to 44, 45 to 64, 65 and over, and all citizens |
| `age_gap_by_election.csv` | 65+ turnout minus 18 to 24 turnout, split into presidential and midterm columns |
| `turnout_by_race.csv` | Turnout (%) for white non-Hispanic, Black, Hispanic or Latino and Asian citizens |
| `race_gaps.csv` | White non-Hispanic turnout minus each group's turnout (points) |
| `women_minus_men.csv` | Women's turnout minus men's (points), total voting-age population |
| `gaps_presidential_vs_midterm.csv` | Average of each gap across presidential years and across midterm years |
| `relative_turnout.csv` | Average 18 to 24 and 65+ turnout by election type, and young voters per 100 older voters |
| `latest_values.csv` | Headline numbers for the dashboard |

## Limitations

- Turnout is self-reported in a survey taken after each election and runs higher than official vote counts.
- Race groups are single-race. Hispanic or Latino can be of any race, so groups overlap.
- Census race categories changed in 2003, so the data starts with 2004.
- The 2026 midterm results are expected from the Census Bureau in 2027.

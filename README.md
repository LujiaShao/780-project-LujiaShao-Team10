# Emergency department visit times across U.S. regions

A patient discharged from an emergency department (ED) at a typical Northeast hospital spent about **195 minutes** from arrival to departure. In the Midwest, the comparable figure was **133 minutes**. Our BA780 team at Boston University’s Questrom School of Business asked whether the Northeast’s longer visits also appeared when we compared hospitals of similar size.

[Explore the analysis notebook](https://github.com/LujiaShao/780-project-LujiaShao-Team10/blob/main/A10_Hospital_Operational_Efficiency_for_Elderly_Across_U_S_Regions.ipynb)

## What we found

The Northeast had the longest median visit in each of the three bed-count groups. Even among hospitals with fewer than 100 beds, the Northeast median was 23 minutes longer than the Midwest median.

| Hospital size | Northeast | Midwest | South | West |
| --- | ---: | ---: | ---: | ---: |
| Under 100 beds | 140 min | 117 min | 120 min | 125 min |
| 100–299 beds | 197 min | 169 min | 162 min | 171 min |
| 300 or more beds | 219 min | 189 min | 184 min | 199 min |

Each cell is the median of hospitals’ reported visit-time scores for discharged ED patients (CMS measure OP-18b). A hospital is the unit of comparison. The underlying scores cover eligible patients across ages. We used population and Medicare enrollment data to put these comparisons in the context of an aging population.

## How we compared hospitals

We combined public data on hospital performance and bed counts from the Centers for Medicare & Medicaid Services (CMS), and grouped hospitals by region and size in Python. We retained missing scores and their footnotes in the cleaned data, then calculated medians using reported scores. The notebook’s Question 14 includes the hospital count for each group.

## My contribution

I prepared rural–urban data for the team. Census tracts and counties use different identifiers, so I standardized the county FIPS codes, preserved leading zeros, and joined each tract to its county classification. I kept every tract in the output and flagged unmatched records for review. I also helped write the conclusion and limitations, especially what we could infer from the regional comparisons.

## What a hospital team could do next

Bed count alone leaves a gap in every size group. A Northeast hospital could start with similar-sized peers, then compare hourly arrivals, staffing by shift, and the time admitted patients spend waiting for a bed. Those measures would help test where delays arise. Our regional comparisons identify a place to investigate, but cannot establish the cause of a longer visit.

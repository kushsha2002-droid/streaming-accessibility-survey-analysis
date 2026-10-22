# Streaming Services Accessibility & Usability Survey Analysis

An end-to-end analysis of a 337-response survey on how accessible and usable eight major streaming services are, from data cleaning through rankings, comment analysis and a full report with 71 charts.

> **Privacy note:** This repo contains aggregate results only. The public report omits all verbatim respondent comments (about 1,200 responses across 18 open-ended questions); theme counts and sentiment are kept. No survey exports or respondent details are included.

**Read the public report:** [Download the Word report (.docx, 76 pages)](https://github.com/kushsha2002-droid/streaming-accessibility-survey-analysis/raw/main/Streaming_Accessibility_Survey_Report_Public.docx)

## Overview
- **Goal:** Compare streaming services on accessibility and usability and find the biggest pain points for users, with a focus on audio description and other assistive features.
- **Data:** A SurveyMonkey survey with 337 responses and 41 questions (rating matrices, closed-ended questions and 18 open-ended comment questions).
- **Services compared:** Amazon Prime, Apple TV+, Disney+, HBO Max, Hulu, Netflix, Paramount+ and Peacock. A ninth service, YouTube TV, was written up in a separate mini report.
- **Deliverable:** A Word report (111 pages in the full version, 76 pages in the public version without verbatim comments) with 71 charts, per-question comment themes, an overall ranking and 28 pairwise service comparisons, plus a mini report with recommendations for each platform.

## Key findings
- **Apple TV+ ranks first (3.84) and Paramount+ last (3.17).**
- **Netflix (3.61) and HBO Max (3.58) are within 0.03 of each other,** close enough that one more wave could swap them.
- **Audio description activation is the biggest pain point.** It had the widest gap of any aspect measured (1.20 points between the best and worst service) and audio description discovery and activation dominate the open-ended complaints.
- **Independent volume control is the weakest aspect overall:** it is the lowest-scoring aspect for six of the eight services and falls below the neutral midpoint for four.
- **The most common request is standardization:** one consistent way to find and turn on audio description everywhere.

![Overall ranking chart](images/overall_ranking.png)

*Mean overall rating on a 1-5 scale, n = 337. The horizontal axis starts at 2.6 to make differences between services visible.*

## Approach
1. **Pulled summary data** from SurveyMonkey for ratings and closed-ended questions, and used it as the source of truth for every chart and table.
2. **Compiled open-ended responses** from per-question SurveyMonkey exports and checked each question's response count against the export's own total.
3. **Applied a documented filtering rule:** only literal "N/A" answers are excluded; short substantive answers such as "None" or "nothing" are kept and counted.
4. **Coded open-text answers into themes** (for example audio description activation, volume control, navigation) and scored sentiment using each question's framing, so a response that names a problem on a "most frustrating challenge" question counts as negative.
5. **Recoded open-text country answers** into US / non-US, with state and city answers counted as US.
6. **Verified before publishing:** 41 questions, 71 charts, all 72 rating means present, 28 pairwise comparisons, and every comment count matching its source data.

## Judgment calls
- **Sentiment scoring is framing-based:** on a "most frustrating challenge" question, a response that names a problem counts as negative even without negative wording. The method is described in the report's method section.
- **Country recoding** treats Puerto Rico and sub-national answers as US.

## Skills demonstrated
Survey data analysis, thematic coding of open-ended responses, descriptive statistics and ranking, data visualization, data quality verification, and report writing for non-technical readers.

## Tools
SurveyMonkey, Microsoft Word, Microsoft Excel

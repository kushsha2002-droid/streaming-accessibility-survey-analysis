# Streaming Services Accessibility & Usability Survey Analysis

An end-to-end analysis of a 337-response survey on how accessible and usable eight major streaming services are, from data cleaning through rankings, comment analysis and a full report with 71 charts.

> **Privacy note:** This repo contains aggregate results only. The public report omits all verbatim respondent comments (about 1,200 responses across 18 open-ended questions); theme counts and sentiment are kept. No survey exports or respondent details are included.

**Read the public report:** [Streaming_Accessibility_Survey_Report_Public.docx](Streaming_Accessibility_Survey_Report_Public.docx)

## Overview
- **Goal:** Compare streaming services on accessibility and usability and find the biggest pain points for users, with a focus on audio description and other assistive features.
- **Data:** A SurveyMonkey survey with 337 responses and 41 questions (rating matrices, closed-ended questions and 19 open-ended text questions).
- **Services compared:** Amazon Prime, Apple TV+, Disney+, HBO Max, Hulu, Netflix, Paramount+ and Peacock. A ninth service, YouTube TV, was written up in a separate mini report.
- **Deliverable:** A Word report (111 pages in the full version, 76 pages in the public version without verbatim comments) with 71 charts, per-question comment themes, an overall ranking and 28 pairwise service comparisons, plus a mini report with recommendations for each platform.

## Key findings
- **Apple TV+ ranks first (3.84) and Paramount+ last (3.17).** Rankings were identical across two survey waves.
- **Netflix (3.61) and HBO Max (3.58) are within 0.03 of each other,** close enough that one more wave could swap them.
- **Audio description activation is the biggest pain point.** It had the widest gap of any aspect measured (1.20 points between the best and worst service) and was the most-mentioned theme in open-ended comments across every service.
- **Independent volume control is the weakest aspect overall,** below the neutral midpoint for five of the eight services.
- **The most common request is standardization:** one consistent way to find and turn on audio description everywhere.

![Overall ranking chart](images/overall_ranking.png)

*Mean overall rating on a 1-5 scale, n = 337. The horizontal axis starts at 2.6 to make differences between services visible.*

## Approach
1. **Pulled summary data** from the SurveyMonkey API for ratings and closed-ended questions, and used it as the source of truth for every chart and table.
2. **Parsed open-ended responses** from per-question PDF exports with Python (`pdfplumber`), stripping page furniture and checking each question's response count against the export's own total.
3. **Applied a documented filtering rule:** only literal "N/A" answers are excluded; short substantive answers such as "None" or "nothing" are kept and counted.
4. **Coded open-text answers into themes** (for example audio description activation, volume control, navigation) and scored sentiment using each question's framing, so a response that names a problem on a "most frustrating challenge" question counts as negative.
5. **Recoded open-text country answers** into US / non-US, with state and city answers counted as US.
6. **Verified before publishing:** 41 questions, 71 charts, all 72 rating means present, 28 pairwise comparisons, and every comment count matching its source data. This caught and fixed a recoding bug that had silently labeled Australia and Austria as United States.

## Judgment calls
- **Sentiment scoring is framing-based,** which pushes percentages higher than a plain keyword count (one question moved from 30% negative under keyword counting to 98% under framing-based scoring). Both methods are described in the report's method section.
- **Country recoding** treats Puerto Rico and sub-national answers as US.

## Skills demonstrated
Survey data analysis, API data retrieval, text extraction and cleaning with Python, thematic coding of open-ended responses, descriptive statistics and ranking, data visualization, data quality verification, and report writing for non-technical readers.

## Tools
SurveyMonkey (API), Python (`pdfplumber`, `matplotlib`), Microsoft Word

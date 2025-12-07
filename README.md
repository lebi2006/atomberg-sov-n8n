#Atomberg Smart Fan: Share of Voice Analysis Workflow

##Overview

This repository contains an n8n workflow that analyzes Atomberg’s Share of Voice (SoV) on Reddit for the keyword “smart fan India”. It counts mentions of Atomberg and competitors, performs sentiment analysis, and calculates weighted SoV.

##Workflow Structure##
**1. HTTP Request Node**

-Fetches recent Reddit posts containing keywords like "smart fan India"

-Output: JSON data with post titles, self-text, and upvotes

**2. Extract Post Data (JS Node)**

Flattens JSON and extracts:

-title

-text

-upvotes

**3. Brand Mention Count (JS Node)**

-Counts mentions of brands: Atomberg, Havells, Crompton, Orient, Bajaj

-Adds brandCounts field to each post

**4. Sentiment Analysis (JS Node)**

-Calculates a simple sentiment score based on positive/negative keywords

-Adds sentiment field

**5. Share of Voice Calculation (JS Node)**

-Computes weighted mentions (by upvotes + positive sentiment)

-Outputs totals per brand and Atomberg SoV

##Workflow Screenshots##
**Full Workflow**

<img width="1917" height="965" alt="image" src="https://github.com/user-attachments/assets/bd8ebc72-d063-43bb-a536-471cbfa36708" />

**Output (SoV Calculation)**

<img width="1909" height="959" alt="image" src="https://github.com/user-attachments/assets/d12b6fa9-58ca-40c1-9e34-48bb3e2db9c8" />

##Recommendations to Atomberg Team##

**Based on the analysis of Reddit posts:**

-Atomberg leads SoV with 48.14% among competitors.

-Engagement is strong for posts mentioning Atomberg; maintain active interaction with the community.

-Focus on India-specific content for “smart fan” discussions.

-Monitor competitors like Orient and Havells for trending topics.

-Use positive sentiment phrases in campaigns to further strengthen brand perception.

**Tech Stack**

-n8n – Workflow automation

-HTTP Request Node – Fetch Reddit posts

-Code (JS) Nodes – Extract data, count mentions, analyze sentiment, calculate SoV

-JSON Output – Store structured data for reporting

-Fully free → no paid APIs or credentials required

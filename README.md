# AI-Powered Job Matching System

## Problem Solved
Job seekers waste hours manually browsing job boards and evaluating 
listings that don't match their skills. This system automates daily 
job hunting — fetching, scoring, and delivering only relevant 
opportunities every morning.

## How It Works
1. Scheduled trigger fires every morning
2. Fetches live job listings from We Work Remotely RSS feed
3. Deduplication check against previously logged jobs
4. Claude AI scores each job 1-10 for relevance
5. Results logged to Google Sheets
6. Morning digest email delivered with top opportunities

## Workflow Architecture
```
Schedule Trigger → Get Existing Jobs (Google Sheets) → HTTP Request (RSS) → Parse Jobs → Claude API → Format Row → Append to Sheets → Build Email → Gmail
```

## Tech Stack
- **Orchestration:** n8n
- **Job Source:** We Work Remotely RSS feed
- **AI:** Anthropic Claude API (claude-sonnet-4)
- **Logging:** Google Sheets
- **Email:** Gmail
- **Language:** JavaScript (n8n Code nodes)

## Key Features
- Fully automated daily execution
- Deduplication — never shows the same job twice
- AI relevance scoring 1-10 with reasoning
- Apply recommendation — true or false
- Google Sheets audit log of all scored jobs
- Clean HTML email digest with apply links
- Configurable skill profile in Claude prompt

## Sample Output
Each job scored with:
- Relevance Score (1-10)
- Reason for score
- Apply recommendation
- Direct link to job posting

## Business Value
- Eliminates hours of daily manual job searching
- Delivers pre-scored opportunities directly to inbox
- Fully configurable for any skill profile
- Scales to multiple job boards simultaneously

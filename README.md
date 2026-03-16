# Automated AI Sales Reporting Engine

## Problem Solved
Sales teams waste hours every week manually pulling data, writing 
reports, and distributing them via email. This system automates 
the entire reporting cycle — from data extraction to email delivery 
— with zero human involvement.

## How It Works
1. Scheduled trigger fires every morning
2. Reads sales data from Google Sheets automatically
3. Data formatted and sent to Claude AI
4. Claude generates professional HTML report with executive 
   summary, observations, and recommendations
5. Report delivered via Gmail automatically

## Workflow Architecture
```
Schedule Trigger → Google Sheets → Code (format data) → Claude API → Gmail (send report)
```

## Tech Stack
- **Orchestration:** n8n
- **Data Source:** Google Sheets
- **AI:** Anthropic Claude API (claude-sonnet-4)
- **Email:** Gmail
- **Language:** JavaScript (n8n Code nodes)

## Key Features
- Fully automated daily execution
- AI-generated executive summary
- Key observations and trend analysis
- Actionable recommendations
- Professional HTML email formatting
- Zero manual steps required

## Report Sections
| Section | Description |
|---|---|
| Executive Summary | High level overview of performance |
| Key Observations | Notable trends and patterns |
| Recommendations | Actionable next steps |

## Business Value
- Eliminates 2-3 hours of weekly manual reporting
- Delivers insights every morning before business hours
- Consistent professional formatting every time
- Scales to any data structure or reporting frequency

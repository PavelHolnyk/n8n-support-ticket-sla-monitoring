# AI Ticket Routing & SLA Monitoring for an Online Store

**n8n · OpenAI · Gmail · Google Sheets · Slack**

Automatic email triage, ticket assignment and three-level escalation for the HouseBox online-store scenario.

## Problem

Customer requests required manual reading, categorization, assignment and deadline tracking. A shared inbox made it difficult to prioritize urgent issues and keep a clear view of overdue tickets. A generic acknowledgement did not count as a meaningful first response.

## Solution

**Track 1 — Ticket intake**

Gmail → AI classification → category / priority / owner / SLA / summary / sentiment → spam check → Google Sheets ticket log → Slack notification.

**Track 2 — SLA monitoring**

A scheduled watcher checks open tickets every five minutes and sends escalating alerts.

| Level | Action |
| --- | --- |
| L0 | Reminder to the ticket owner |
| L1 | Slack notification to the support team lead |
| L2 | Email to the business owner |

Categories: support, returns, billing, sales and spam.

## Results

- **Faster routing:** Gmail is checked every **1 minute**, so eligible tickets can be classified and assigned in the next trigger cycle.
- **SLA control:** open tickets are checked every **5 minutes**. First-response targets are **P1: 30 min · P2: 60 min · P3: 120 min · P4: 480 min**.
- **Less manual triage:** classification, owner assignment, ticket logging and repeated deadline checks are handled by the workflow.
- **Capacity planning:** the case is designed around approximately **900 tickets per month**.
- **Estimated time savings:** at that assumed volume, the Notion case estimates **45–52 manager hours per month**, approximately **6–7 working days**. This is a scenario estimate, not a measured production result.

## Tech Stack

n8n, OpenAI API, Gmail API, Google Sheets API, Slack API, Structured Output Parser, JSON Schema, JavaScript expressions.

## Demo & Case Study

- [Watch the demo](https://youtu.be/jhmWyUoOIms)
- [Read the full Notion case](https://tangy-whitefish-6d0.notion.site/248c12839d0682fbb99c01ad2bafa261)

## Author

**Pavlo Holnyk — AI Automation & AI Agents**

[Portfolio](https://tangy-whitefish-6d0.notion.site/408c12839d06816f9e61ff1aa7392587) · [LinkedIn](https://www.linkedin.com/in/pavlo-holnyk/) · [Upwork](https://www.upwork.com/freelancers/~011ee82fd5725aa92e)

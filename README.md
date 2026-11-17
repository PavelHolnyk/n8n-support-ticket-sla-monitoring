# Automated Ticket Routing and Response-Time Monitoring

Portfolio project by Pavlo Holnyk, based on the HouseBox online-store scenario.

## Overview

An n8n support automation for AI email triage, ticket assignment, notifications and monitoring the first meaningful response.

## Workflow

Gmail -> AI classification -> spam check -> Google Sheets ticket log -> Slack notification to the owner.

A separate scheduled branch checks open tickets every five minutes and applies L0 owner reminders, L1 team-lead notifications and L2 escalation emails to the business owner.

Classification includes category, P1-P4 priority, owner, SLA, summary, reasoning and sentiment. Categories cover support, returns, billing, sales and spam.

## Stack

n8n, OpenAI API, Gmail API, Google Sheets API, Slack API, Structured Output Parser, JSON Schema and JavaScript expressions.

## Demo and case study

- [Case study in Notion](https://tangy-whitefish-6d0.notion.site/248c12839d0682fbb99c01ad2bafa261)
- [Video demo](https://youtu.be/jhmWyUoOIms)

## Repository contents

Project documentation only. Workflow exports and source files have not been added. Ticket volume and time-saving estimates are not presented as independently verified results.

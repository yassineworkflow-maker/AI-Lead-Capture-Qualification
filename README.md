# AI Lead Capture & Qualification

An AI-powered lead capture and qualification workflow built with n8n.

This automation receives lead information through a webhook, analyzes and qualifies the lead using an AI Agent, evaluates the qualification result, saves qualified leads to Google Sheets as a CRM, and automatically sends a personalized qualification email through Gmail.

## Workflow Overview

The workflow follows this process:

1. Receive lead data through a Webhook.
2. Send the lead information to an AI Agent.
3. Analyze and qualify the lead using an OpenAI model.
4. Return structured qualification data.
5. Check whether the lead is qualified.
6. Save qualified leads to Google Sheets.
7. Send a personalized follow-up email through Gmail.

## Architecture

```text
Webhook
   ↓
AI Lead Qualification
   ↓
Is Lead Qualified?
   ↓
Save Qualified Lead to CRM
   ↓
Send Qualification Email

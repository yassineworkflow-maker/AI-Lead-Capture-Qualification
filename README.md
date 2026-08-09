# AI Lead Capture & Qualification

> An AI-powered lead qualification and follow-up automation built with n8n, OpenAI, Google Sheets, and Gmail.

## Overview

This project automates the lead qualification process from initial submission to follow-up.

The workflow receives lead information through a Webhook, uses an AI Agent to analyze and qualify the lead based on predefined business criteria, generates structured qualification data, evaluates whether the lead meets the qualification requirements, stores qualified leads in a Google Sheets-based CRM, and automatically sends a follow-up email through Gmail.

The goal is to reduce manual lead screening, improve response speed, and ensure that qualified prospects are processed consistently.

## Workflow Preview

![AI Lead Capture & Qualification Workflow](AI%20Lead%20Capture%20%26%20Qualification.png)

## Business Use Case

This automation can be used by businesses that receive leads through websites, forms, landing pages, or other digital channels.

Instead of manually reviewing every lead, the automation can:

- Capture incoming lead information
- Analyze the lead using AI
- Evaluate business requirements and budget
- Assign qualification information
- Determine whether the lead is qualified
- Store qualified leads in a centralized CRM-style Google Sheet
- Send an automated follow-up email

This allows sales teams to focus their time on higher-value prospects instead of manually processing every incoming lead.

## Workflow Architecture

```text
Lead Submission
      ↓
Receive Lead
      ↓
AI Lead Qualification
      ↓
Structured Qualification Output
      ↓
Is Lead Qualified?
      ↓
Save Qualified Lead to CRM
      ↓
Send Qualification Email

# AI Lead Capture & Qualification

> An AI-powered lead qualification and follow-up automation built with n8n, OpenAI, Google Sheets, and Gmail.

## Overview

This project demonstrates an end-to-end AI-powered lead qualification system designed to automate one of the most repetitive stages of a sales process: receiving, analyzing, qualifying, organizing, and following up with potential customers.

Instead of manually reviewing every incoming lead, the workflow receives lead data through a webhook, analyzes the prospect using an AI Agent, applies qualification criteria, generates structured results, and automatically processes qualified leads.

Qualified leads are then stored in a centralized Google Sheets CRM and receive a personalized follow-up email through Gmail.

The workflow is designed as a reusable automation architecture that can be adapted to different businesses, qualification rules, CRM systems, and communication channels.

---

## Business Problem

Sales teams often spend significant time manually reviewing incoming leads, deciding which prospects are worth pursuing, updating CRM records, and sending follow-up messages.

This creates several common problems:

- Manual lead screening
- Inconsistent qualification decisions
- Delayed follow-up
- Repetitive data entry
- Leads being overlooked
- Time spent on low-quality prospects

This automation addresses these problems by moving the initial qualification and follow-up process into an automated workflow.

---

## Solution

The system creates an automated lead qualification pipeline:

**Lead Submission → AI Analysis → Qualification → Decision → CRM Storage → Personalized Follow-up**

The AI Agent evaluates the incoming lead according to defined business requirements and produces structured qualification data.

Only qualified leads continue to the CRM and follow-up stage, allowing the sales process to focus attention on higher-value prospects.

---

## Workflow Preview

![AI Lead Capture & Qualification Workflow](./workflow.png)

---

## Key Features

- Capture incoming leads automatically through a Webhook
- Analyze prospect information using an AI Agent
- Evaluate leads according to business requirements
- Consider qualification factors such as business needs and budget
- Generate structured qualification results
- Assign qualification information and priority
- Automatically determine whether a lead is qualified
- Store qualified leads in a centralized Google Sheets CRM
- Send personalized follow-up emails through Gmail
- Reduce repetitive manual sales operations
- Create a workflow architecture that can be adapted to different businesses

---

## How It Works

### 1. Receive Lead

A Webhook acts as the entry point for the automation.

Lead information can come from sources such as:

- Website forms
- Landing pages
- Lead generation systems
- External applications
- Other automation workflows

The incoming information is passed into the qualification pipeline.

---

### 2. AI Lead Analysis

The lead data is sent to an AI Agent.

The AI analyzes the available information and evaluates the prospect according to predefined qualification criteria.

This allows the workflow to perform an initial qualification automatically instead of relying entirely on manual review.

---

### 3. Structured Qualification

The AI response is converted into structured data using a Structured Output Parser.

This makes the qualification result easier for the workflow to process reliably.

The structured result can contain information such as:

- Qualification status
- Qualification score
- Priority
- Reasoning
- Lead information
- Other business-specific fields

---

### 4. Qualification Decision

The workflow evaluates the structured qualification result using a decision step.

The system determines whether the lead meets the required qualification criteria.

This creates a clear separation between qualified and non-qualified prospects.

---

### 5. CRM Storage

Qualified leads are stored in Google Sheets.

The Google Sheet acts as a lightweight CRM-style database containing the information required by the sales process.

This provides a centralized place where qualified prospects can be reviewed and managed.

---

### 6. Automated Follow-up

After a lead is qualified and stored, the workflow sends a personalized follow-up email through Gmail.

This allows the business to respond to qualified prospects automatically and reduce delays between qualification and communication.

---

## Workflow Architecture

```text
Incoming Lead
      │
      ▼
    Webhook
      │
      ▼
   AI Agent
      │
      ▼
Structured Output
      │
      ▼
Qualification Decision
      │
      ├── Not Qualified
      │
      └── Qualified
              │
              ▼
        Google Sheets CRM
              │
              ▼
       Personalized Email
              │
              ▼
             Gmail

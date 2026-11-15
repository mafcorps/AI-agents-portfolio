# Agent 09 — The Polite Debt Collector

**AI-Powered Payment Reminder Assistant**

## Overview

The Polite Debt Collector is an AI-powered accounts receivable assistant designed to identify overdue invoices, calculate payment delays, classify urgency levels and generate professional, personalized payment reminder emails.

The agent helps businesses streamline their payment follow-up process while maintaining a professional and respectful relationship with customers.

Its communication style becomes progressively firmer depending on how long an invoice has been overdue.

## Key Features

- **CSV Invoice Processing:** Reads invoice records from uploaded CSV files.
- **Overdue Invoice Detection:** Identifies unpaid invoices that have passed their due dates.
- **Automatic Overdue Calculation:** Calculates the number of days each invoice is overdue.
- **Four Urgency Levels:** Classifies overdue invoices according to payment delay.
- **Personalized Email Generation:** Creates payment reminder drafts using actual invoice and customer information.
- **Multilingual Support:** Generates reminders in the language selected by the user.
- **Payment Status Validation:** Excludes paid, cancelled and refunded invoices.
- **Data Accuracy Controls:** Prevents invented invoice details, payment terms, fees and unsupported legal claims.

## Urgency Classification

| Level | Category | Communication Style |
|---|---|---|
| Level 1 | Friendly Reminder | Polite and helpful |
| Level 2 | Professional Follow-up | Direct and professional |
| Level 3 | Firm Reminder | Firm and explicit |
| Level 4 | Urgent Payment Notice | Strong but respectful |

## Workflow Architecture

The agent is built using n8n and follows this workflow:

1. **Form Trigger** — Collects company information, payment settings and the invoice CSV file.
2. **Extract from File** — Extracts invoice records from the uploaded CSV.
3. **Edit Fields** — Maps and prepares the invoice and company information.
4. **Code in JavaScript** — Validates invoice statuses, processes due dates, calculates overdue days and assigns urgency levels.
5. **IF Node** — Separates invoices eligible for payment reminders from invoices requiring no reminder or manual review.
6. **Basic LLM Chain** — Generates personalized payment reminder emails.
7. **OpenAI Chat Model** — Powers the email generation.
8. **Form Ending** — Displays the generated results.

## User Inputs

The agent accepts:

- Invoice CSV file
- Company name
- Company email
- Currency
- Default payment terms
- Reminder language

The CSV contains invoice-level information such as invoice number, customer details, invoice date, due date, amount and payment status.

## Generated Output

For eligible invoices, the agent generates:

- Customer email address
- Professional email subject
- Personalized greeting
- Invoice reference
- Outstanding amount and currency
- Original due date
- Number of overdue days
- Payment request
- Professional closing
- Urgency classification

Invoices that are not eligible for reminders are identified with an explanation instead of receiving an email draft.

## Accuracy and Safety Controls

The agent follows strict rules:

- Never invent invoice numbers, customer details, amounts or dates.
- Never generate reminders for invoices that are already paid or cancelled.
- Never invent bank details, payment links or payment methods.
- Never introduce unauthorized late fees, interest or legal threats.
- Never claim that an email has been sent.
- Flag missing or invalid invoice information for human review.
- Generate drafts for human review before sending.

## Technology Stack

- **Automation:** n8n
- **AI Model:** OpenAI GPT-4.1
- **Data Processing:** JavaScript
- **Input Format:** CSV
- **Interface:** n8n Forms

## Testing and Validation

The agent was tested using a sample invoice dataset containing multiple invoice records.

The final validation included an overdue invoice with the following details:

- Invoice Number: INV-2026-1041
- Customer: Northstar Dental Clinic
- Amount: €1,250.00
- Due Date: 15 October 2026
- Days Overdue: 31
- Urgency: Level 4 — Urgent Payment Notice

The generated email correctly used the supplied invoice information, calculated overdue period and urgency classification.

Testing also covered invoice eligibility and data accuracy controls.

**Final Test Result: Successfully validated for the tested scenario.**

## Current Limitations

- The current version processes uploaded CSV files rather than connecting directly to accounting software.
- Generated emails are drafts and are not automatically sent.
- Invoice data and payment statuses depend on the accuracy of the uploaded file.
- Human review is required before sending payment reminders.

## Future Improvements

Potential future developments include:

- Integration with accounting platforms.
- Automatic invoice synchronization.
- Gmail and Outlook integration.
- Automated email delivery with approval controls.
- Scheduled payment follow-ups.
- Customer payment history and tracking.
- Payment reconciliation.

## Project Status

**Completed — Built and tested.**

Agent 09 is part of the AI Agents Portfolio, a collection of specialized AI agents designed to automate practical business tasks.

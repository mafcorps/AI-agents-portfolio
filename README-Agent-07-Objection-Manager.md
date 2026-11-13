# Agent 07 — Objection Manager

**AI Sales Objection Coach**

## Overview

Objection Manager is an AI-powered sales assistant designed to help sales professionals understand customer objections and develop effective responses.

The agent analyzes a customer's objection, considers the product or service being offered, and uses the company's supplied sales history to generate three personalized strategies for handling the situation.

Its goal is to help sales teams respond more confidently, handle objections strategically, and move conversations forward without relying on generic sales scripts.

## Key Features

- **Objection Analysis:** Identifies the underlying reason behind a customer's objection.
- **Sales History Analysis:** Uses previous sales examples supplied by the user to identify relevant approaches.
- **Three Response Strategies:** Generates exactly three different strategies for handling each objection.
- **Ready-to-Use Responses:** Provides practical responses that sales professionals can adapt and use.
- **Strategy Recommendation:** Identifies the most suitable approach based on the available context.
- **Follow-up Suggestions:** Recommends the next step in the sales conversation.
- **Sales Coaching:** Provides additional advice to improve the salesperson's approach.
- **Evidence-Based Recommendations:** Avoids inventing customer results, product capabilities, or commercial claims.

## Workflow Architecture

The agent was built using n8n.

**Workflow:**

Form Trigger → Edit Fields → Basic LLM Chain → OpenAI Chat Model → Form Ending

The user submits the customer objection and relevant sales information through an n8n form. The workflow organizes the information and sends it to the language model for analysis and strategy generation.

## User Inputs

The agent collects the following information:

| Input | Description |
|---|---|
| Customer Objection | The customer's specific objection |
| Customer / Company Name | Name of the prospect or company |
| Product / Service Offered | The product or service being sold |
| Customer Profile | Relevant information about the customer |
| Sales Stage | Current stage of the sales process |
| Previous Conversation | Context from previous interactions |
| Company Sales History | Examples of previous objection-handling situations |
| Preferred Response Tone | Professional, Friendly, Confident, Consultative, or Persuasive |
| Additional Context | Any other relevant information |

## Generated Output

For every submission, the agent generates:

1. **Objection Breakdown** — Analysis of the customer's concern and its possible underlying motivations.
2. **Historical Sales Insights** — Relevant lessons from the supplied sales history.
3. **Three Recommended Strategies** — Three distinct approaches, each including:
   - Objective
   - Recommended approach
   - Ready-to-use response
   - Why the strategy may work
   - When to use it
   - Confidence level
4. **Recommended Strategy** — The approach considered most suitable for the situation.
5. **Suggested Follow-up** — A recommended next step in the conversation.
6. **Sales Coach Advice** — Practical guidance for the salesperson.

## Accuracy and Commercial Controls

The agent follows strict rules to improve the reliability of its recommendations:

- Does not invent customer results, testimonials, statistics, or business outcomes.
- Does not promise unsupported product capabilities or performance improvements.
- Does not automatically recommend discounts.
- Distinguishes documented sales history from general sales assumptions.
- Does not interpret meetings or positive discussions as confirmed sales.
- Avoids unsupported claims about customer adoption.
- Labels pilots and phased implementations as proposals requiring commercial and operational confirmation.
- Adjusts confidence levels according to the strength of the available evidence.

## Technology Stack

- **n8n

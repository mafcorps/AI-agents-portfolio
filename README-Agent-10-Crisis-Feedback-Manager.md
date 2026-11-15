# Agent 10 — Crisis Feedback Manager

**AI-Powered Review Crisis Management**

## Overview

Crisis Feedback Manager is an AI-powered customer reputation management assistant designed to help businesses handle negative customer reviews professionally and efficiently.

It analyzes customer complaints, identifies potential reputation risks, generates personalized public responses and prepares internal escalation emails to help management understand and address customer dissatisfaction.

The agent aims to transform negative feedback into actionable business insights.

## Key Features

### 1. Negative Review Analysis
- Analyzes negative customer reviews (1-star and 2-star ratings).
- Identifies the main complaint category.
- Evaluates customer sentiment.
- Classifies the severity of the situation.
- Assesses potential business and reputational impact.

### 2. Public Response Generation
- Generates professional and personalized responses.
- Adapts communication to the business type and review platform.
- Uses an empathetic and non-defensive tone.
- Acknowledges the customer's concerns.
- Avoids unsupported promises, compensation or claims.

### 3. Internal Escalation Email
- Prepares an email for the business manager.
- Summarizes the customer's complaint.
- Highlights the main issues requiring attention.
- Recommends immediate actions.
- Suggests appropriate follow-up steps.

### 4. Recurring Complaint Detection
- Compares the current review with previous complaints supplied by the user.
- Identifies recurring service or operational problems.
- Highlights patterns that may require management attention.
- Distinguishes confirmed patterns from assumptions.

### 5. Recommended Action Plan
- Suggests immediate corrective actions.
- Provides short-term follow-up recommendations.
- Identifies areas requiring further investigation.
- Helps management prioritize customer service improvements.

## Workflow Architecture

The agent was developed using n8n and OpenAI GPT-4.1.

**Workflow:**

Form Trigger → Edit Fields → Basic LLM Chain → OpenAI Chat Model → Form Ending

### Main Components

| Component | Purpose |
|---|---|
| Form Trigger | Collects business and customer review information |
| Edit Fields | Organizes and prepares input data |
| Basic LLM Chain | Processes the review and generates the crisis report |
| OpenAI Chat Model | Provides AI-powered analysis and response generation |
| Form Ending | Displays the final report to the user |

## Input Information

The user provides:

- Business Name
- Business Type
- Review Platform
- Customer Name
- Customer Rating
- Customer Review
- Review Date
- Manager Email
- Previous Similar Complaints
- Additional Context
- Response Language

## Supported Business Types

The agent can be used across different industries, including:

- Restaurants
- Hotels
- Healthcare
- Retail
- Professional Services
- Other business categories

## Example Use Cases

**Restaurant:** Analyze a negative review about long waiting times, cold food and poor staff communication.

**Hotel:** Identify recurring complaints about room readiness, housekeeping and cleanliness.

**Healthcare:** Prepare a professional response to a patient's negative service experience, while protecting confidential information.

**Retail:** Analyze complaints about customer service, product quality or delivery experiences.

## Testing and Validation

The agent was tested using two different business scenarios:

**Test 1 — Restaurant**
- Analyzed a 1-star Google review.
- Identified service quality and communication issues.
- Generated a personalized public response.
- Prepared an internal escalation email.
- Detected recurring complaints about waiting times.

**Test 2 — Hotel**
- Analyzed a 2-star Trustpilot review.
- Identified room readiness and cleanliness problems.
- Generated a tailored public response.
- Prepared management recommendations.
- Detected recurring complaints about housekeeping and check-in delays.

Both scenarios demonstrated that the agent can adapt its analysis and recommendations to different business sectors.

## Current Limitations

This version is an MVP.

- Reviews must be submitted manually through the form.
- The agent does not automatically monitor Google Reviews, Trustpilot or other platforms.
- No direct integration with review platforms is currently implemented.
- Public responses are generated as drafts and are not automatically published.
- Internal escalation emails are prepared as drafts and are not automatically sent.
- Recurring complaint detection relies on historical complaints manually supplied by the user.

## Future Improvements

Potential future developments include:

- Automatic monitoring of online review platforms.
- Integration with Google Business Profile and other review APIs.
- Automated alerts for critical negative reviews.
- Email integration for management escalation.
- Review history database for long-term complaint tracking.
- Analytics dashboard for customer satisfaction and recurring issues.

## Technology Stack

- **Automation:** n8n
- **AI Model:** OpenAI GPT-4.1
- **AI Workflow:** Basic LLM Chain
- **Input:** n8n Form Trigger
- **Output:** n8n Form Ending

## Project Status

**Completed — MVP built and tested.**

Crisis Feedback Manager is the tenth agent in the AI Agents Portfolio, a project focused on developing specialized AI agents that solve practical business problems.

---

*Part of the AI Agents Portfolio — 20 Specialized AI Agents.*

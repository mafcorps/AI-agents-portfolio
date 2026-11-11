# Agent 05 — Lead Detective

**AI-Powered B2B Lead Research & Personalized Outreach Agent**

## Overview

Lead Detective is an AI-powered sales intelligence agent designed to research potential business clients, identify relevant business challenges and generate highly personalized B2B outreach messages.

By combining public web research with AI-driven business analysis, the agent helps sales professionals move beyond generic cold outreach and create more relevant, evidence-based conversations with potential customers.

Users provide information about a potential contact, their company and the product or service they offer. Lead Detective investigates the available public information and transforms it into a structured business intelligence report and personalized sales approach.

## Key Features

- **Company Intelligence:** Researches company activities, business models, products, services and relevant developments.
- **Business Pain Point Detection:** Identifies potential business challenges using public information and industry research.
- **Evidence-Based Analysis:** Provides supporting evidence and confidence levels for identified challenges.
- **Sales Opportunity Identification:** Connects potential business needs with the user's product or service.
- **Personalized LinkedIn Outreach:** Generates tailored connection requests, initial messages and follow-ups.
- **Strategic Sales Recommendations:** Recommends the strongest commercial angle and the best message to send.
- **Research Sources:** Includes available source links to support the analysis.
- **Accuracy Controls:** Distinguishes verified facts from assumptions and commercial hypotheses.

## Workflow Architecture

The agent is built using n8n and OpenAI.

**Workflow:**

1. **Form Trigger** — Collects information about the potential client, company and product/service being offered.
2. **Edit Fields** — Organizes and standardizes the submitted information.
3. **HTTP Request (Tavily)** — Searches publicly available information about the target company.
4. **Basic LLM Chain** — Analyzes the research, identifies potential pain points and generates personalized outreach.
5. **OpenAI Chat Model** — Powers the AI analysis and content generation.
6. **Form Ending** — Presents the final business intelligence report.

## User Inputs

The agent accepts the following information:

| Input | Description |
|---|---|
| Potential Client's LinkedIn URL | LinkedIn profile or company page |
| Contact's Full Name | Name or role of the potential contact |
| Company Name | Target company |
| Company Website | Company's official website |
| Your Product / Service | Solution being offered |
| Your Ideal Customer | Description of the target customer |
| Your Main Value Proposition | Main commercial benefit |
| Preferred Outreach Tone | Professional, Friendly, Direct or Consultative |
| Main Call to Action | Desired next step |

## Generated Outputs

Each execution produces a structured report containing:

### 1. Company Intelligence
Company overview, business model, products, services, target market and relevant public developments.

### 2. Identified Business Pain Points
Up to three potential challenges, including supporting evidence, business impact, confidence level and commercial relevance.

### 3. Sales Opportunity
Analysis of how the user's product or service could address the identified business needs.

### 4. Personalized Outreach Messages
- LinkedIn connection request.
- Initial LinkedIn message.
- Follow-up message.

### 5. Strategic Recommendation
Recommended pain point, best outreach angle and suggested first message.

### 6. Research Sources
Available public sources and relevant URLs.

### 7. Research Confidence & Limitations
Transparency regarding evidence quality, assumptions and research limitations.

## Technology Stack

- **n8n** — Workflow automation and orchestration.
- **OpenAI GPT-4.1** — Business analysis, reasoning and outreach generation.
- **Tavily Search API** — Public web research.
- **n8n Forms** — User input and report presentation.

## Testing & Validation

Lead Detective was tested using three dental healthcare businesses and different commercial research scenarios:

- MALO CLINIC — Tested company intelligence, innovation-related opportunities and outreach personalization.
- Colosseum Dental Group — Tested multi-location business analysis and the relationship between business challenges and commercial relevance.
- Dentalzorg — Tested patient communication opportunities, extended opening hours and the relevance of an AI-powered virtual receptionist.

Testing identified and helped resolve issues involving missing form data, incomplete personalization and generic sales recommendations.

The final Dentalzorg test demonstrated the agent's ability to:

- Identify relevant business signals.
- Distinguish potential challenges from confirmed company problems.
- Connect the user's solution to plausible commercial opportunities.
- Generate complete LinkedIn outreach messages without placeholders.
- Provide supporting research sources and limitations.

## Limitations

- LinkedIn profiles are not directly extracted from private LinkedIn data.
- Research depends on publicly accessible information and Tavily search results.
- Company-specific operational problems cannot be confirmed without direct evidence.
- Third-party company metrics may be estimates or outdated.
- Generated outreach should be reviewed before sending.
- The agent does not automatically send LinkedIn messages or contact prospects.
- The quality of the analysis depends on the information supplied by the user and the available research.

## Future Improvements

Potential future developments include:

- Integration with professional CRM platforms.
- Lead scoring and qualification.
- Automated decision-maker identification.
- Multi-source company intelligence.
- Automated follow-up sequence generation.
- Prospect database management.
- Sales pipeline integration.

## Project Status

**Completed — Built, tested and validated.**

Lead Detective is Agent 05 in the AI Agents Portfolio.

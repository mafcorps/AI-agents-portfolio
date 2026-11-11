# Agent 06 — ProposalCraft

**AI Commercial Proposal Generator**

## Overview

ProposalCraft is an AI-powered commercial proposal generation agent designed to transform client briefings, business enquiries and original emails into structured, professional and personalized commercial proposals.

It helps businesses and consultants reduce the time spent preparing proposals by analyzing client requirements, identifying business challenges and structuring tailored solutions.

The agent is designed to work across multiple industries, including consulting, marketing, technology, design, business services and other B2B sectors.

## Key Features

- **Client Briefing Analysis:** Interprets client emails and identifies their main needs, objectives and challenges.
- **Business Needs Identification:** Extracts key requirements and translates them into relevant business opportunities.
- **Tailored Solution Development:** Connects the company's products or services to the client's specific needs.
- **Scope of Work Generation:** Structures proposed activities, responsibilities, deliverables and project boundaries.
- **Timeline Planning:** Organizes project phases, milestones and expected delivery periods.
- **Commercial Investment Structuring:** Incorporates user-provided budgets and pricing information.
- **Professional Proposal Writing:** Generates polished, persuasive and well-organized commercial proposals.
- **Internal Review:** Provides a separate internal assessment highlighting missing information, commercial risks and questions to clarify before sending the proposal.

## Workflow Architecture

The agent is built using n8n and follows this workflow:

1. **Form Trigger** — Collects client information, the original briefing and company details.
2. **Edit Fields** — Organizes and normalizes the submitted information, including dynamic date generation.
3. **Basic LLM Chain** — Processes the information and generates the commercial proposal.
4. **OpenAI Chat Model** — Powers the proposal generation using GPT-4.1.
5. **Form Ending** — Displays the generated proposal to the user.

## User Inputs

The agent collects the following information:

| Input | Description |
|---|---|
| Client / Company Name | Name of the potential client |
| Client Briefing / Original Email | Original client request or project description |
| Your Company Name | Name of the company preparing the proposal |
| Your Company Description | Background and business description |
| Product / Service Offered | Services or products being proposed |
| Proposed Budget / Price | Available budget or proposed investment |
| Expected Delivery Time | Expected project duration |
| Additional Requirements | Specific requirements or restrictions |
| Proposal Tone | Professional, Corporate, Persuasive or Consultative |
| Currency | Selected commercial currency |

Optional fields can be left unspecified when the information is unavailable.

## Generated Output

Each proposal follows a structured commercial format:

1. Executive Summary
2. Understanding of Client Needs
3. Proposed Solution
4. Scope of Work
5. Deliverables
6. Timeline and Milestones
7. Commercial Investment
8. Terms and Conditions
9. Next Steps
10. Information Requiring Confirmation

The agent also generates a separate internal review containing:

- Overall proposal quality assessment.
- Missing information.
- Potential commercial risks.
- Three questions to clarify with the client.
- Recommendations before sending.

## Accuracy and Commercial Controls

ProposalCraft includes specific safeguards to improve the reliability of generated proposals:

- Does not invent prices, discounts, payment terms or additional costs.
- Does not create unsupported guarantees or business results.
- Distinguishes confirmed services from AI-generated suggestions.
- Identifies missing information instead of assuming details.
- Separates project start dates, project duration and delivery deadlines.
- Clearly identifies services and activities outside the proposed scope.
- Uses a dynamic execution date rather than a hardcoded date.
- Separates client-facing content from internal business analysis.

All generated proposals should be reviewed and approved by a human before being sent to clients.

## Technology Stack

- **Automation Platform:** n8n
- **AI Model:** OpenAI GPT-4.1
- **AI Processing:** Basic LLM Chain
- **User Interface:** n8n Forms
- **Data Processing:** n8n Edit Fields
- **Date Handling:** Dynamic n8n expressions

## Testing and Validation

ProposalCraft was tested using two different business scenarios:

### Test 1 — Digital Marketing

**Client:** Amsterdam Fitness Studio  
**Provider:** GrowthLab

The client requested support with Instagram management, content creation and local customer acquisition.

The agent generated a structured proposal including:

- Instagram content strategy.
- Proposed content deliverables.
- Local advertising campaign.
- Project timeline.
- Commercial investment of €1,500.

This test helped identify the need for stronger controls around invented deliverables, advertising expenditure and commercial commitments.

### Test 2 — Business Consulting

**Client:** TechNova Solutions  
**Provider:** BusinessFlow Consulting

The client requested operational consulting to improve internal processes, departmental coordination and performance measurement.

The agent generated a six-week consulting proposal including:

- Current process analysis.
- Workflow optimization recommendations.
- KPI framework development.
- Operational improvement roadmap.
- Defined project boundaries.
- Commercial investment of €4,000.

The second test also validated the dynamic date functionality and improved commercial accuracy controls.

**Final validation score: 9.5/10**

## Limitations

- Proposal quality depends on the completeness and accuracy of the information provided.
- The agent does not independently verify client information.
- Generated deliverables and project milestones may require human confirmation.
- Legal terms and contractual conditions require professional review.
- Pricing, taxes and payment arrangements must be validated before sending.
- The agent generates proposal drafts and does not automatically send them to clients.

## Future Improvements

Potential future developments include:

- Exporting proposals directly to PDF and DOCX.
- Integrating CRM platforms.
- Creating reusable company proposal templates.
- Adding automatic pricing calculations.
- Supporting multiple languages.
- Building a proposal history and client database.
- Integrating electronic signature platforms.

## Project Status

**Completed — Built, tested and validated.**

ProposalCraft is Agent 06 in the AI Agents Portfolio.

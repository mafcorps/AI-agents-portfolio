# Agent 02 — Content Pulse
### Infinite Ideas Manager

**Turning business information and social media trends into 30 days of actionable content.**

## 1. Overview

ContentPulse is an AI-powered social media strategy and content generation agent designed to help businesses, brands and creators develop consistent, engaging and strategic content.

The agent analyses business information, researches relevant social media trends and generates a tailored 30-day editorial calendar with ready-to-use content ideas, video scripts, captions and hashtags.

ContentPulse is designed to work across different industries, including fitness, fashion, healthcare, hospitality, real estate, technology, retail and more.

## 2. Problem It Solves

Businesses often struggle with:
- Finding fresh content ideas consistently.
- Keeping up with social media trends.
- Planning content in advance.
- Creating engaging video scripts.
- Maintaining a consistent publishing strategy.
- Adapting content to their target audience.

ContentPulse addresses these challenges by combining AI-powered research, business analysis and content planning in one automated workflow.

## 3. Key Features

- **Business Analysis:** Analyses the company's industry, positioning, audience and business description.
- **Trend Research:** Uses Tavily search to research relevant TikTok and Instagram trends, formats and content opportunities.
- **Content Strategy:** Develops tailored content pillars for each business.
- **30-Day Content Calendar:** Generates 30 daily content ideas.
- **Ready-to-Use Scripts:** Provides hooks, video scripts, captions, hashtags and calls to action.
- **Production Guidance:** Includes practical instructions for creating each piece of content.
- **Performance Recommendations:** Suggests posting strategies and KPIs.

## 4. Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI GPT-4.1 | AI content analysis and generation |
| Tavily API | Web research and trend discovery |
| n8n Forms | Business information collection |

## 5. Workflow Architecture

The agent follows this automated process:

1. **Form Submission:** Collects business information from the user.
2. **HTTP Request — Tavily:** Researches relevant trends and content opportunities.
3. **Basic LLM Chain:** Processes business information and research findings.
4. **OpenAI Chat Model:** Generates the complete content strategy.
5. **Form Ending:** Presents the generated report to the user.

## 6. Input Requirements

The user provides:
- Business Name
- Website URL
- Industry / Niche
- Business Description

## 7. Expected Output

ContentPulse generates a structured social media strategy containing:

1. Business Analysis
2. Trend Research
3. Content Strategy
4. 30-Day Editorial Calendar
5. Execution Strategy
6. Performance Recommendations

Each daily content entry includes a platform, format, title, objective, opening hook, video script, caption, hashtags, CTA and production instructions.

## 8. Target Users

- Small and medium-sized businesses.
- Marketing agencies.
- Social media managers.
- Content creators.
- Entrepreneurs and startups.
- Personal brands.
- E-commerce businesses.

## 9. Business Value

ContentPulse helps businesses reduce content planning time, identify creative opportunities and establish a more consistent social media presence.

Its industry-independent design makes it adaptable to different business models and target audiences.

## 10. Current Development Status

**Version:** 1.0  
**Status:** Initial functional prototype  
**Workflow Platform:** n8n  
**Primary Model:** OpenAI GPT-4.1

Future improvements may include:
- More advanced real-time trend monitoring.
- Direct social media platform integrations.
- Automated content scheduling.
- Performance tracking and analytics.
- Exportable editorial calendars.
- Improved report presentation and formatting.

---

*ContentPulse is part of the AI Agents Portfolio — a collection of practical AI-powered agents designed to solve real business problems through automation and artificial intelligence.*

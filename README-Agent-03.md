# Agent 03 — ContentForge
### AI Content Repurposing Engine

## Overview

ContentForge is an AI-powered content repurposing agent built with n8n. It transforms a single blog article into three different marketing assets, helping businesses save time and distribute their content across multiple platforms.

Users can either provide a public article URL or paste the full article directly into the form.

## Key Features

- **X / Twitter Threads:** Transforms articles into engaging threads of 8–12 posts.
- **LinkedIn Carousels:** Creates structured carousels with 8–10 slides, including headlines, content and visual suggestions.
- **Sales Emails:** Generates persuasive marketing emails with subject line options, preview text and clear calls to action.
- **Content Strategy Notes:** Identifies the central message and explains the approach used for each platform.
- **Dual Input System:** Accepts both article URLs and manually pasted content.
- **Brand Personalization:** Adapts the output to the business, target audience, product or service, and brand tone.

## Workflow Architecture

Built using n8n, the workflow follows this structure:

1. **Form Trigger** — Collects the user's information and article.
2. **IF Node** — Determines whether the user provided an article URL.
3. **HTTP Request** — Retrieves the article using Jina Reader.
4. **Edit Fields** — Standardizes the article content from both input methods.
5. **Merge** — Combines the two input paths.
6. **Basic LLM Chain** — Processes the article and generates the marketing assets.
7. **OpenAI Chat Model** — Powers the content generation.
8. **Form Ending** — Displays the final report.

## Input Fields

- Brand / Business Name
- Article Title
- Article URL
- Full Blog Article / Content
- Target Audience
- Product / Service
- Brand Tone
- Main CTA

Users must provide either an article URL or the full article content.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI GPT-4.1 | AI content generation |
| Jina Reader | Article extraction |
| HTTP Request | Retrieving web content |

## Generated Outputs

Each execution produces a structured ContentForge Report containing:

1. X / Twitter Thread
2. LinkedIn Carousel
3. Sales Email
4. Content Strategy Notes

## Testing

The agent was tested with:

- Public article URLs.
- Manually pasted articles.
- Different businesses and target audiences.
- Multiple brand tones and CTAs.
- Content accuracy and platform adaptation.

The tests successfully generated all three marketing formats using both input methods.

## Limitations

- Article URLs must be publicly accessible.
- Some websites may block automated content extraction.
- AI-generated content should be reviewed before publication.
- Factual claims should be checked against the original article.

## Project Status

**Completed — Built and tested.**

Part of the AI Agents Portfolio — a collection of specialized AI agents designed to automate practical business and marketing tasks.

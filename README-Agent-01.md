# AI Ad Copywriter

An n8n-powered AI advertising copywriting workflow that researches a business and generates campaign-ready ad variations.

## What it does

1. Collects a campaign brief through an n8n form.
2. Uses Tavily Search to research the business, product/service, benefits, target audience, and competitors.
3. Passes the research and brief to an OpenAI model (GPT-5 mini) through an n8n Basic LLM Chain.
4. Returns:
   - 5 Meta Ads variations
   - 5 Google Ads variations
   - 3 strategic campaign recommendations

## Form inputs

- Business Name
- Website URL
- Product/Service
- Target audience
- Main Advertising Objective
- Advertising Platform (Meta Ads, Google Ads, or both)
- Additional Information (optional)

## Setup

1. Import `workflow.json` into n8n.
2. Configure a valid Tavily API key. The exported workflow contains the placeholder `REPLACE_WITH_TAVILY_API_KEY`; replace it securely before running.
3. Confirm the OpenAI model credentials are configured in n8n.
4. Test the form with a business brief before publishing.

## Security

- Never commit API keys, passwords, tokens, or credential exports.
- The API key in the original local export was replaced with a placeholder in this repository version.
- If an API key has been exposed, revoke it and create a new one.

## Current status

- Workflow exported from n8n.
- Tested successfully with Adidas and Gymshark sample briefs.
- The generated copy is based on the research results supplied to the model; verify product claims, availability, pricing, and legal/compliance requirements before publishing ads.

## Workflow file

`workflow.json`

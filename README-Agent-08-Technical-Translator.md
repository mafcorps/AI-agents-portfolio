# Agent 08 — Technical Translator

**AI-Powered Technical Translation Assistant**

## Overview

Technical Translator is an AI-powered document translation assistant designed to translate complex documents while preserving their original meaning, terminology, structure and technical accuracy.

The agent accepts PDF and TXT documents through an n8n form and uses GPT-4.1 to generate translations adapted to the selected language, industry and technical specialization.

It also produces a terminology table and a translation quality report.

## Key Features

- **Document Upload:** Accepts PDF and TXT files through an n8n form.
- **Multi-Language Translation:** Translates documents between supported languages.
- **Industry Adaptation:** Adapts terminology to engineering, healthcare, technology, automotive, manufacturing, legal, finance and other industries.
- **Technical Terminology:** Maintains consistent industry-specific terminology.
- **Glossary Support:** Allows users to provide preferred terminology.
- **Structure Preservation:** Attempts to preserve headings, lists, tables, references and document organization.
- **Translation Quality Report:** Reviews terminology consistency, numerical values, formatting and potential ambiguities.
- **Industry Validation:** Identifies mismatches between the selected industry and the actual document content.
- **Human Review Flags:** Highlights ambiguous or potentially safety-critical content requiring specialist review.

## Workflow Architecture

Built using n8n.

**Workflow:**

Form Trigger → Extract from File → Edit Fields → Basic LLM Chain → OpenAI Chat Model → Form Ending

The document is uploaded through an n8n form. Its extractable text is processed and organized before being sent to GPT-4.1 for translation.

## User Inputs

| Input | Description |
|---|---|
| Original Document | PDF or TXT file |
| Source Language | Original document language |
| Target Language | Desired translation language |
| Industry | Relevant industry |
| Technical Specialization | Specific technical field |
| Preferred Terminology / Glossary | Preferred translations and terminology |
| Translation Style | Technical, formal, simplified or instructional |
| Additional Instructions | Specific translation requirements |

## Generated Output

1. **Translation Overview** — Languages, industry, specialization and translation style.
2. **Complete Translated Document** — Translated text maintaining the original structure where possible.
3. **Technical Terminology** — Table of important original and translated terms.
4. **Translation Quality Report** — Terminology consistency, numerical preservation and extraction limitations.
5. **Items Requiring Human Review** — Ambiguous or safety-critical passages requiring specialist verification.

## Accuracy and Quality Controls

The agent follows strict translation rules:

- Preserves the original technical meaning.
- Maintains numerical values, units, formulas and references.
- Avoids inventing or omitting information.
- Preserves programming code and technical identifiers unless instructed otherwise.
- Uses industry-appropriate terminology.
- Flags mismatches between selected industry and document content.
- Identifies visual content that has not been processed.
- Does not claim professional certification or independent verification.

## Technology Stack

- **n8n** — Workflow automation and orchestration.
- **OpenAI GPT-4.1** — Technical translation and quality analysis.
- **n8n Forms** — Document upload and translation result presentation.
- **Extract from File** — PDF text extraction.

## Testing and Validation

The agent was tested using an academic document about Emotional Intelligence.

Testing covered:

- English-to-Portuguese translation.
- English-to-Spanish translation.
- Preservation of numerical scores and references.
- Industry mismatch detection.
- Technical terminology consistency.
- Translation quality reporting.
- Identification of visual content limitations.

The tests demonstrated that the agent can translate extracted document text and correctly identify when the selected industry does not match the document's actual subject.

## Limitations

- Currently supports PDF and TXT uploads.
- DOCX support is not included in this MVP.
- Scanned PDFs and image-based text require OCR, which is not currently implemented.
- Charts, diagrams and embedded images are not independently processed.
- Complex document layouts may not be reproduced exactly.
- Translation quality depends on the extractable source content.
- Medical, legal and safety-critical translations require qualified human review.

## Future Improvements

- DOCX support.
- OCR for scanned documents.
- Image and chart text extraction.
- Improved table and layout preservation.
- Downloadable translated documents.
- Persistent technical glossaries.
- Industry-specific terminology databases.
- Additional document formats.

## Project Status

**Completed — MVP built and tested.**

Agent 08 is part of a portfolio of 20 specialized AI agents designed to solve practical business and professional problems.

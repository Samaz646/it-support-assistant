# IT Support Assistant

A private IT support workflow project designed to combine structured ticket analysis, existing troubleshooting history, internal knowledge and external technical research.

This repository documents the workflow and concept of an AI-assisted IT troubleshooting environment.

The project can process different sources of technical information, including support tickets, Markdown files, documents, screenshots and other case-related material.

> Portfolio repository — documentation only.  
> No customer data, production support cases or confidential internal information is included.

## Project focus

This project is not intended to be a traditional end-user helpdesk chatbot.

Its focus is to assist IT technicians during ongoing support cases by correlating the existing ticket history, previous troubleshooting steps, technical evidence, connected knowledge sources and external documentation.

Rather than immediately proposing configuration changes, the workflow aims to determine the current state of the case and identify the smallest useful diagnostic step first.

The long-term direction is technician-focused decision support: AI assists with analysis, research and correlation while administrative actions remain explicitly separated from diagnostic recommendations.

## Motivation

Long-running IT support cases often contain information distributed across tickets, messages, documents, screenshots, diagnostic outputs and previous troubleshooting attempts.

This makes it increasingly difficult to determine:

- what has already been tested
- which findings are still relevant
- what has changed since the previous analysis
- which information is still missing
- whether a reported or monitored condition still reflects the current system state
- what the next useful diagnostic step should be

The IT Support Assistant is intended to structure this information and support a systematic troubleshooting process without repeatedly starting the analysis from the beginning.

## Workflow

```text
Support Case Input
(tickets, Markdown, documents, screenshots)
          |
          v
Ticket & Evidence Analysis
          |
          +----> Knowledge Base
          |
          +----> Vendor Documentation
          |
          +----> Web Research
          |
          v
Context Correlation
          |
          v
Next Diagnostic Step
```

## Features

### Structured case analysis

The assistant evaluates the available information from the support case and identifies:

- the original problem
- previous troubleshooting steps
- user or technician feedback
- diagnostic results
- unresolved issues
- new technical evidence

### Multi-format input

Support cases are not limited to a single file format.

Depending on the case, the analysis can include:

- Markdown files
- ticket exports
- technical documents
- PDFs
- screenshots
- diagnostic information
- additional case-related material

This allows different sources of technical evidence to be considered together.

### Context-aware troubleshooting

Existing troubleshooting steps and previous findings are taken into account before determining the next diagnostic action.

This helps avoid repeating steps that have already been performed and keeps the analysis focused on the current state of the case.

### Knowledge base integration

Additional technical context can be retrieved from a connected knowledge base.

This can include:

- technical documentation
- troubleshooting notes
- previous solutions
- information from comparable cases

The retrieved information can then be correlated with the current support case.

### External technical research

When required, additional information can be gathered from external sources such as:

- vendor documentation
- technical documentation
- knowledge bases
- web research

This is useful when investigating product-specific behavior, documented limitations or known technical issues.

### Read-only-first diagnostics

Where possible, the workflow prefers the smallest useful read-only verification step before recommending configuration changes.

A monitoring alert or reported error is not automatically treated as proof of the current system state.

Instead, the workflow attempts to distinguish between:

- the reported or monitored condition
- the actual current system state
- the evidence required to verify the problem

Diagnostic recommendations and administrative changes are treated as separate stages.

### Multiple evidence sources

Information from different sources can be evaluated together.

For example:

```text
Support Ticket
     +
Screenshot / PDF
     +
Previous Troubleshooting
     +
Knowledge Base
     +
Vendor Documentation
     |
     v
Correlated Technical Context
     |
     v
Next Diagnostic Step
```

## Example workflow

### 1. Support case input

A support case is provided together with the available technical information.

Depending on the situation, this may include a ticket or Markdown export, documents, screenshots or other diagnostic material.

![Support case input](docs/01-support-case-input.png)

### 2. Chronological ticket analysis

The existing case history is evaluated chronologically to identify previous troubleshooting steps, new evidence and the current unresolved state.

![Ticket analysis](docs/02-ticket-analysis.png)

### 3. Technical classification and vendor research

When product-specific behavior needs to be verified, relevant vendor documentation and external technical sources can be researched.

![Vendor research](docs/03-vendor-research.png)

### 4. Knowledge base search

Existing technical documentation and previous troubleshooting knowledge can be searched for additional context.

![Knowledge base search](docs/04-knowledge-base-search.png)

### 5. Read-only verification

Before recommending changes, the workflow attempts to identify the smallest useful diagnostic step that can verify the actual system state.

![Read-only analysis](docs/05-readonly-vendor-research.png)

### 6. Multiple evidence sources

Documents, screenshots and other supporting material can be included in the same troubleshooting process and correlated with the existing case information.

![Multiple evidence sources](docs/06-multimodal-ticket-analysis.png)

## Project components

The current workflow combines:

- AI-assisted support case analysis
- multi-format case input
- structured troubleshooting instructions
- connected knowledge base research
- vendor documentation
- web research
- evidence correlation
- read-only-first diagnostic guidance

The repository focuses on the workflow and its practical application rather than publishing private prompts, customer information or production data.

## Planned development

Possible future extensions of the workflow include:

- structured integration with ticket or ITSM data
- read-only retrieval of relevant device and monitoring context
- correlation of current incidents with previous support cases
- additional asset context such as system role, installed software or recent technical changes
- clearer separation between diagnostic recommendations and explicitly authorized administrative actions

These are development directions rather than features claimed by the current portfolio version.

## Privacy

All material published in this repository is intended for demonstration and portfolio purposes.

The public repository does not contain:

- real customer support tickets
- personal information
- passwords or API keys
- confidential infrastructure information
- real internal hostnames or IP addresses
- private knowledge base content
- internal project prompts

Examples and screenshots are anonymized or created specifically for demonstration purposes.

## Project status

This is an actively developed private project.

The workflow is being refined using practical IT troubleshooting scenarios with the goal of improving structured case analysis, technical research, evidence correlation and the selection of appropriate diagnostic steps.

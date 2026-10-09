# Choosing a CRM

An organisation choosing a CRM today will probably ask an AI assistant for advice before it talks to anyone. That conversation can lead somewhere useful: **the organisation's own AI assistant as its first CiviCRM guide**, from "is this right for us?" to a working set-up, with implementers brought in at the right moments.

## The journey

```mermaid
flowchart LR
    F["Is it right<br/>for us?"] --> H["Getting it<br/>running"] --> S["Set up<br/>for us"] --> D["Bring our<br/>data in"] --> O["Day one"] --> G["Growing"]
    click F "#stages" "Stages"
    click S "#stages" "Stages"
```

## Stages

| Stage | The question | What the AI could do | Capability | Where an expert comes in |
|---|---|---|---|---|
| **Is it right for us?** | "We're a 5-person food bank. Would CiviCRM work?" | Explain fit honestly, including when it isn't the right choice, from CiviCRM's own docs | [C10](capabilities.md) | Complex or unusual needs |
| **Getting it running** | "How do we get CiviCRM running?" | Compare hosted options and self-hosting for the organisation's budget and skills | [C10](capabilities.md) | Custom or high-volume hosting |
| **Set up for us** | "We run a membership programme and two annual events." | Propose a starter configuration, preview it, apply it on confirmation | [C5, C6](capabilities.md) | Anything beyond a starter kit |
| **Bring our data in** | "Here's our donor spreadsheet." | Map columns to fields, flag problems, run the import with a preview | [C7](capabilities.md) | Migrations from another CRM |
| **Day one** | "How do I record a donation?" | Answer from the docs and the organisation's own configuration | [C2, C10](capabilities.md) | Training |
| **Growing** | "We need online payments and tax receipts." | Explain the options and their trade-offs, and recommend expert help | [C11](capabilities.md) | Payments, receipting, integrations |

The first two stages need **no CiviCRM installed at all**, so they depend on a knowledge service over CiviCRM's documentation and directories, most likely on civicrm.org, rather than on an extension.

## What has to be true

- **Every stage works with any capable AI assistant**, not a single vendor's.
- **Previews protect beginners.** A new organisation can't judge a configuration change it doesn't understand, so the preview has to explain the change in plain language.
- **The AI is honest about fit.** Steering an organisation into CiviCRM when it would be better served elsewhere costs everyone.
- **Implementers are part of the path.** The journey should hand an organisation to an implementer when it's ready.

Hosted offerings such as [CiviCRM Spark](https://civicrm.com/spark/) already remove the hosting step for small organisations; how AI capabilities might be offered there is CiviCRM LLC's decision.

# Community work so far

People across the CiviCRM community are already building AI capabilities. This list aims to be complete as of October 2026; additions and corrections are very welcome in the comments.

=== "Organisation's own AI uses CiviCRM"

    | Project | Who | What it does | Stage |
    |---|---|---|---|
    | [civicrm_mcp](https://lab.civicrm.org/extensions/civicrm_mcp) | Community extension | MCP served from inside CiviCRM, with OAuth 2.1 sign-in, per-person permissions and a call log | Alpha, read-only |
    | [civi-mcp](https://github.com/yo61/civi-mcp), [civicrm-mcp](https://github.com/YogiAdhik/civicrm-mcp), [civicrm_mcp_python](https://github.com/Stewie23/civicrm_mcp_python) and others | Individuals | Separate programs that connect AI assistants to CiviCRM's API; the Python one strips personal data before it reaches the AI | Early versions |
    | [n8n CiviCRM nodes](https://www.npmjs.com/package/@ixiam/n8n-nodes-civicrm) | iXiam | Workflow automation that AI agents can use to reach CiviCRM | Released |

=== "CiviCRM uses AI"

    | Project | Who | What it does | Stage |
    |---|---|---|---|
    | [DocBot](https://civicrm.org/extensions/docbot) | CiviCRM Core Team | A dashboard assistant that answers questions from the CiviCRM documentation | Released 2024 |
    | [ai-connection](https://lab.jmaconsulting.biz/extensions/ai-connection) | JMA Consulting | A chat page inside CiviCRM backed by the organisation's choice of model, including tools that build SearchKit searches | Alpha |
    | [AI Assistant](https://github.com/kurund/civicrm_ai_assistant) | Kurund Jalmi | Plain-English requests turned into SearchKit searches; an `Ai.prompt` API action for several providers, including local ones | Prototype |
    | [CiviAI](https://civicrm.org/blog/jamienovick/civiai-exploring-future-ai-civiplus) | Compucorp | An in-CRM assistant and "smart fields" | Exploratory |
    | [AI in CiviCRM reporting](https://circle-interactive.co.uk/AI-in-CiviCRM-reporting) | Circle Interactive | Plain English to SearchKit reports; insights from anonymised data | Hosted beta |
    | [Dialogflow](https://civicrm.org/extensions/dialogflow) | Community | Conversations with CiviCRM over SMS or WhatsApp | In development |

=== "Through the CMS"

    | Project | Who | What it does | Stage |
    |---|---|---|---|
    | [Self-hosted AI for your CiviCRM stack](https://civicrm.org/blog/jackrabbithanna/self-hosted-ai-your-civicrm-stack) | Skvare | Drupal's AI module plus CiviCRM Entity, for search over CRM records with local models | Architecture write-up |

=== "Conversations"

    | Topic | Where |
    |---|---|
    | An AI policy for contributions to CiviCRM | [dev/core#6796](https://lab.civicrm.org/dev/core/-/work_items/6796) |
    | Values for AI in CiviCRM: responsible, sustainable, secure; no single organisation owns AI for CiviCRM | [Circle Interactive's write-up of a partner discussion](https://www.circle-interactive.co.uk/article/AI-and-CiviCRM-leading-with-values) |
    | Day-to-day discussion | The `~ai` channel on [chat.civicrm.org](https://chat.civicrm.org) |

## How these fit together

Each of these efforts covers part of the picture. The [proposed building blocks](path-forward.md) are one way they could share foundations: a common tool registry, one AI provider setting and shared safety rules, so a tool built by one team works for everyone.

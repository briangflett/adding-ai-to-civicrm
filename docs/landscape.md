# The wider CRM landscape

!!! abstract "Background"
    A snapshot from late September 2026 of what nonprofit and open-source CRMs offer, researched with an AI assistant from current sources. It's useful as a checklist of what organisations are being offered, not an endorsement, and vendors change quickly. Corrections welcome.

## In short

**No nonprofit CRM was designed around AI from the start.** Every nonprofit product found began as a conventional database, with AI features added on top. The CRMs designed around AI from day one are built for businesses, and none handles fundraising.

## Commercial nonprofit CRMs

| Product | AI features | Can act, not just answer | Open AI connector (MCP) |
|---|---|---|---|
| **Salesforce Nonprofit Cloud + Agentforce** | Prospect research and participant management agents; donor support agent | Yes | Yes, Salesforce-hosted |
| **Blackbaud Raiser's Edge NXT** | Development agent (US only); Microsoft 365 Copilot integration | Claimed | No |
| **Bonterra Que** | Launched Oct 2025; several skills still "coming" | Claimed | No |
| **Bloomerang (Penny)** | In beta | Partly | No |
| **Virtuous** | Generative outreach, predictive insights | No | No |
| **Neon One** | Search over customer data | No | No |
| **Keela, Givebutter, DonorPerfect** | Suggestions and summaries, several in beta | No | No |

## How nonprofits actually use AI

- In a September 2026 sector survey (n=917), **45% used AI daily, but only 4% reported fully integrated AI operations**, and more than half of executives had no AI budget.
- Another survey (December 2025, n=346) found **92% using AI, but only 7% reporting major impact on their mission**, and 47% with no AI policy.
- Neither separated AI built into a CRM from staff using a general assistant. The pattern suggests most use is the second kind, which is exactly what connecting an organisation's own assistant serves.

## Open-source CRMs

| Project | AI features | MCP connector | Nonprofit features |
|---|---|---|---|
| **Twenty** | Chat and agents | Official, behind a feature flag | None (no donations, memberships, grants or cases) |
| **EspoCRM, SuiteCRM** | None in core | Community only | None |
| **Odoo** | Yes, but not in the free Community edition | No official | Limited |
| **Dolibarr** | Content generation module | No | Donations |
| **CiviCRM** | Community extensions | Community extensions | Broad: contributions, memberships, events, cases, grants, campaigns, mailings |

## What good AI integration looks like under the hood

- **The AI acts with the user's permissions**, checked before the AI even sees a tool.
- **Changes are proposed, shown and confirmed** before they're saved.
- **Sensitive data can be kept from the AI** entirely.
- **Search by meaning**, kept in step with the data.
- **Standard, secure connections**: MCP with OAuth 2.1 and tokens bound to one service.

## How much CiviCRM can do as extensions

| Property | Core changes needed? | Why |
|---|---|---|
| AI tools generated from the data model | No | APIv4 describes every entity and field |
| MCP as the connection | No | An extension can serve it |
| AI acting as the user | No | Permissions and ACLs already enforce it |
| Audit trail | No | An extension can log every call |
| Validated, previewed changes | No | APIv4 writes are already validated |
| Search by meaning | Partly | Needs an external index |
| Long-running AI tasks | Outside CiviCRM | Needs an external worker |

Most of what good AI integration requires can be built as extensions, and the hardest parts, acting with the user's permissions and validating every change, are things CiviCRM has done well for many years.

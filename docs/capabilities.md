# What AI could do in CiviCRM

Fifteen capabilities, who they help and how they could be provided. **"Your AI"** marks capabilities used by an outside assistant; **"In CiviCRM"** marks ones where CiviCRM calls a model itself ([the two directions](two-directions.md)).

| # | Capability | Direction | Who it helps most | How it could be provided | Status (Oct 2026) |
|---|---|---|---|---|---|
| C1 | **A safe connection** between an AI assistant and CiviCRM: sign-in, permissions, audit | Your AI | Everyone | An MCP gateway extension ([civicrm_mcp](https://lab.civicrm.org/extensions/civicrm_mcp) is one) | Alpha |
| C2 | **Ask questions of your own data** | Your AI | Existing users | The gateway's built-in read tools | Alpha (read-only) |
| C3 | **Task-specific tools** for fundraising, cases, events, volunteers | Both | Existing users | **Domain tool packs**: separate extensions registering tools with the gateway | One site-specific pack |
| C4 | **Make changes, always previewed**: log an activity, update a record | Both | Existing users | A shared preview-and-confirm framework that every write tool uses | Planned |
| C5 | **Set CiviCRM up by describing what you need**: fields, groups, searches, forms, previewed | Both | Small organisations without an administrator | A **configuration** extension built on C4 | Idea |
| C6 | **Starter kits**: ready-made configurations for common kinds of organisation, applied by the AI | Both | New organisations | A starter-kit extension, or packaged configurations | Idea |
| C7 | **Bring your data in** from spreadsheets or another CRM, with the AI mapping fields | Both | New organisations | An **import assistant**, using CiviCRM's existing import tools | Idea |
| C8 | **Search by meaning**, not just exact words, across notes and activities | Both | Existing users | A **semantic search** extension with an external index (MySQL can't hold one) | Idea |
| C9 | **Data quality**: duplicates, gaps, inconsistencies | Both | Existing users | A data-quality pack using CiviCRM's dedupe rules | Idea |
| C10 | **Help before you've installed anything**: is CiviCRM right for us, which hosting, how to start | Your AI | New organisations | A **knowledge service** over CiviCRM's docs and directories, most likely run by civicrm.org; the Core Team's **DocBot** is the natural start | Partly (DocBot) |
| C11 | **Knowing when to call an expert**, and pointing to the [partner directory](https://civicrm.com/partners/) | Both | Everyone | A shared convention every tool follows, plus a partner lookup in C10 | Principle |
| C12 | **Background work**: scheduled or long-running AI tasks | In CiviCRM | Existing users | An **external worker**, because CiviCRM's request cycle can't run long agent loops | Idea |
| C13 | **AI inside CiviCRM's own screens**: a chat page, a "summarise" button | In CiviCRM | Staff without their own AI assistant | An **in-app assistant** extension, using the organisation's own model key and the same tools as C1 | Prototypes |
| C14 | **Privacy controls**: keep contacts, fields or groups away from AI entirely | Both | Everyone | Data scoping in the tool registry, plus a "safe for AI" marker on fields | Partly (permissions and ACLs today) |
| C15 | **One place to set an AI provider**, its key and a spending limit | In CiviCRM | Organisations that want C12 or C13 | An **AI provider layer** extension, eventually core | Prototypes |

## Extensions that could provide them

| Extension (working name) | Capabilities | Depends on | Exists today? |
|---|---|---|---|
| **MCP gateway** | C1, C2, C4 framework, C11 convention, C14 | — | Alpha ([civicrm_mcp](https://lab.civicrm.org/extensions/civicrm_mcp)); other MCP servers exist, see [related work](related-work.md) |
| **Fundraising tool pack** | C3: donor summaries, lapsed and upgrade lists, pledge follow-up | Gateway | — (Circle Interactive's SearchKit reporting agent is related) |
| **Case and programme tool pack** | C3: case summaries, caseload, follow-ups | Gateway | One site-specific pack |
| **Events and volunteers pack** | C3 | Gateway | — |
| **Configuration assistant** | C5 | Gateway (C4) | — |
| **Starter kits** | C6 | Configuration assistant | — |
| **Import assistant** | C7 | Gateway (C4) | — |
| **Semantic search** | C8 | Gateway, external index | — (Skvare has described a Drupal-side approach) |
| **Data-quality assistant** | C9 | Gateway | — |
| **AI background worker** | C12 | Gateway, provider layer | — |
| **In-app assistant** | C13 | Provider layer; the gateway's tools | Prototypes: JMA's ai-connection, Kurund Jalmi's AI Assistant, Compucorp's CiviAI |
| **AI provider layer** | C15 | — | Prototypes inside ai-connection and Kurund Jalmi's AI Assistant |
| **CiviCRM knowledge service** | C10, C11 | — (runs on civicrm.org) | Partly: DocBot |

## The gateway's job

The MCP gateway is the piece every other AI extension would depend on, so it should stay small and trustworthy. [Where civicrm_mcp fits](civicrm-mcp-scope.md) sets out what it takes on and what belongs in other extensions.

## Where to start

Several capabilities are open for anyone who wants to help: a shared AI provider setting (C15), AI-assisted data quality (C9), a reusable way to keep personal data away from AI (C14), and AI-proposed changes approved by a person (C4). The [proposed building blocks](path-forward.md) suggest an order. [Community work so far](related-work.md) shows who is already building what.

# Principles, and why now

## What "AI capabilities" means here

An AI assistant that can safely do real work in CiviCRM: answer questions, help set things up, and carry out tasks for the person using it. It acts as that person, under their permissions, and checks with them before changing anything. A chatbot bolted onto one screen isn't the goal.

## AI on, or AI off: both have to work

Some organisations want no AI near their data, for reasons of policy, privacy, their funders or simple preference. Others are looking for exactly the AI-assisted tools now being advertised across the sector. **CiviCRM can serve both, and its extension model already makes that natural:**

- **Nothing changes unless you install it.** Every AI capability lives in an optional extension. A site without them works exactly as it does today.
- **Turned on, everything is controlled.** Which people, which data and which AI service is up to the organisation.
- **Bring your own model.** CiviCRM doesn't choose an AI vendor, hold anyone's AI key in core, or pay for anyone's AI usage.

## Why now

- **Staff already use AI assistants every day**, and increasingly expect them to work with the systems they use.
- **The standards have settled.** MCP (for connecting assistants to systems) and OAuth 2.1 (for signing in) matured during 2025 and 2026, and the PHP libraries for both are now usable.
- **WordPress and Drupal have done the groundwork.** Their designs, and their mistakes, are public. Building now means building on what they've learned.

## Where AI can help most

CiviCRM's depth is its strength: contributions and receipting, memberships, events, cases, grants, campaigns and mailings in one system, with custom fields, SearchKit and FormBuilder on top. The places where organisations most often want help are **getting started, configuration, and day-to-day use by occasional staff**. Those are exactly the jobs an AI assistant is good at: explaining in plain language, proposing a set-up, and doing routine steps on someone's behalf. AI can make that depth easier to reach without giving any of it up.

## Principles

<div class="grid cards" markdown>

-   :material-toggle-switch-off-outline: **Optional, always**

    No AI capability is ever required to use CiviCRM.

-   :material-key-outline: **Bring your own model**

    CiviCRM provides capabilities. The organisation chooses the AI.

-   :material-account-lock-outline: **The AI acts as you**

    Your permissions, never a hidden service account.

-   :material-eye-check-outline: **Preview before change**

    Nothing is saved until a person confirms it.

-   :material-account-tie-outline: **Experts stay central**

    Tools recognise when a job needs an implementer and point to the neutral [partner directory](https://civicrm.com/partners/), never to one firm.

-   :material-server-outline: **Ordinary hosting**

    Nothing that needs a new server to install, except where clearly marked.

-   :material-source-branch: **Open and shared**

    Community-owned, with more than one maintainer per extension.

</div>

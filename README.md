# Web Identity Layer (WIL)

A proposal for a machine-readable identity layer for websites in the age of AI.

## The problem

Modern AI systems increasingly rely on web content to answer questions, summarize businesses, recommend services and retrieve information.
However, websites currently communicate with machines through a collection of disconnected mechanisms:

- robots.txt
- sitemap.xml
- Open Graph
- Schema.org
- metadata
- HTML structure

These tools were designed for different purposes and different generations of crawlers.
As a result, AI systems often have to reconstruct a website's identity from fragmented signals. This can lead to:

- outdated information
- incomplete understanding of services
- inconsistent business descriptions
- unnecessary crawling and processing

## Why now?

AI systems increasingly act as intermediaries between users and websites.
Unlike traditional search engines, these systems often generate summaries, recommendations and direct answers based on their interpretation of web content.
As AI adoption grows, the quality and reliability of machine-readable website information becomes increasingly important.

## The question

> What if websites exposed a simple, explicit and machine-readable identity layer?

A single source of truth that allows machines to understand:
- who owns the site
- how ownership can be verified
- what the site represents
- which information is official
- where structured resources can be found

## Proposed concept

At the root of the website:

```text
/identity.json
```

An example:

```json
{
  "name": "PuntaSoft",
  "type": "business",
  "description": "Software development and IT consulting",
  "logo": "https://puntasoft.it/wp-content/uploads/2026/05/marchio-300x101.png",
  "officialDomain": "puntasoft.it",
  "keywords": [
    "software",
    "automation",
    "consulting"
  ],
  "contacts": {
    "email": "support@puntasoft.it"
  }
}
```

This file is not intended to replace:

- robots.txt
- sitemap.xml
- Schema.org

Instead, it aims to provide a stable identity layer for machines.

## Current status

⚠️ Early draft.

This repository currently exists to:

- validate the problem
- collect feedback
- discuss requirements
- explore implementation options

No formal specification has been defined yet.

## Goals

- Simple
- Human-readable
- Machine-readable
- CMS-independent
- AI-friendly
- Easy to generate

## Non-goals

WIL is not intended to:

- replace SEO standards
- replace Schema.org
- replace sitemaps
- dictate ranking or indexing behavior

## Discussion

The project is currently in the exploration phase.

Questions:

- Is this a real problem?
- Are existing standards already sufficient?
- What information should belong in a web identity layer?
- How should ownership and verification work?

Contributions, criticism and alternative approaches are welcome.

## Why not existing standards?

Existing standards solve important problems:

- robots.txt controls crawler access
- sitemap.xml helps discovery
- Open Graph improves content sharing
- Schema.org adds structured data

WIL explores a different question:

How can a website explicitly communicate its identity, ownership and official machine-readable representation?

## Disclaimer

WIL is an exploratory proposal.

The goal of this repository is to encourage discussion around how websites communicate identity and ownership to AI systems and future web agents.

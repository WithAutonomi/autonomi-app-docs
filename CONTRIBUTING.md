# Contributing to the Autonomi App docs

This repository is the source of truth for the **Autonomi App** documentation space on [docs.autonomi.com](https://docs.autonomi.com). It is synced two-ways with GitBook, so changes made here are reflected on the live docs site, and edits made in GitBook are committed back to this repo.

## Repository layout

```
.
├── README.md                  ← the Quick Start landing page
├── SUMMARY.md                 ← GitBook sidebar navigation
├── .gitbook.yaml              ← GitBook sync config
├── .gitbook/assets/           ← images and screenshots
├── system-requirements.md
├── downloads.md
├── guides/
│   ├── running-nodes.md
│   ├── files.md
│   ├── wallets.md
│   ├── settings.md
│   └── troubleshooting.md
└── support/
    ├── get-help.md
    ├── faqs.md
    ├── acronyms.md
    └── terms-and-conditions.md
```

Folder names mirror the URL structure on docs.autonomi.com.

## Making changes

You have two options:

**1. Edit in GitBook (recommended for most changes).** Changes made in the GitBook editor are committed back to this repo automatically via the two-way sync. This is the easiest path for content edits and small fixes.

**2. Edit in this repo.** Open a pull request against `main`. Once merged, GitBook pulls the change within a few seconds. Use this path for:
- Structural changes (new pages, renamed pages, moved pages)
- Changes to `SUMMARY.md` or `.gitbook.yaml`
- Bulk edits
- Anything that needs code review before going live

## Adding a new page

1. Create the `.md` file in the correct folder.
2. Add a one-line `description` at the top (YAML frontmatter) — GitBook uses this as the page subtitle.
3. Add an entry to `SUMMARY.md` so it appears in the sidebar.
4. Open a PR.

## Frontmatter

Every page should start with:

```yaml
---
description: A one-line summary of what this page is about.
---
```

## Images and screenshots

Store under `.gitbook/assets/`, named by section and sequence — e.g. `nodes-dashboard-01.png`, `wallets-import-02.png`. Reference them with a relative path:

```markdown
![Nodes dashboard](.gitbook/assets/nodes-dashboard-01.png)
```

## Style notes

- Sentence case for page titles and headings ("Running nodes", not "Running Nodes").
- Use "the app" when referring to the Autonomi App after first mention.
- Link to other pages with relative paths (`guides/wallets.md`), not full URLs.
- Prefer short sentences and clear verbs in headings ("Start your first node", not "Node initialisation").

## GitBook sync

The two-way sync is configured in the GitBook space settings for "Autonomi App". If you need to reconnect or change the branch, ask a maintainer — changing sync settings can cause temporary outages on the live docs.

# PorchLyte AI Agent Team

Your nine-person AI team for real estate, distributed as an installable Claude plugin. Instead of downloading and uploading a zip, you add this marketplace once and Claude installs (and updates) the plugin for you.

This is **step two**. Set up your [AI Agent Foundation](https://github.com/PorchLyte/porchlyte-foundations) first — usually on an earlier day so you're not doing everything at once. Then come here to hire your team. Every team member reads from the Voice, Brand, and Local profiles you build in the Foundation.

This marketplace holds one plugin:

- **AI Agent Team** — your nine-person AI team: Ella (email), Darla (daily briefing), Chloe (content), Poppy (podcast), Treena (transactions), Lia (listings), Sloane (sphere), Rhonda (relocation), and Olivia (objections). Requires the Foundation.

## How to install (for agents using these)

First install the Foundation from its own repo: [porchlyte-foundations](https://github.com/PorchLyte/porchlyte-foundations). Once your Foundation is set up, come back here.

In the Claude desktop app with Cowork enabled, open a chat and run these commands one at a time:

```
/plugin marketplace add PorchLyte/porchlyte-agents
/plugin install ai-agent-team@porchlyte-agents
```

> Replace `PorchLyte` with the GitHub username (or org) this repo lives under. The pattern is always `owner/repo`.

Then hire your team:

```
/set-me-up
```

That walks you through meeting and hiring your team one at a time. You don't have to hire all nine at once — start with one, see how it goes, come back later. Your work saves.

## How updates work

Once someone has added the marketplace, they get your latest version automatically. When you push a change to this repo, their Claude picks it up the next time it refreshes the marketplace. If they want to pull updates immediately, they run:

```
/plugin marketplace update porchlyte-agents
```

No new zip. No re-uploading. You edit here, they get it there.

## How to update the plugin (for Tracy)

1. Edit the files inside `plugins/ai-agent-team/`.
2. Commit and push to GitHub.

That's it. Because the plugin doesn't pin a version number, every commit you push counts as a new version, so your users receive the update on their next refresh.

If you'd rather control exactly when updates go out, add a `"version"` field to `plugins/ai-agent-team/.claude-plugin/plugin.json` and bump it on each release. Then users only update when that number changes.

## The Foundation lives in a separate repo

The Voice, Brand, and Local skills now ship from [porchlyte-foundations](https://github.com/PorchLyte/porchlyte-foundations). They're split out so course users can set up their Foundation first and add the Team on a later day without being overwhelmed. The Team still requires the Foundation — it just installs from its own marketplace.

## Repo layout

```
.claude-plugin/marketplace.json     <- the catalog that lists the Team plugin
plugins/
  ai-agent-team/                    <- Team plugin (the nine members)
```

## Questions

Email tracy@porchlyte.com or visit porchlyte.com.

— Tracy

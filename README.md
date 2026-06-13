# PorchLyte AI Agents

The AI Agent system for real estate agents, distributed as installable Claude plugins. Instead of downloading and uploading a zip, you add this marketplace once and Claude installs (and updates) the plugins for you.

This marketplace holds two plugins:

- **AI Agent Foundation** — three skills (Voice, Brand, Local) that teach Claude how you sound, how your brand looks, and what your market is really like. Install this first. Everything else reads from it.
- **AI Agent Team** — your nine-person AI team: Ella (email), Darla (daily briefing), Chloe (content), Poppy (podcast), Treena (transactions), Lia (listings), Sloane (sphere), Rhonda (relocation), and Olivia (objections). Requires the Foundation.

## How to install (for agents using these)

In the Claude desktop app with Cowork enabled, open a chat and run these commands one at a time:

```
/plugin marketplace add tracyhenning/porchlyte-agents
/plugin install ai-agent-foundation@porchlyte-agents
/plugin install ai-agent-team@porchlyte-agents
```

> Replace `tracyhenning` with the GitHub username (or org) this repo lives under. The pattern is always `owner/repo`.

Then set up your Foundation:

```
/foundations-setup
```

That walks you through Voice, Brand, and Local one at a time (about 15–20 minutes for all three). You can stop after one and come back later. Your answers save.

## How updates work

Once someone has added the marketplace, they get your latest version automatically. When you push a change to this repo, their Claude picks it up the next time it refreshes the marketplace. If they want to pull updates immediately, they run:

```
/plugin marketplace update porchlyte-agents
```

No new zip. No re-uploading. You edit here, they get it there.

## How to update the plugins (for Tracy)

1. Edit the files inside `plugins/ai-agent-foundation/` or `plugins/ai-agent-team/`.
2. Commit and push to GitHub.

That's it. Because the plugins don't pin a version number, every commit you push counts as a new version, so your users receive the update on their next refresh.

If you'd rather control exactly when updates go out, add a `"version"` field to the plugin's `.claude-plugin/plugin.json` and bump it on each release. Then users only update when that number changes.

## Repo layout

```
.claude-plugin/marketplace.json     <- the catalog that lists both plugins
plugins/
  ai-agent-foundation/              <- Foundation plugin (Voice, Brand, Local)
  ai-agent-team/                    <- Team plugin (the nine members)
```

## Questions

Email tracy@porchlyte.com or visit porchlyte.com.

— Tracy

# Onboarding Page Updates

Spec for updating the [Agent AI Studio onboarding page](https://porchlyte.com/wp-content/uploads/2026/06/ash-ai-team-onboarding-13.html).

**Goal:** Replace zip download/upload with GitHub marketplace install (copy/paste commands). Keep steps 1–3, 7–8 as-is in spirit. Align page, repo READMEs, and training materials.

**Two repos (split so users do Foundation first, Team another day):**

- **Foundation:** `PorchLyte/porchlyte-foundations` → installs `ai-agent-foundation`
- **Team:** `PorchLyte/porchlyte-agents` → installs `ai-agent-team`

Replace `PorchLyte` with the actual GitHub owner/org if it changes. The Foundation and Team are separate marketplaces, so they're added and updated independently. This matches the course pacing: Foundation on day one, Team on a later day.

---

## Summary of changes

| Area | Current | New |
|------|---------|-----|
| Steps 04–06 | Download zips, upload via Customize | Marketplace slash commands in Cowork chat (Foundation marketplace on day one, Team marketplace on a later day) |
| Foundation / Team download buttons | Primary install path | Remove or demote to “backup only” (see optional section) |
| FAQ | References zip install | References marketplace install + update command |
| Setup time copy | “~30 minutes straight through” | Two-session workshop timing (recommended for live training) |
| New content | — | “How to get updates” section + optional zip fallback |

**Do not change:** Steps 01–03 (Pro, desktop app, privacy), step 07 (`/foundations-setup`), step 08 (`/set-me-up`), team character cards, connectors section, testimonial CTA.

---

## Checklist: replace steps 04–06

Renumber stays **01–08**. Only steps 04–06 get new copy.

Foundation and Team are separate marketplaces. Steps 04–05 (Foundation) happen on day one. Step 06 (Team) happens on a later day, after the Foundation interviews are done — that's the whole point of the split: don't overwhelm people by installing everything at once.

### Step 04 — Add the Foundation marketplace

**Title:** Add the PorchLyte Foundation marketplace

**Body:**

Open a new chat in the Claude desktop app. Type this command and press Enter:

```
/plugin marketplace add PorchLyte/porchlyte-foundations
```

Claude will connect your account to the PorchLyte Foundation catalog. You only do this once.

**Tip box:**

Run each command in its own message. Wait for Claude to finish before you send the next one.

---

### Step 05 — Install AI Agent Foundation

**Title:** Install AI Agent Foundation

**Body:**

In the same chat, type:

```
/plugin install ai-agent-foundation@porchlyte-foundations
```

That installs Voice, Brand, and Local — the personalization layer every team member reads from. This is the only thing you install today. Once it's in, go to step 07 and run `/foundations-setup`.

**Tip box:**

To confirm it's active: **Customize → Plugins**. You should see **AI Agent Foundation** listed.

---

### Step 06 — Add the Team marketplace and install AI Agent Team

**Title:** Install AI Agent Team (a later day)

**Body:**

Do this step once your Foundation interviews are done — usually a different day, so you're not setting up everything at once. The Team lives in its own marketplace, so you add it separately:

```
/plugin marketplace add PorchLyte/porchlyte-agents
/plugin install ai-agent-team@porchlyte-agents
```

That installs your nine-person AI team (Darla, Chloe, Ella, and the rest). It requires Foundation to be installed and set up first.

**Tip box:**

To confirm both plugins are active: **Customize → Plugins**. You should see **AI Agent Foundation** and **AI Agent Team** listed.

---

### Steps 07–08 — No copy changes

Keep existing copy for `/foundations-setup` and `/set-me-up`.

**Minor tweak for step 07** (optional, one line):

> Takes about 15–20 minutes if you do all three back to back. You can stop after one and come back later.

(Aligns with repo wording.)

---

## New section: Getting updates

Add after the Setup Checklist (before “Start with the Foundations”) or as step 09 if the checklist expands.

**Section title:** Getting updates

**Body:**

When Tracy publishes improvements to your agents, you do not need to download or reinstall anything.

Open a Cowork chat and run whichever you have installed:

```
/plugin marketplace update porchlyte-foundations
/plugin marketplace update porchlyte-agents
```

The first updates your Foundation; the second updates your Team. Claude pulls the latest version automatically. Your Foundation interviews and hired team members stay saved in your account — updates only change how the agents work, not your personalization.

---

## Optional section: Zip backup (collapsed or footer)

Use only if someone cannot get marketplace install working during a live session. Do not feature prominently on the main checklist.

**Title:** Backup: install from zip files

**Body:**

If the commands above do not work, you can still install manually:

1. Download [ai-agent-foundation.zip](https://members.porchlyte.com/wp-content/uploads/2026/05/ai-agent-foundation.zip) and [ai-agent-team.zip](https://members.porchlyte.com/wp-content/uploads/2026/05/ai-agent-team.zip).
2. In the Claude desktop app: **Customize → Plugins → Add → Upload plugin**.
3. Upload Foundation first, then Team.

Zip installs do not update automatically. Switch to the marketplace commands above when you can so you get future updates with one command.

---

## “Start with the Foundations” section

### Remove or replace download button

**Remove:** `[ Download Foundation ]` button (or replace with link to step 05 if you want an anchor, not a zip).

**Optional replacement button label:** `See install steps` → scrolls to checklist step 05.

Card copy (Voice, Brand, Local) — **no changes needed.**

---

## “Your Team” section

### Remove or replace download button

**Remove:** `[ Download Team ]` button (or replace with `See install steps` → checklist step 06).

Character cards — **no changes needed.**

---

## FAQ updates

### Replace: “What if a slash command doesn't work?”

**New answer:**

First, make sure you ran the install commands for the part you're on. For Foundation that's the marketplace add plus the Foundation install; for Team it's the Team marketplace add plus the Team install. Check **Customize → Plugins** — the plugin you installed should appear.

Second, start a brand-new Cowork chat before running `/foundations-setup` or `/set-me-up`.

Third, close and reopen the desktop app.

That fixes it about 95% of the time. If marketplace install still fails, use the zip backup at the bottom of this page.

---

### Replace: “How long does the full setup take?”

**New answer:**

About 30–40 minutes if you go straight through install, Foundation, and hiring your first team member.

For live workshops, plan two sessions:

- **Session 1 (~20 min):** Claude Pro, desktop app, privacy setting, plugin install, and `/foundations-setup`.
- **Session 2 (~20 min):** `/set-me-up`, hire your first agent (Darla is the most common starting point), and connect Gmail or Calendar if you want.

You do not have to finish everything in one sitting. Your work saves between sessions.

---

### Add: “How do I get updates?”

**Question:** How do I get updates when Tracy improves the agents?

**Answer:**

Run these in any Cowork chat (whichever you have installed):

```
/plugin marketplace update porchlyte-foundations
/plugin marketplace update porchlyte-agents
```

No zip to download. No reinstall. Your voice, brand, and hired team stay as you set them up.

---

### Add: “Do I need to reinstall when something changes?”

**Question:** Do I need to reinstall when something changes?

**Answer:**

No. Run `/plugin marketplace update porchlyte-foundations` and/or `/plugin marketplace update porchlyte-agents` to pull the latest version. Only use the zip backup if marketplace install is not working for you.

---

### Update: “Do I need to install the plugins on every device?”

**Keep question.** Update answer to mention marketplace:

**New answer:**

Yes, but only on devices where you will use Cowork. On each device, run the install commands from the checklist — the Foundation marketplace add and install, and (once you're on the Team) the Team marketplace add and install. You do not need to repeat `/foundations-setup` or `/set-me-up` on every device unless you want separate personalization there — your main setup lives in your Claude account.

*(Verify this behavior with a two-device test before publishing; adjust if Claude sync differs.)*

---

## Live training handout (copy-paste block)

Include on the page or as a printable sidebar for workshop attendees.

```
DAY ONE — FOUNDATION (run one at a time in Cowork chat)

1. /plugin marketplace add PorchLyte/porchlyte-foundations
2. /plugin install ai-agent-foundation@porchlyte-foundations
3. /foundations-setup

A LATER DAY — TEAM

4. /plugin marketplace add PorchLyte/porchlyte-agents
5. /plugin install ai-agent-team@porchlyte-agents
6. /set-me-up

UPDATES (anytime)

/plugin marketplace update porchlyte-foundations
/plugin marketplace update porchlyte-agents
```

**Trainer note:** Recommend Darla as the first hire during `/set-me-up`. Have Gmail ready if they want Darla’s full morning brief.

---

## Workshop timing (for trainers, not necessarily on page)

| Session | Steps | Time | Outcome |
|---------|-------|------|---------|
| 1 (Foundation day) | 01–05, 07 | ~20 min | Pro, app, privacy, Foundation marketplace + plugin installed, Foundation started or complete |
| 2 (Team day) | 06, 08 + connectors | ~20 min | Team marketplace + plugin installed, first team member hired, optional Gmail/Calendar connect |

The repo split mirrors this: Foundation (`porchlyte-foundations`) is all session 1 needs; the Team marketplace (`porchlyte-agents`) isn't added until session 2.

Do not pressure attendees to hire all nine in one session. `/set-me-up` supports coming back later.

---

## Cross-repo updates (same launch)

These are not on the HTML page but should ship with the page update:

| File | Change |
|------|--------|
| `porchlyte-agents/plugins/ai-agent-team/commands/set-me-up.md` | ✅ Done — `[link]` placeholder replaced with the Foundation marketplace install commands + `/foundations-setup`. |
| `porchlyte-agents/README.md` | Team-only now; points Foundation to the `porchlyte-foundations` repo. Still TODO: add step 03 privacy (“Help improve Claude” off) to match onboarding page |
| `porchlyte-foundations/README.md` | Foundation repo top-level README. Still TODO: add privacy step before install commands |
| `porchlyte-foundations/plugins/ai-agent-foundation/README.md` | Uses the `porchlyte-foundations` marketplace. Still TODO: add privacy step |
| `porchlyte-agents/plugins/ai-agent-team/README.md` | Foundation now installs from `porchlyte-foundations`. Still TODO: add privacy step |

**Note:** the Foundation now lives in its own repo (`PorchLyte/porchlyte-foundations`) so the two install paths are independent — Foundation on day one, Team on a later day.

---

## Longer-term note (private repo)

**Pilot:** Public repo + marketplace commands is fine for the first cohort.

**Before scaling paid access:** Make both GitHub repos (`porchlyte-foundations` and `porchlyte-agents`) private, grant purchasers read access (org invite), keep the same commands on the onboarding page. Optional line for paid cohorts:

> After purchase, accept your GitHub invite from Tracy, then run the install commands below.

Do not publish this line until private-repo access is wired up.

---

## Implementation checklist

- [ ] Replace checklist steps 04–06 with marketplace copy above
- [ ] Add “Getting updates” section
- [ ] Move zip instructions to backup section (de-emphasized)
- [ ] Remove or replace Foundation / Team download buttons
- [ ] Update FAQ (slash commands, timing, updates, multi-device)
- [ ] Add copy-paste command block for workshops
- [ ] Update repo files listed in cross-repo section
- [ ] Test full flow on a clean Claude account before next training
- [ ] Test `/plugin marketplace update porchlyte-agents` after a repo push

---

*Prepared for PorchLyte / Agent AI Studio onboarding. Source repo: `porchlyte-agents`.*

# Renku Cloud plugin

> **Generated. Do not edit.** The Renku Skills release makes this repository from
> [GoRenku/studio-skills](https://github.com/GoRenku/studio-skills)
> v0.4.1 (commit `8d214b430ede2d5e92228f736e880f56b9245d2d`). Every release replaces its contents,
> and GitHub refuses changes from anything but the release. Make skill changes in
> GoRenku/studio-skills.

Renku's filmmaking skills for Claude and Codex, connected to Renku Cloud at
https://app.gorenku.com. Renku Cloud is invite only: sign in with the email
address your invitation was sent to.

## Install

**Claude:** do this on https://claude.ai/customize/plugins in your web browser,
not in the Claude desktop app. The desktop app installs the plugin on that one
computer (marked **Installed locally**), and that copy never updates. A plugin
added on claude.ai is saved to your Claude account, and the desktop app picks
it up from there.

1. **Add** → **Add marketplace**, and enter `GoRenku/renku-cloud-plugin`.
   This adds the marketplace only; Claude lists it as `renku-cloud-plugin`.
2. **Add** → **Manage marketplaces** → **⋯** on `renku-cloud-plugin` → turn on
   **Sync automatically**.
3. Search `renku`, open **Renku cloud**, and select **Add**.
4. On its page, select **Connect** for the `renku` connector and sign in.
5. In the desktop app, start a new Code-tab session once it has picked up the
   plugin, within about 20 minutes.

**ChatGPT app, or the Codex app on Windows:** Settings → Manage plugins,
skills, and MCPs → Add → Add a marketplace, with Source
`GoRenku/renku-cloud-plugin` and the Git ref left empty. Install Renku
Cloud, then select Connect when asked and sign in.

**Terminal:**

```bash
claude plugin marketplace add GoRenku/renku-cloud-plugin
claude plugin install renku-cloud@renku-cloud
claude mcp login plugin:renku-cloud:renku
```

```bash
codex plugin marketplace add GoRenku/renku-cloud-plugin
codex plugin add renku-cloud@renku-cloud
codex mcp login renku
```

## Update

Your app keeps its own copy of this repository and shows a new version only
after it refreshes that copy.

**Claude:** on https://claude.ai/customize/plugins, **Add** → **Manage
marketplaces** → **⋯** on `renku-cloud-plugin` → **Check for updates**. The
desktop app downloads the new version within about 20 minutes; then start a
new session.

**ChatGPT app, or the Codex app on Windows:** neither has an update button.
Codex looks for a new version only when its background service starts, which
can be days apart. To update now, run this in a terminal, then start a new
chat:

```bash
codex plugin marketplace upgrade renku-cloud
```

**Claude Code installed from a terminal or the Code tab:**

```bash
claude plugin marketplace update renku-cloud
claude plugin update renku-cloud@renku-cloud
```

To have Claude Code update it by itself, turn on auto-update for
`renku-cloud` in `/plugin` → Marketplaces.

More: https://gorenku.com/renku-plugins/

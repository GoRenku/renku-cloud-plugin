# Renku Cloud plugin

> **Generated. Do not edit.** The Renku Skills release makes this repository from
> [GoRenku/studio-skills](https://github.com/GoRenku/studio-skills)
> v0.5.1 (commit `c58147c63ffc334babf33c13072556b2e938bc1b`). Every release replaces its contents,
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
2. Search `renku`, open **Renku cloud**, and select **Add**.
3. On its page, select **Connect** for the `renku` connector and sign in.
4. In the desktop app, start a new Code-tab session once it has picked up the
   plugin, within about 20 minutes.

**ChatGPT (Codex):** use the ChatGPT desktop app; ChatGPT on the web can't add
a marketplace. Settings → Manage plugins, skills, and MCPs → Add → Add a
marketplace, with Source `GoRenku/renku-cloud-plugin` and the Git ref
left empty. Install Renku Cloud, then select Connect when asked and sign in.

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
after it refreshes that copy. From 0.5.0, your agent tells you when a newer
version is out, and says so plainly when Renku Cloud needs a newer one to
work correctly.

**Claude:** after each new release, on https://claude.ai/customize/plugins,
**Add** → **Manage marketplaces** → **⋯** on `renku-cloud-plugin` →
**Check for updates**. Don't count on Claude to fetch a new version by itself.
The desktop app can take up to about an hour and a half to download it; then
start a new session.

**ChatGPT (Codex):** the app has no update button. Codex looks for a new
version only when it starts, and the ChatGPT app keeps it running while the
app is open, often for days. After each new release, quit the ChatGPT app
completely (closing its window isn't enough) and open it again, then start a
new chat.

If the new version still isn't there, run the app's own `codex`, then start a
new chat. On a Mac, in Terminal:

```bash
/Applications/ChatGPT.app/Contents/Resources/codex-cli/CodexCLI.app/Contents/MacOS/codex plugin marketplace upgrade renku-cloud
```

On Windows, in PowerShell:

```powershell
& (Join-Path (Get-AppxPackage OpenAI.Codex).InstallLocation 'app\resources\codex.exe') plugin marketplace upgrade renku-cloud
```

With `codex` in your terminal, `codex plugin marketplace upgrade renku-cloud`
does the same.

**Claude Code installed from a terminal or the Code tab:**

```bash
claude plugin marketplace update renku-cloud
claude plugin update renku-cloud@renku-cloud
```

To have Claude Code update it by itself, turn on auto-update for
`renku-cloud` in `/plugin` → Marketplaces.

More: https://gorenku.com/renku-plugins/

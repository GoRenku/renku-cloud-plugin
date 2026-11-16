# Renku Cloud plugin

> **Generated. Do not edit.** The Renku Skills release makes this repository from
> [GoRenku/studio-skills](https://github.com/GoRenku/studio-skills)
> v0.2.0 (commit `47076db202878c129f34a11f90ccb7d511a9ef53`). Every release replaces its contents,
> and GitHub refuses changes from anything but the release. Make skill changes in
> GoRenku/studio-skills.

Renku's filmmaking skills for Claude and Codex, connected to Renku Cloud at
https://app.gorenku.com. Renku Cloud is invite only: sign in with the email
address your invitation was sent to.

## Install

**Claude app or claude.ai:** Customize → Plugins → Add → Add marketplace, and
enter `GoRenku/renku-cloud-plugin`. Add Renku Cloud, then on its
Connectors tab select Add, then Connect, and sign in.

**ChatGPT app (Codex):** Settings → Manage plugins, skills, and MCPs → Add →
Add a marketplace, with Source `GoRenku/renku-cloud-plugin`. Install
Renku Cloud, then select Connect when asked and sign in.

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

More: https://gorenku.com/renku-plugins/

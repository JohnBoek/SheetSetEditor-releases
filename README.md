# SheetSetEditor — Releases

This repository is the **public distribution channel** for BoekSolutions.SheetSetEditor's auto-update feature. It does not contain, and will never contain, application source code.

## What's here

- `update.xml` — the [AutoUpdater.NET](https://github.com/ravibpatel/AutoUpdater.NET) feed the app polls on startup to check for a newer version.
- `CHANGELOG.md` — human-readable release notes, linked from `update.xml`.
- Installer executables are attached to [GitHub Releases](../../releases) as release assets — they are **not** committed into this repository's git history (keeps the repo small and every download traceable through GitHub's release/asset system).

## What's deliberately *not* here

- No application source code — that lives in a private repository.
- No license keys, signing keys, customer data, API tokens, or internal build/deploy configuration.
- No debug or unprotected builds. Every installer published here is a Release build produced by the private repo's canonical `protect/Build-Protected.ps1` pipeline (ConfuserEx-obfuscated) — never a raw `dotnet build` output.
- No secrets of any kind. If you ever find something here that looks like one, please open an issue immediately.

## Publishing process (manual, human-gated — never automated)

A new version is **never** pushed here by a script or CI job. Every release goes through:

1. A full local Release build via `protect/Build-Protected.ps1` in the private source repo.
2. Manual smoke test: standalone app launches, opens a `.dst` file, plugin loads in AutoCAD, installer installs and uninstalls cleanly, settings/license survive an update.
3. Only after that passes: the installer is uploaded as a GitHub Release asset here, `update.xml` is hand-edited to point at the new version/asset/changelog, and `CHANGELOG.md` is updated.

If a release ever needs to be pulled (e.g. a bug found post-publish), `update.xml` is reverted to the previous known-good version first — the update feed is the single source of truth the app trusts, so it is treated with the same care as production infrastructure.

## Security

If you believe a Release asset in this repository was tampered with, or doesn't match what you'd expect from an official BoekSolutions release, **do not run it** — please open an issue here instead of downloading it.

# BoekSolutions Sheet Set Editor

A Windows desktop tool for viewing and editing AutoCAD Sheet Set (`.dst`) data — as a standalone application, or integrated directly into AutoCAD 2027.

## ⬇️ Download

Grab the latest installer from **[Releases](../../releases/latest)**. Run the `.exe`, follow the wizard — no admin rights required.

## What it does

- **Edit Sheet Set data without opening AutoCAD.** Browse sheets, subsets, and custom properties from a standalone app — AutoCAD doesn't need to be running.
- **AutoCAD integration.** Install the optional plugin component and use the `SSM_UI` command from inside AutoCAD 2027 for the same editor, in context.
- **Bulk import from CSV/TSV.** Import wizard for editing custom properties across many sheets at once.
- **Smart Field Groups.** Organize custom properties into your own visual groups/cards — purely a display convenience, your `.dst` file is never restructured.
- **Field linking.** Link two fields together: a value-mapping table (source value → target value), or a live 1-to-1 mirror (edit either field, the other updates automatically) — works across custom properties, standard sheet fields (Number, Title, Description, ...), and sheet set metadata (Project Name, Project Number, ...).
- **Field rules.** Dropdown choice lists, max lengths, date fields, and formula-driven fields ({token} substitution).
- **Drag & drop DWG import**, with automatic detection of layouts already added to a sheet set.
- **10 languages**, including Dutch, English, German, French, Spanish, Italian, Portuguese, Afrikaans, Frisian — and Klingon, for the curious.
- **Three themes**: Light, Dark, and "Book" (a warm parchment-and-gold look).
- **Automatic backups** before every write, with a configurable backup location.
- **Automatic update checks**, so you're always notified when a new version is available.

## Requirements

- Windows 10/11, x64
- AutoCAD 2027 — only needed if you want the in-AutoCAD plugin; the standalone app works without it

## Updates

The app checks for new versions on startup and prompts you when one's available — no manual downloading required after your first install.

## Security

Every installer here is a tested Release build, manually verified before publishing. Note: installers are not yet code-signed, so Windows SmartScreen may warn on first run — click "More info" → "Run anyway" if so. If a Release asset in this repository ever looks tampered with or doesn't match what you'd expect from an official BoekSolutions release, **do not run it** — open an issue here instead.

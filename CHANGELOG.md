# Changelog

Release notes for BoekSolutions.SheetSetEditor, in sync with `update.xml` and the version tags on this repo's [Releases](../../releases) page.

## 1.1.5

- Security: strengthened how license keys are generated and validated. If you have an existing
  license and it's no longer recognized after updating, this is expected — email
  info@boeksolutions.nl with your Machine ID for a replacement key, a one-time step.

## 1.1.4

- Fixed: the update download could fail with an error for anyone updating from 1.1.2 or earlier —
  the installer link had gone stale after a naming change on the release side.
- Fixed: Options > Info could claim "latest version installed" even when the update check itself
  had actually failed (for example due to a network problem) — it now says clearly that the check
  failed instead of falsely suggesting you're up to date.
- New: a "Check for updates" button in Options > Info, so you can check again right away instead of
  having to restart the app.

## 1.1.3

- New: sheet and field names with accented letters, Cyrillic, Greek, Hebrew, Arabic, CJK
  (Chinese/Japanese/Korean), Thai, Devanagari, Georgian, Armenian, and emoji now read and save
  correctly — previously these could show up as "*" or other garbled characters, and in some
  cases saving one could silently corrupt an unrelated field elsewhere in the same file.
- Fixed: renaming a sheet or subset via the right-click menu didn't immediately update the
  properties panel — clicking Apply right after could silently undo the fresh rename.
- Improved: clearer error messages — saving a file with a character that isn't supported yet now
  tells you exactly which one, instead of risking a corrupted file; opening a file AutoCAD wrote
  with such a character now explains what happened instead of suggesting the file is locked.

## 1.1.2

- Fixed: linking a sheet set's own fields (like Project Number) to each other never actually
  worked — that panel had no way to set up a field link at all until now.
- Fixed: linking a sheet set field to a sheet field (or vice versa) could silently do nothing,
  since a single sheet-set-wide value and a per-sheet value don't line up — the field-link picker
  now only offers matching fields, both inline and in Options.
- Fixed: when two fields were mirrored, only one side showed the green "linked" icon.
- New: right-click a field's link icon to clear its value directly, even without an active link —
  useful for date/choice fields that previously couldn't be emptied through the UI.
- Fixed: removing a field link left the old value behind instead of clearing it.
- Fixed: date fields were unreadable (black text) in Dark and Book theme.
- Fixed: switching themes while a date field had a value could silently clear it.
- Improved: the calendar picker for date fields now closes itself as soon as you pick a date.

## 1.1.1

- Fixed: app could crash on launch when a second instance was started while one was already
  running (single-instance detection released a lock it never owned).
- Fixed: Options window sidebar didn't pick up the Light/Book theme colors, always showing a
  plain near-white background regardless of theme.
- Improved: Options sidebar now has a subtle "book cover" shadow gradient in Light/Book themes.
- New: in-app update checking — the app can now notify you when a new version is available.

## 1.1.0 — baseline

First version tracked through this update channel. No changelog entries prior to this point are recorded here.

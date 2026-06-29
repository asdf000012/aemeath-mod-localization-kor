# Translation Guide

Thank you for helping translate the Aemeath mod.

## What To Edit

Only edit files under `localization/<language>/`.

Each language folder should contain the same JSON files and the same JSON keys as the existing `eng` and `zhs` folders.

## What Not To Change

- Do not rename JSON keys.
- Do not remove formatting tags such as `[img]...[/img]`, `[color]...[/color]`, or `{0}` placeholders.
- Do not change file names.
- Do not edit source code or image assets in this repository.

## Korean Translation

For Korean, please create a folder named:

```text
localization/kor/
```

If the game or mod loader expects a different Korean locale code, we can rename the folder later before integration.

## JSON Check

After editing, please make sure every changed file is still valid JSON.

On PowerShell, one quick check is:

```powershell
Get-ChildItem localization\kor\*.json | ForEach-Object { Get-Content -Raw $_.FullName | ConvertFrom-Json -AsHashtable > $null }
```

# CrashBytes Scoop bucket

[Scoop](https://scoop.sh) manifests for CrashBytes CLIs on Windows.

## Install

If you don't have Scoop yet, follow https://scoop.sh — one PowerShell
command and you're in.

```powershell
scoop bucket add crashbytes https://github.com/CrashBytes/scoop-bucket
scoop install pipemason
```

After that, `scoop update pipemason` keeps you on the latest release.

## What's here

| Manifest | What it installs |
|---|---|
| `pipemason` | Local runner for the [pipemason](https://pipemason.com) development pipeline. Pulls the same `pipemason-windows-x64.exe` artifact that ships with every `v*` release. |

macOS / Linux users: use Homebrew instead — `brew install
CrashBytes/tap/pipemason`. See [pipemason.com](https://pipemason.com).

## How updates happen

The `bump-scoop-bucket` job in the [`CrashBytes/pipemason`](https://github.com/CrashBytes/pipemason)
release workflow regenerates `bucket/pipemason.json` on every `v*` tag
once the public mirror at `CrashBytes/pipemason-binaries` has the new
artifacts. Do not hand-edit the manifest — your changes will be
overwritten on the next release.

## Reporting issues

CLI bugs / behavior: see [pipemason.com](https://pipemason.com).
Manifest problems (won't install on Windows, wrong hash): file here.

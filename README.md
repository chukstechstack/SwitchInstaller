# Switch Installer

A Windows installer for the Switch desktop application, built with WiX and designed for a clean, reliable installation experience.

## Overview

This project packages the compiled Switch app into a standard Windows installation flow. It installs the application into the Program Files directory, includes the required .NET runtime files, creates a desktop shortcut, and lets the user launch the app immediately after installation.

## Features

- Clean Windows installer workflow
- .NET 8 app deployment
- Program Files installation structure
- Desktop shortcut creation
- Upgrade-aware installer behavior
- Optional launch after install
- Minimal and professional setup UX

## Project Files

```text
SwitchInstaller/
├── README.md
├── SwitchInstaller.wixproj
├── Product.wxs
├── HarvestedFiles.wxs
├── bin/
│   └── build output
├── obj/
│   └── intermediate build output
└── ...
```

## Build Requirements

- Windows 10/11
- WiX Toolset v3.11+
- .NET SDK 8+
- Visual Studio 2022 or compatible MSBuild environment

## Build

From the project folder:

```powershell
msbuild SwitchInstaller.wixproj /p:Configuration=Release
```

Or build directly in Visual Studio using the WiX project file.

## Install Behavior

When the installer runs, it will:

1. Install the required application files to the target folder
2. Place the app under the `net8.0-windows` directory
3. Add a desktop shortcut for quick access
4. Offer the option to launch Switch immediately after setup completes

## Notes

This installer is intended for Windows deployment and is tuned for a lightweight but professional end-user experience.

## Author

C.E Kingsley

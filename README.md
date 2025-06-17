# Fly Solo

**Fly Solo** is a modular PowerShell tool that helps users disable unwanted Microsoft Windows features such as Copilot, Cortana, telemetry, ads, and other bloatware. It provides a clean, graphical interface built with Windows Forms, along with automatic backups and a restore manager for safe configuration changes.

---

## Features

- Disable Copilot, Cortana, telemetry, and adware
- Modular tweak system — just drop in `.ps1` scripts
- Simple GUI built with WinForms
- Registry + App backup and restore
- Fully customizable and extensible

---

## Requirements

- Windows 10 or 11
- PowerShell 5.1+
- Admin privileges to make system changes

---

## Getting Started

1. **Clone or Download the Repository**
    ```powershell
   git clone https://github.com/your-username/flysolo.git
   cd flysolo
2. Run the Tool
    ```powershell
    powershell -ExecutionPolicy Bypass -File .\flysolo.ps1
Select the tweaks you want from the GUI and apply them!

## Creating New Modules
To add a new tweak, create a .ps1 file in the modules/ folder. Each module must include:

    # @name Your Module Name
    # @desc (Optional) Description shown in tooltip
      
    function Invoke-FlySolo-Tweak {
      # Your tweak code here
    }

Modules are automatically detected and added to the GUI.

## Restore Manager
Fly Solo creates a registry and app list backup before applying any tweaks. You can launch the Restore Manager from the main window to revert changes.

Backups are stored in the backups/ folder and include:

.reg file of the user registry hive

apps.txt list of current AppX packages

## Project Structure

    FlySolo/
    ├── flysolo.ps1          # Main launcher
    ├── flysolo.ico          # Optional icon for the GUI
    ├── modules/             # Folder for tweak modules
    │   └── disable-copilot.ps1
    ├── backups/             # Generated automatically
    ├── LICENSE              # MIT License
    └── README.md            # You're reading it!

## License
This project is licensed under the MIT License — see LICENSE for details.
You are free to use, modify, and distribute this software with proper attribution.

## Contributing
Pull requests are welcome! If you have a useful tweak, create a new .ps1 file under modules/ following the template. Please test your changes before submitting.

## Disclaimer
This tool modifies system settings and registry keys. Use at your own risk. Always ensure a backup is created before applying tweaks.

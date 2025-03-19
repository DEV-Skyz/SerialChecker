# System Information Script

## Overview
This batch script gathers and displays system-related information, such as serial numbers, installed software, and hardware details. It provides a simple menu for users to choose what information they want to see.

## Features
- Displays system serial numbers for various components including CPU, GPU, RAM, and more.
- Shows installed software (optional feature).
- Retrieves IP addresses, network adapter details, and TPM information.
- Works with Windows and leverages PowerShell commands to extract system details.

## Requirements
- Windows OS
- PowerShell installed (default on Windows 7 and later)
- NVIDIA GPU (for `nvidia-smi` command to work, otherwise it will fail)

## Usage
1. Run the script by double-clicking on it.
2. A menu will appear with the following options:
   - `1` Show Serial Numbers
   - `2` Show Installed Software (Optional)
   - `3` Exit
3. Select the desired option:
   - If `1` is chosen, system serial numbers and hardware details will be displayed.
   - If `2` is chosen, the script will prompt whether to display installed software before showing system details.
   - If `3` is chosen, the script exits.

## Information Retrieved
- **GPU:** Name, Serial, UUID (requires NVIDIA GPU and `nvidia-smi` command)
- **Baseboard (Motherboard):** Product, Manufacturer, Version, Serial Number
- **BIOS:** Serial Number, SMBIOS Version
- **CPU:** Serial Number, Processor ID
- **Computer System Product:** Identifying Number, UUID
- **Disk Drive:** Model, Serial Number
- **RAM:** Serial Number
- **Network Adapters:** Device ID, Name, MAC Address
- **TPM (Trusted Platform Module):** SHA256 Public Key Hash
- **Windows Product Key**
- **IP Addresses**

## Notes
- Administrator privileges may be required for some PowerShell commands.
- The script uses `chcp 65001` to ensure UTF-8 encoding for proper character display.
- Some PowerShell commands may take time to execute, especially for retrieving installed software.




# Virtual Machine Environment Setup

## Virtual Machine Configuration
- **Virtualization Software:** VMware Fusion
- **Operating System:** Ubuntu Server 24.04
- **Memory:** 4GB
- **Disk Space:** 40GB
- **Processors:** 2 cores
- **Network:** Bridged

## Installation Steps
1. **Download Ubuntu Server:**
   - [Ubuntu Server Download](https://ubuntu.com/download/server)
2. **Install VMware Fusion on macOS.**
3. **Create a new VM:**
   - Select the Ubuntu Server ISO.
   - Choose UEFI as the firmware type.
4. **Configure VM resources:**
   - Set memory, disk space, and processors.
5. **Install Ubuntu Server:**
   - Select OpenSSH Server during setup.
   - Skip additional snaps for now.

## Post-Installation
- **Update System:**
  ```bash
  sudo apt update && sudo apt upgrade

  •	Install essential packages:
  sudo apt install openssh-server git

## Graphical Interface Installation

### Change of Plan
Initially, I planned to use the command-line interface, but I decided to switch to a graphical interface for ease of use.

### Desktop Environment
- **Desktop Environment:** Xubuntu
- **Installation Command:**
  ```bash
  sudo apt install xubuntu-desktop

  	•	Reboot the System:
  sudo reboot

	•	Log in with your user credentials after the reboot.

# Change in Setup

Initially, I planned to use a virtual machine with Ubuntu Server on my MacBook Air M1. However, I encountered compatibility issues:

1. **ARM Architecture**:
   - Splunk Enterprise is primarily designed for x86_64 architectures.
   - The M1 chip uses ARM architecture, leading to compatibility issues with Splunk packages.

2. **Ubuntu on M1**:
   - While Ubuntu supports ARM, Splunk does not fully support ARM on Linux, causing installation problems.

### Reasons for Change:

- **Better Support**: Splunk runs natively on macOS with Rosetta 2.
- **Performance**: Avoids virtualization overhead, utilizing the M1's capabilities.
- **Ease of Use**: Simplifies the setup process on macOS.

### Updated Setup:

- **Operating System**: macOS M1
- **Splunk Version**: Splunk Enterprise
- **Installation Path**: `/Applications/Splunk/`

### Commit the Changes:

- Write a commit message like "Updated to use macOS M1 for Splunk due to ARM compatibility issues."

### Introducing Linux and Unix
* Unix is family of operating systems
* Linux is Unix-based OSs
* Linux is popular for uses cases such as mobile-devices, supercomputers, data centers, and cloud servers.

### Video•. Duration: 5 min - Linux Distributions
* Linux distros differences:
  - System utilities
  - Graphical User Interface (GUI)
  - Shell commands
  - Support types
    - Community versus Enterprise
    - Long-term support (LTS) versus rolling release

* Linux distros: Debian - First release in 1993
  - Open source
  - Supports many computer architectures

* Linux distros: Ubuntu (Debian-based) - First release in 2004
  - Ubuntu Desktop
  - Ubuntu Server
  - Ubuntu Core

* Linux distros: Red Hat Linux
  - like debian, "core" linux distro
  - Red Hat Enterprise Linux (RHEL)

* Linux distros: Fedora - stable operating system
  - Supports many architectures
  - Sponsored by Red Hat

* Linux distros: SUSE Linux Enterprise (SLE)
  - Server (SLES)
  - Desktop (SLED)
  - Supports many architectures
  - SUSE package hub

* Linux distros: Arch Linux
  - Do it yourself approach
  - Required knowledge about Linux OSs

### Video•. Duration: 5 min - Overview of Linux Architecture
```
Includes:
- UI
- Application
- Operating systems
- Kernel
- Hardware
```

* UI
* Application
  ```Include: Sytem tools, Programming languages, Shells, User apps (such as browsers, text editors, games)```
  - System daemons
  - Shells
  - User apps
  - Tools
* Operating systems ```perform file management tasks```
* Kernel
  ```
  perform vital operations
  starts on boot
  bridge between apps and hardware

  Key jobs:
  Memory management
  Process management
  Device drivers
  Security
  ```
* Hardware
  ```
  Includes:
  CPU
  RAM
  Storage
  Screen
  USB devices
  ```

* Linux filesystem
  ```
  /bin
  /usr
  /home
  /boot
  /media
  (/sbin, /etc, /dev, /proc, /var, /tmp, /lib, /opt, /mnt, /srv)
  ```

### Video•. Duration: 6 min - Linux Terminal Overview
* Linux shell
  - OS-level application that interprets commands
  - Shells:
    - Bash
    - Zsh
* Linux terminal
  - An application you use to interact with the shell
  - Enter comnands and receive output from them
  - Communicating with Linux system
  
* Linux terminal and shell work together
  ```
    +--------+   +--------+   +---------------+   +--------+
    |        |-->|        |-->|               |-->|        |
    |  User  |   |Terminal|   |Shell OS Kernel|   |Hardware|
    |        |<--|        |<--|               |<--|        |
    |        |   |        |   |               |   |        |
    +--------+   +--------+   +---------------+   +--------+

    ```

* Use a Linux terminal to navigate directories
  - Special paths
    - ~ Home directory
    - / Root directory
    - .. Parent directory
    - . Current directory

### Reading: Browsing directories with the Linux terminal

### Ungraded Plugin - Reading: Linux Terminal Tips - Tab completion, command history

### Ungraded Plugin - Hands-on Lab: Getting Started with the Linux Terminal

### Ungraded App Item•. Duration: 115 min - Creating and Editing Text Files
* Popular text editors
  * Command-line text editors
    - GNU nano
    - vi
    - vim
  * GUI-based text editors: gedit
    - Integrated file browser
    - Undo and redo
    - Search and replace
    - Extensibility
  * Command-line or GUI
    - emacs 

### Hands-on Lab: Installing and working with text editors

### Video•. Duration: 6 min - Installing Software and Updates
* Packages and package managers
  * Packages: archive files
  * Packages managers
    - Manage the download and installation of packages
    - Available for different Linux distros
    - Can be GUI-based or command-line tools
* Deb and RPM packages
  * Packages for Linux OS
  * Distinct file types for different Linux OS
  * .deb files
    - For Debian-based distributions such as Debian, Ubuntu, and Mint
    - deb stands for Debian
  * .rpm files
    - For Red Hat-bases distributions such as CentOS/RHEL, Fedora, and open SUSE
    - RPM stands for Red Hat Package Manager
  * deb and rpm format are equivalent
  * If a package is only available in one format, you can you alien to convert it
    - RPM to deb
    ```bash
    alien <package-name>.rpm
    ```
    - deb to RPM
    ```bash
    alien -r <package-name>.deb
    ```
* Package managers
  * Benefits
    - Automatically resolve dependencies
    - GUI-based package managers can automatically check for updates
    - Automatic or manual installation
  * Linux distro package managers include PackageKit and Update Manager
* Updating deb-bases Linux
  * GUI tool: Update Manager
  * Command line: apt
    ```bash
    sudo apt upgrade
    ```
  * GUI tool: PackageKit
  * Command line tool: Yum
* Other software package managers
  * Python package managers include pip and conda
### Video•. Duration: 6 min - Cheat Sheet: Introduction to Linux

### Ungraded Plugin•. Duration: 3 min - Summary & Highlights

### Reading•. Duration: 2 min - Practice Quiz: Introduction to Linux

### Practice Quiz•5 questions
Upgrade to unlock - Graded Quiz: Introduction to Linux

### Status: Upgrade to unlock
Upgrade to unlock - Quiz•10 questions

# Introduction to Linux Commands
![image](https://github.com/dtlam2601/bash-shell/assets/12412633/15bff1d2-5e97-468e-a031-f1dc95b5ec0f)

## Informational, Navigational, & Management Commands
### Video: Overview of Common Linux Shell Commands
. Duration: 6 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/3lRqW/overview-of-common-linux-shell-commands)
* What is a shell?
  * User interface for running commands
  * Interactive language

* A sea of shell
  * Default shell is usually Bash
  * Many other shells, including sh, ksh, tcsh, zsh, and fish
  * This course uses Bash
  ```bash
  # print the default shell program
  printenv SHELL
  ```
* Shell command applications
  * Getting information
  * Navigating and working with files and directories
  * Printing file and string contents
  * Compression and archiving
  * Performing networking operations
  * Monitoring performance status
  * Running batch jobs

* Getting information
  ```text
  whoami - username
  id - user ID and group ID
  uname - operating system name
  ps - running process
  top - resource usage
  df - mounted file systems
  man - reference manual
  date - today's date
  ```
* Working with files
  ```text
  cp - copy file
  mv - change file name or path
  rm - remove file
  touch - remove empty file, update file timestamp
  chmod - change/modify file permissions
  wc - get count of lines, words, characters in file
  grep - return lines in file matching pattern
  ```

* Navigating and working with directories
  ```text
  ls - list files and directories
  find - find files in directory tree
  pwd - get present working directory
  mkdir - make directory
  cd - change directory
  rmdir - remove directory
  ```

* Printing file and string contents
  ```text
  cat - print file contens
  more - print file contents page-by-page
  head - print first N lines of file
  tail - print last N lines of file
  echo - print string or variable value
  ```

* Compression and archiving
  ```text
  tar - archive a set of files
  zip - compress a set of files
  unzip - extract files from  a compressed zip archive
  ```

* Networking
  ```text
  hostname - print hostname
  ping - send packets to URL and print response
  ifconfig - display or configure system network interfaces
  curl - display contents of file at a URL
  wget - download file from URL
  ```

* Running Linux on a Windows machine
  ```text
  Dual boot with a partition
  Install Linux on a virtual machine
  Use a Linux emulator (Cygwin)
  Windows Subsystem for Linux (WSL)
  ```

### Video: Informational Commands
. Duration: 8 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/hqkCy/informational-commands)

* User Information
  ```text
  Display user information
  Verify identity or identity user account
  whoami - returns user name
  id (identity) -u -n - user or group ID
  ```

* System information
  * uname (Unix name) - return OS information
    - Identity system or diagnose issues
  ```bash
  uname
  uname -s -r
  uname -v
  ```

* Displaying your disk usage
  * df (disk free) - Shows disk usage
    - Monitor disk usuge or check space
  ```bash
  df
  df -h ~
  ```

* Displaying running processes
  * ps (process status) - Running processes
    - Monitor or manage processes
  ```bash
  ps
  ps -e
  ```

* Monitoring system health and status
  * top (table of processes) - Task manager
    - Monitor system performance and resource usage
  ```bash
  top
  top -n 3
  ```

* Printing strings and variable values
  * echo - Print string or variable value
  ```bash
  echo
  echo ""
  echo $PATH
  ```

* Getting date information
  * date - Displays system date and time
  ```bash
  date
  date "+%d/%m/%y"
  date "+%d/%m/%Y"
  # %j, %A, %Y
  ```

* Viewing the manual
  * man (manual) - Shows manual for any commands
  ```bash
  man id
  ```


### Ungraded Plugin: Reading: Getting Help for Linux Commands
. Duration: 3 min - Link

###  ItemHands-on Lab: Informational Commands
. Duration: 330 min - Link

### Video: File and Directory Navigation Commands
. Duration: 4 min - Link

### Video: File and Directory Management Commands
. Duration: 7 min - Link

###  ItemHands-on Lab: Navigating and Managing Files and Directories
. Duration: 330 min - Link

### Reading: Security - Managing File Permissions and Ownership
. Duration: 4 min - Link

###  ItemHands-on Lab: Access Control Commands
. Duration: 110 min - Link

### Practice Quiz: Informational, Navigational, & Management Commands
. Duration: 6 min - Link


## Working with Text Files, Networking & Archiving Commands
### Video: Viewing File Content
. Duration: 3 min - Link

### Video: Useful Commands for Wrangling Text Files
. Duration: 5 min - Link

###  ItemHands-on Lab: Wrangling Text Files at the Command Line
. Duration: 440 min - Link

### Reading (Optional): A Brief Introduction to Networking
. Duration: 3 min - Link

### Video: Networking Commands
. Duration: 6 min - Link

###  ItemHands-on Lab: Working with Networking Commands
. Duration: 330 min - Link

### Video: File Archiving and Compression Commands
. Duration: 6 min - Link

###  ItemHands-on Lab: Archiving and Compressing Files
. Duration: 115 min - Link

### Practice Quiz: Practice Quiz: Text Files, Networking & Archiving Commands
. Duration: 6 min - Link

## Module Summary and Assessment
### Reading: ReadingModule Summary & Highlights
. Duration: 2 min - Link

### Cheat Sheet: Introduction to Linux Commands
. Duration: 110 min - Link

### Upgrade to unlock
Quiz: Graded Quiz: Linux Commands
. Duration: 330 min - Link

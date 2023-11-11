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
. Duration: 3 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/VmOux/reading-getting-help-for-linux-commands)
* 1. Use the built-in man command
man -k .

* 2. Install and use the tldr command
Similar to man pages
npm install -g tldr
tldr command_name

* 3. Search Stack Overflow
Newest questions on Stack Overflow tagged "Linux": https://stackoverflow.com/questions/tagged/linux

* 4. Search Stack Exchange
Unix and Linux community on Stack Exchange: https://unix.stackexchange.com/

* 5. Just google it!
Learn how to enter the right queries and filter your results, such as by including "Wikipedia", "Stack Overflow", or "Linux" as part of your search.

* 6. Use the cheat sheets from this course
Throughout this course, you will encounter "cheat sheets" that condense the information you've learned into easy-to-reference guides. They are great for reviewing the material you've learned and can also help you out with your graded assignments.

* 7. Refer to Wikipedia's list of Unix commands:
Finally, Wikipedia maintains a list of commands that can be found on Unix operating systems, along with a short description. You can check the page to quickly reference a Unix command: https://en.wikipedia.org/wiki/List_of_Unix_commands
```


###  Hands-on Lab: Informational Commands
. Duration: 330 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/ZFgCW/hands-on-lab-informational-commands)

### Video: File and Directory Navigation Commands
. Duration: 4 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/OFZjk/file-and-directory-navigation-commands)

* Listing your directory contents
  - ls (list) - list files and directories
  ```text
  ls
  ls folder
  ls -l 
  ```

* Finding your working directory
  - pwd (print working directory) - get current working directory

* Navigating your directory - Relative and absolute navigation
  - cd (change directory) - change directory
  ```text
  cd ..
  cd ~ # tilde symbol
  cd /
  ```

* Finding files
  - find - find files in directory tree
  ```mermaid
  graph TD;
      Documents-->folder1;
      Documents-->folder2;
      folder1-->a.txt;
      folder1-->b.txt;
      folder2-->A.txt;
      folder2-->Y.txt;
      folder2-->Z.txt;
  ```
  ```text
  pwd
  find . -name "a.txt"
  ./folder1/a.txt

  # find case-insensitive
  find . -iname "a.txt"
  ./folder1/a.txt
  ./folder2/A.txt
  ```

### Video: File and Directory Management Commands
. Duration: 7 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/pwUDl/file-and-directory-management-commands)
* Creating directories
  - mkdir (make directory) - Make directory

* Removing files and directories
  - rm (remove) - Remove file or directory
  ```text
  rm file1
  rm -r folder1

  mkdir empty_folder
  rmdir empty_folder
  ls
  ```

* Creating files
  - touch - Create empty file, update file date
  ```text
  touch a.txt b.txt c.txt d.txt

  date -r a.txt
  touch a.txt
  date -r a.txt
  ```

* Copying files and directories
  - cp (copy) - Copy file or directory to destination
  ```text
  To copy files:
  cp /source/file /dest/filename
  cp /source/file /dest/

  To copy directories:
  cp -r /source/dir/ /dest/dir/
  ```

* Moving files and directories
  - mv (move) - Move a file or directory
  ```text
  To move files:
  mv /source/file /dest/file

  To move directories:
  mv /source/dir/ /dest/dir/
  ```

* Managing file permissions
  - chmod (change mode) - Change file permissions
  ```text
  chmod +x my_script.sh
  ./my_script.sh
  ```

###  Hands-on Lab: Navigating and Managing Files and Directories
. Duration: 330 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/RKRTp/hands-on-lab-navigating-and-managing-files-and-directories)

### Reading: Security - Managing File Permissions and Ownership
. Duration: 4 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/AnNec/reading-security-managing-file-permissions-and-ownership)

###  Hands-on Lab: Access Control Commands
. Duration: 110 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/wXPUJ/hands-on-lab-access-control-commands)

| Note: You might be wondering what that s permission is in the execute slot for your group. The s stands for "special permission". It means that any new files created within the directory will have their group ownership set to be the same as the directory owner. We won't go into this level of detail in this course, but you can learn more about advanced Linux permissions here:[ Linux permissions: SUID, SGID, and sticky bit](https://www.redhat.com/sysadmin/suid-sgid-sticky-bit?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMLX0117ENSkillsNetwork860-2023-01-01#:~:text=Commonly%20noted%20as%20SUID%2C%20the,use%20an%20uppercase%20S%20here.).

### Practice Quiz: Informational, Navigational, & Management Commands
. Duration: 6 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/quiz/VTAGj/practice-quiz-informational-navigational-management-commands)


## Working with Text Files, Networking & Archiving Commands
### Video: Viewing File Content
. Duration: 3 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/NRDyr/viewing-file-content)
* Viewing your file all at once
  - cat (catenate) - Print entire file contents

* Viewing your file page-by-page
  - more - Print file contents page-by-page

* Viewing the first N lines
  - head - Print first 10 lines of file
  - head -n N - Print first N lines of file

* Viewing the last N lines
  - tail - Print last 10 lines of file
  - tail -n N - Print last N lines of file

* Counting lines, words, and characters
  - wc (word count) - Count characters, words, lines

```text
cat file.txt
more file.txt
less file.txt

head file.txt
head -n 5 file.txt
head -5 file.txt

tail file.txt
tail -n 5 file.txt

wc file.txt
# line, word, character
wc -l file.txt
wc -w file.txt
wc -c file.txt
```

### Video: Useful Commands for Wrangling Text Files
. Duration: 5 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/frBog/useful-commands-for-wrangling-text-files)
* Sorting your view line-by-line
  - sort - Sort lines in a file 

* Excluding repeated lines from views
  - uniq (unique) - Filter out repeated lines

* Extracting lines matching a pattern
  - grep (global regular expression print) - Return lines in file matching pattern

* Extracting slices from lines
  - cut -c - Extracts a section from each line
  - cut -d - Extracts a field from each line

* Merging lines from multiple files
  - paste - Merge lines from different files

```text
sort file.txt
sort -r file.txt

cat file.txt

# for case-sensitive and case-insensitive
grep ch file.txt
grep -i ch file.txt

cut -c 2-9 people.txt
cut -d ' ' -f2 people.txt

paste first.txt last.txt yob.txt
paste -d "," first.txt last.txt yob.txt
```

###  Hands-on Lab: Wrangling Text Files at the Command Line
. Duration: 40 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/Zhpj8/hands-on-lab-wrangling-text-files-at-the-command-line)

### Reading (Optional): A Brief Introduction to Networking
. Duration: 3 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/bJwJZ/reading-optional-a-brief-introduction-to-networking)

* Computer Networks
  - A computer network is a set of computers that are able to communicate with each other and share resources provided by network nodes.
  - A network resource is any object, such as a file or document, which can be identified by the network.
  - A network node is any device that participates in a network.

* Hosts, Clients, and Servers
  - A host is a special type of node in a computer network - it is a computer that can function as a server or a client on a network.
  - A server is a host computer that is able to accept a connection from a client host and fulfill certain resource requests made by the client.
  - Many hosts can perform either role, acting as both client and server.

* Packets and Pings
  - A network packet is a formatted chunk of data that can be transmitted over a network.
  - Today's computer networks typically use communication protocols that are based on such packets of information. Every packet consists of two types of data: 1. the control information, and 2. the payload. The control information is data about how and where to deliver the payload, such as the source and destination network addresses, while the payload is the message being sent.
  - The ping command works by sending special 'echo request' packets to a host and waiting for a response from the host.

* URLs and IP Adresses
  - IP stands for "Internet Protocol" which defines the format of data transmitted over the internet or a local network.
  - An IP address is a code used to uniquely identify any host on a network.
  - An IP address can be used to establish a connection to a host and exchange packets with it, for example using the ping command. In addition to their payload, IP packets - a type of network packet that conforms to the Internet Protocol - contain the IP addresses of the source and destination hosts.
  - A URL, more commonly known as a web address, stands for Uniform Resource Locator.

### Video: Networking Commands
. Duration: 6 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/46KpH/networking-commands)
* Getting your machine's host name
  - hostname - Print host name

* Getting network information - ethernet adapter info
  - ifconfig (Interface configuration) - Display or configure the system network interfaces 

* Testing server connections
  - ping - Send ICMP packets to URL and print response

* Web scraping with curl - a web page's HTML to file
  - curl (Client URL) - Transfer data to and from URL(s)

* Downloading files from a URL
  - wget (Web get) - Download file(s) from a URL
  - more focused than curl, supports recursive file downloads

```text
hostname
hostname -s
hostname -i

ifconfig
ifconfig eth0

ping www.google.com
ping -c 5 www.google.com

curl www.google.com
curl www.google.com -o google.txt

wget https://www.w3.org/TR/PNG/iso_8859-1.txt
```

* Recap
  - The hostname command is used to get or set the hostname.
  - The ifconfig command displays information regarding all your device's communication devices.
  - You can use the ping command to test connectivity to a host or IP address.
  - The curl command enables you to transfer data to and from URLs.
  - The wget command is used to retrieve files located at a URL.

###  Hands-on Lab: Working with Networking Commands
. Duration: 30 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/Jf9iq/hands-on-lab-working-with-networking-commands)

### Video: File Archiving and Compression Commands
. Duration: 6 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/KDMpO/file-archiving-and-compression-commands)
* Archiving and compression
  * Archives
    - stores rarely used information and preserve it
    - are a collection of data files and directories stored as a single file
    - make the collection more portable and serve as a backup in case of loss or corruption
  * File compression
    - reduces file size by reducing information redundancy
    - preserves storage space, speeds up data transfer, and reduces bandwidth load

* Directory tree archiving
  - ls -r

* File archiving and compression
  * tar (tape archiver) - Archive and extract files
  * Checking your archive contents
  - tar - List archive contents
  * Extracting archived files
    - tar - Extract files and folders
  * Decompressing and extracting archives
    - tar - Decompress and extract

* File compression and archiving - Extracting and decompressing archives
  * zip - Compression files and directories to an archive
    - zip: compress --> bundle
    - tar: bundle --> compress
  * unzip - Extract and decompress zipped archive

```text
tar -cf notes.tar notes
tar -czf note.tar.gz notes

tar -tf notes.tar

tar -xf notes.tar notes
ls -R

zip -r notes.zip notes
unzip notes.zip
```

###  Hands-on Lab: Archiving and Compressing Files
. Duration: 15 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/YJd8h/hands-on-lab-archiving-and-compressing-files)

### Practice Quiz: Practice Quiz: Text Files, Networking & Archiving Commands
. Duration: 6 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/quiz/eZo16/practice-quiz-text-files-networking-archiving-commands)

## Module Summary and Assessment
### Reading: ReadingModule Summary & Highlights
. Duration: 2 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/supplement/zYXGk/module-summary-highlights)
```text
A shell is an interactive user interface. You use shell commands to navigate and work with files and directories.

The `curl` and `wget` commands display and download files from URLs, and the`cat` and `tail`commands display file contents.

You can get user information with the `whoami` and `id`commands, and get operating system information using the `uname` command. You can check system disk usage using the `df` command and monitor processes and resource usage with `ps` and `top`.Print string or variable value using `echo`,print and extract information about the date with the `date` command, and read the manual for any command using `man`.

`ls` lists all files and directories within a specified directory tree and `cd` navigates between directories. The `find` command finds files in your directories.

Relative paths are relative to your current working directory, while absolute paths stand independently

You can create files and directories with the `touch` and `mkdir` commands, delete them with `rm` and `rmdir`, and copy and move them `cp` and `mv`.

The `cat`, `more`, `head`, and `tail` commands allow you to sort and view file contents or view only a certain number of lines. Determine line, word, and character counts with `wc`.

You can use `sort` to view the lines of a file alphanumerically and `uniq` to remove repeated lines from your view. `grep` gets the lines of a file that match your desired criteria, and `cut` extracts slices and fields from lines. You can merge lines from different files using `paste`.

`hostname` and `ifconfig` allow you to view the network configuration. You can test a network connection using `ping` and send and receive data using `curl` and `wget`.

Compression preserves storage space, speeds data transfer, and reduces system load.

`zip` compresses files and folders prior to archiving them. `tar` archives and compresses files and directories into a tarball. `unzip` unpacks and decompresses a zipped archive, and `tar` can also decompress and unpack a tar.gz archive.
```

### Cheat Sheet: Introduction to Linux Commands
. Duration: 10 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/W5gX4/cheat-sheet-introduction-to-linux-commands)

### Upgrade to unlock
Quiz: Graded Quiz: Linux Commands
. Duration: 30 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/exam/Dl739/graded-quiz-linux-commands)

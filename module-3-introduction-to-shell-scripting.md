## Introduction to Shell Scripting


### Video: Shell Scripting Basics 
. Duration: 4 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/9xMbm/shell-scripting-basics)
* What is a script?: interpreted not compiled
  - List of commands that can be interpreted
  - Commands can be entered interactively
  - Scripting languages are interpreted at runtime
  - Slower to run but faster to develop

* What is a script used for:
  - Widely used to automate processes
  - Automates:
    - ETL jobs
    - File backup and archiving
    - System adminstration tasks
  - Nearly computational task

* Shell scripts and the 'shebang'
  * Shell scripts - executable text file with an interpreter directive
    ```text
    #!interpreter [optiontal-arg]
    ```
    - 'interpreter' - path to an executable program
    - 'optional-arg' - single argument string
    ```text
    #! /bin/sh
    #! /bin/bash
    #! /usr/bin/env python3
    ```
    ```bash
    ls -l hello_world.sh
    chmod +x hello_world.sh
    ls -l hello_world.sh
    ```

### Ungraded Plugin: Reading: A Brief Introduction to Shell Variables 
. Duration: 3 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/VxCx5/reading-a-brief-introduction-to-shell-variables)


### Ungraded App Item: Ungraded App ItemHands-on Lab: Getting Started with Shell Scripting
. Duration: 30 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/Fguee/hands-on-lab-getting-started-with-shell-scripting)

### Video: Filters, Pipes, and Variables 
. Duration: 3 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/Pj79L/filters-pipes-and-variables)
* Pipes and filters: Filters are shell commands
  - Take input from standard input
  - Send output to standard output
  - Transform input data into output data
  - Examples: wc, cat, more, head, sort, grep
  - Filters can be chained together
  ```text
  | - pipe command
  For chaining filter commands
  command1 | command2

  Output of command 1 is input of command 2

  ls | sort
  ls | sort -r
  ```
* Shell variables
  - Scope limited to shell
    - set - list all shell variables
    - unset to clear variables
  - Extended scope
    - export var_name
    - env - list all environment variables

### Ungraded Plugin: Reading: Examples of Pipes . Duration: 5 min

### Video: Useful Features of the Bash Shell . Duration: 5 min

### Ungraded Plugin: Reading: Examples of Bash Shell Features . Duration: 5 min

### Ungraded Plugin: Reading: Introduction to Advanced Bash Scripting . Duration: 5 min

### Ungraded App Item: Ungraded App ItemHands-on-Lab: Advanced Bash Scripting . Duration: 30 min

### Video: Scheduling Jobs using Cron . Duration: 4 min

### Ungraded App Item: Ungraded App ItemHands-on Lab: Scheduling Jobs using Crontab . Duration: 20 min

### Ungraded Plugin: Cheat Sheet: Introduction to Shell Scripting . Duration: 15 min

### Reading: ReadingSummary & Highlights . Duration: 2 min

### Practice Quiz: Practice Quiz: Shell Scripting . Duration: 15 min

### Upgrade to unlock Quiz: Graded Quiz: Shell Scripting

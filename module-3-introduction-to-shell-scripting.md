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

### Ungraded Plugin: Reading: Examples of Pipes 
. Duration: 5 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/RaPeL/reading-examples-of-pipes)
```text
$ curl -s --location --request GET https://api.coinstats.app/public/v1/coins/bitcoin\?currency\=USD |\
    grep -oE "\"price\":\s*[0-9]*?\.[0-9]*" |\
    grep -oE "[0-9]*?\.[0-9]*"

-o tells grep to only return the matching portion
-E tells grep to be able to use extended regex symbols such as ?
\"price\" matches the string "price"
\s* matches any number (including 0) of whitespace (\s) characters
: matches :
[0-9]* matches any number of digits (from 0 to 9)
?\. optionally matches a .
```

### Video: Useful Features of the Bash Shell 
. Duration: 5 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/pLqoL/useful-features-of-the-bash-shell)
* Metacharacters
  ```text
  # - precedes a command
  ; - command separator
  * - filename expansion wildcard
  ? - single character wildcard in filename expansion
  ```
* Quoting
  ```text
  \ - escape unique character interpretation
  " " - interpret literally, but evaluate metacharacters
  ' ' - interpret literally
  ```
* I/O redirection
  - Input/Output, or I/O redirection, refers to a set of features used for redirecting
  ```text
  >    - Redirect output to the file
  >>   - Append output to the file
  2>   - Redirect standard error to the file
  2>>  - Append standard error to the file
  <    - Redirect file contents to standard input
  ```
* Command substitution
  - Replace the command with its output: $(command) or `command`
  - Store output of pwd command in here:
    ```bash
    here=$(pwd)
    echo $here
    ```
* Command line arguments
  * Program arguments specified on the command line
  * A way to pass arguments to a shell script
  * Usage:
    ```text
    ./MyBashScript.sh arg1 arg2
    ```
* Batch versus concurrent modes
  * Batch mode: commands run sequentially
    ```text
    command1; command2
    ```
  * Concurrent mode: commands run in parallel
    ```text
    command1 & command2
    ```

### Ungraded Plugin: Reading: Examples of Bash Shell Features 
. Duration: 5 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/f5hVj/reading-examples-of-bash-shell-features)

### Ungraded Plugin: Reading: Introduction to Advanced Bash Scripting 
. Duration: 5 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/QfnFG/reading-introduction-to-advanced-bash-scripting)

```bash
#!/usr/bin/env bash
# initialize array, count, and sum
my_array=(1 2 3)
count=0
sum=0
for i in ${!my_array[@]}; do
  # print the ith array element
  echo ${my_array[$i]}
  # increment the count by one
  count=$(($count+1))
  # add the current value of the array to the sum
  sum=$(($sum+${my_array[$i]}))
done
echo $count
echo $sum
```

### Ungraded App Item: Ungraded App ItemHands-on-Lab: Advanced Bash Scripting 
. Duration: 30 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/XSKJv/hands-on-lab-advanced-bash-scripting)
```text
Tip: It is worth noting that had we been only interested in efficiency, one of the steps could have been avoided. Specifically, you could have redirected your calculations to a text file line-by-line rather than storing them in an array and then writing the array to file.
```

```bash
# 1.1
echo '#!/bin/bash' > script.sh
chmod u+x script.sh


# 3.1
csv_file=https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/M3/L2/arrays_table.csv
wget $csv_file

# 3.2
cat arrays_table.csv

# 3.3
csv_file=arrays_table.csv
column_0=($(cut -d "," -f 1 $csv_file))
column_1=($(cut -d "," -f 2 $csv_file))
column_2=($(cut -d "," -f 3 $csv_file))

nlines=($(cat $csv_file | wc -l))
column_3="./column_3.csv"
echo "column_3" > $column_3
for ((i=1; i<$nlines; i++)); do
  echo $((column_2[$i] - column_1[$i])) >> $column_3
done

# 3.4
paste -d "," $csv_file $column_3 > report.csv
```

### Video: Scheduling Jobs using Cron 
. Duration: 4 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/lecture/Xso6o/scheduling-jobs-using-cron)
* Job scheduling
  * Schedule jobs to run automatically at certain times
* What is a Cron, Crond, and Crontab?
  * Cron is a service that runs jobs
  * Crond interprets 'crontab files'
  * Crontab contains jobs and schedule data
  * Crontab enables to edit a Crontab file
* Scheduling Cron jobs with Crontab
  ```text
  # opens editor
  crontab -e

  # Job syntax:
  # m h dom mon dow command
  # min hour dayofmonth month dayofweek command

  # Example job:
  30 15 * * 0 date >> sundays.txt
  # At 🕥 every Sunday, append date into sundays.txt file
  ```
* Viewing and removing Cron jobs
  ```text
  crontab -e # add/remove cron job with editor
  ```
  ![image](https://github.com/dtlam2601/bash-shell/assets/12412633/8d169cb3-d1cc-4adf-99b8-73e9e35260e1)


### Ungraded App Item: Ungraded App ItemHands-on Lab: Scheduling Jobs using Crontab 
. Duration: 20 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedLti/uIWez/hands-on-lab-scheduling-jobs-using-crontab)
```text
* List cron jobs using crontab -l
* Add cron jobs using crontab -e
* Remove your current crontab using crontab -r
```

### Ungraded Plugin: Cheat Sheet: Introduction to Shell Scripting 
. Duration: 15 min - [Link](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/ungradedWidget/Fh2xm/cheat-sheet-introduction-to-shell-scripting)


### Reading: ReadingSummary & Highlights . Duration: 2 min

### Practice Quiz: Practice Quiz: Shell Scripting . Duration: 15 min

### Upgrade to unlock Quiz: Graded Quiz: Shell Scripting

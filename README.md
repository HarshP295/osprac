# osprac
Exp 1 Unix General Purpose Utility Commands
Case Study 1: System Monitoring and User Interaction in a Shared Development Environment
Scenario:
A team of developers shares a Linux server for code deployment and debugging. Each developer uses the terminal for various tasks including checking system status, writing scripts, and managing files.
Command Usage Scenarios:
Command
Use Case / Scenario
echo
Used in shell scripts or to display output, e.g., echo "Build started at $(date)".
clear
Clears the cluttered terminal screen during debugging or long sessions.
exit
Used to log out from the terminal or end a shell script execution.
date
Displays current system date/time—useful for logging or confirming system time.
time
Measures how long a command or script takes to execute, e.g., time ./build.sh.
uptime
Checks how long the server has been running—useful for troubleshooting crashes.
cal
Checks the calendar, useful when scheduling scripts or meetings via terminal.
cat
Displays contents of configuration or log files quickly.
Tty
(teletype)
Tells which terminal you're connected to, helpful in debugging user sessions.
man
Accesses the manual page for a command, e.g., man grep to see syntax and options.
which
Finds the location of installed utilities, e.g., which python shows Python binary path.
history
Views recently executed commands for repeating or debugging past commands.
id
Displays user ID, group ID, useful in permission troubleshooting.
pwd
Displays the present working directory; helps users verify their path.
whoami
Confirms logged-in user identity—especially important with multiple users.

Case Study 2: System Administration - Networking, Printing & Mail Server Maintenance
Scenario:
A system admin in a university lab environment is responsible for maintaining Linux machines used by students for assignments, printing reports, and sending lab notifications via email.
Command Usage Scenarios:
Command
Use Case / Scenario
ping
Checks network connectivity to an external server (e.g., ping google.com).
ifconfig
Views or configures network interfaces, especially during WiFi/Ethernet issues.
pr
Prepares formatted output for printing (e.g., pr report.txt).
lp / lpr
Sends files to the printer (e.g., lp project_summary.pdf).
lpstat
Checks the status of current print jobs and printer queues.
lpq
Displays the print queue in more detail.
lprm
Removes a specific print job from the queue.
cancel
Cancels a printing job entirely (e.g., cancel 42).
mail
Sends system-generated emails to users (e.g., notifying students of system maintenance).


Exp 2 
Execution of File System Management Commands like ls, cd, pwd, cat, mkdir, rmdir, rm, cp, mv, chmod, wc, piping and redirection, grep, tr, echo, sort, head, tail, diff,comm, less, more, file, type, wc, split, cmp, tar, find, vim, gzip, bzip2, unzip, locate,etc.

Case Study 2: File Management in a Software Development Team

Scenario:

A software development team is working on a Unix-based system to manage project files efficiently.

Implementation Steps:

1. Creating a Project Directory and Files:

mkdir ProjectX → Creates a new directory for the project.

cd ProjectX → Navigates to the project directory.

touch main.py README.md → Creates a Python file and a README.

2. Checking and Managing Files:

ls -l → Lists files with details.

cat README.md → Displays README contents.

nano README.md → Edits the README file.



3. Copying and Moving Files:

cp main.py backup.py → Creates a backup of the script.

mv backup.py old_version.py → Renames the backup file.



4. Archiving and Deleting Files:
tar -cvf archive.tar file3.txt.

rm old_version.py → Deletes the old backup file.

rm -r ProjectX → Deletes the entire project directory if needed.
(rmdir only deletes an empty directory )

5. Checking File Content:

head main.py → Displays the first 10 lines of the script.

tail -n 5 main.py → Shows the last 5 lines.


Explanation of all commands:
ls - Lists directory contents.
Example: ls -l (lists files in long format).
Output: Shows permissions, owner, size, and modification time (e.g., -rw-r--r-- 1 user user 1234 Apr 27 12:00 file.txt).
cd - Changes the current directory.
Example: cd /var/cache/apt/archives/.
Output: No output; changes directory (use pwd to confirm).
pwd - Prints the current working directory.
Example: pwd.
Output: e.g., /home/user.
cat - Concatenates and displays file content.
Example: cat file3.txt (from your earlier input).
Output: e.g., My Name is Khushi (if file3.txt contains that text).
mkdir - Creates a new directory.
Example: mkdir newdir.
Output: No output; creates newdir (use ls to verify).
rmdir - Removes an empty directory.
Example: rmdir newdir.
Output: No output; removes newdir (if empty).
rm - Removes files or directories.
Example: rm file3.txt.
Output: No output; deletes file3.txt (use ls to confirm).
cp - Copies files or directories.
Example: cp file3.txt backup.txt.
Output: No output; creates backup.txt as a copy.
mv - Moves or renames files/directories.
Example: mv backup.txt newdir/.
Output: No output; moves backup.txt to newdir.
chmod - Changes file permissions.
Example: chmod 644 file3.txt.
Output: No output; sets read/write for owner, read-only for others.
wc - Word, line, and character count.
Example: wc file3.txt.
Output: e.g., 1 4 15 file3.txt (1 line, 4 words, 15 chars).
Piping (| - Redirects output of one command to another.
Example: ls -l | grep txt.
Output: Lists only lines with "txt" (e.g., file3.txt details).
Redirection (> or >>) - Redirects output to a file.
Example: echo "Test" > test.txt.
Output: Creates/overwrites test.txt with "Test".
grep - Searches text using patterns.
Example: grep "Khushi" file3.txt.
Output: e.g., My Name is Khushi (if found).
tr - Translates or deletes characters.
Example: echo "Hello" | tr '[:lower:]' '[:upper:]'.
Output: HELLO.
echo - Displays text or variables.
Example: echo $HOME.
Output: e.g., /home/user.
sort - Sorts lines of text.
Example: sort file3.txt.
Output: Sorts content (e.g., My Name is Khushi remains single line unless multiple).
head - Displays the first few lines of a file.
Example: head -n 1 file3.txt.
Output: e.g., My Name is Khushi (first line).
tail - Displays the last few lines of a file.
Example: tail -n 1 file3.txt.
Output: e.g., My Name is Khushi (last line).
diff - Compares files line by line.
Example: diff file3.txt backup.txt.
Output: No output if identical; otherwise, shows differences.
comm - Compares sorted files line by line.
Example: comm file1.txt file2.txt (requires sorted files).
Output: e.g., lines unique to each file and common lines.
less - Views file content page by page.
Example: less file3.txt.
Output: Interactive view (press q to quit).
more - Similar to less, views file content.
Example: more file3.txt.
Output: Similar to less (space to scroll, q to quit).
file - Determines file type.
Example: file file3.txt.
Output: e.g., file3.txt: ASCII text.
type - Displays the type of command.
Example: type ls.
Output: e.g., ls is aliased to ls --color=auto'`.
split - Splits a file into pieces.
Example: split -l 1 file3.txt.
Output: Creates xaa, xab, etc. (use ls to verify).
cmp - Compares two files byte by byte.
Example: cmp file3.txt backup.txt.
Output: No output if identical; otherwise, shows first difference.
tar - Archives files.
Example: tar -cvf archive.tar file3.txt.
Output: e.g., file3.txt.
find - Searches for files in a directory hierarchy.
Example: find . -name "*.txt".
Output: e.g., ./file3.txt.
vim - Text editor.
Example: vim file3.txt.
Output: Opens file3.txt for editing (press i to insert, :wq to save and quit).
gzip - Compresses files.
Example: gzip file3.txt.
Output: Creates file3.txt.gz (original deleted).
bzip2 - Compresses files (higher compression than gzip).
Example: bzip2 file3.txt.
Output: Creates file3.txt.bz2.
unzip - Decompresses zip files.
Example: unzip file.zip (if a zip file exists).
Output: Extracts contents (use ls to verify).
locate - Finds files by name (uses prebuilt database).
Example: locate file3.txt.
Output: e.g., /home/user/file3.txt.




Exp 3 Execution of User Management Commands like who, whoami, su, sudo, login, logout, exit, passwd, useradd/adduser, usermod, userdel, groupadd, groupmod, groupdel, gpasswd, chown, chage, chgrp, chfn, etc.

Case Study 1: User Management in a Multi-User Unix System

Scenario:

A university has a shared Linux server for students and faculty to access programming resources. The system administrator needs to create user accounts, manage permissions, and ensure security.

Implementation Steps:(use sudo when necessary)

1. Creating Student and Faculty Accounts:

useradd student1 → Creates a student account.

useradd faculty1 → Creates a faculty account.

passwd student1 → Sets a password for student1.



2. Assigning Users to Groups:

groupadd students → Creates a group for students.

groupadd faculty → Creates a group for faculty.

usermod -aG students student1 → Adds student1 to the "students" group.

usermod -aG faculty faculty1 → Adds faculty1 to the "faculty" group.



3. Checking Logged-In Users:

who → Displays active users.

id student1 → Shows the UID and GID of student1.



4. Deleting a User Who Graduated:

userdel -r student1 → Removes student1 and their home directory.



5. Checking Password Expiration Policy:

chage -l faculty1 → Checks password expiry for faculty1.


Explanation of commands:
who - Displays currently logged-in users.
Example: who
Output: e.g., ubuntu tty1 2025-04-27 12:00 (shows username, terminal, login time).
whoami - Displays the current user's username.
Example: whoami
Output: e.g., ubuntu (based on your prompt ubuntu@ubuntu).
su - Switches to another user (or root by default).
Example: su - newuser
Output: Prompts for newuser’s password, then switches to their shell (e.g., newuser@Ubuntu:/root$).
sudo - Executes a command with superuser privileges.
Example: sudo touch /root/testfile
Output: No output if successful; creates testfile in /root (prompts for password if not recently authenticated).
login - Initiates a new login session.
Example: login
Output: Prompts for username and password, then logs in (e.g., Ubuntu login: newuser).
logout - Ends the current login session (works in some shells).
Example: logout
Output: Exits the session (returns to login prompt or parent shell).
exit - Exits the current shell or session.
Example: exit
Output: Closes the terminal or returns to the parent shell.
passwd - Changes a user’s password.
Example: passwd
Output: Prompts for current password, then new password (e.g., New password:).
useradd/adduser - Adds a new user (adduser is more user-friendly).
Example: sudo useradd -m -s /bin/bash newuser (or sudo adduser newuser)
Output: useradd creates the user silently; adduser prompts for password and details (e.g., Enter new UNIX password:).
usermod - Modifies a user’s account.
Example: sudo usermod -aG sudo newuser
Output: No output; adds newuser to the sudo group.
userdel - Deletes a user account.
Example: sudo userdel -r newuser
Output: No output; removes newuser and their home directory (-r).
groupadd - Creates a new group.
Example: sudo groupadd devgroup
Output: No output; creates devgroup.
groupmod - Modifies a group.
Example: sudo groupmod -n developers devgroup
Output: No output; renames devgroup to developers.
groupdel - Deletes a group.
Example: sudo groupdel developers
Output: No output; removes developers.
gpasswd - Manages group passwords and membership.
Example: sudo gpasswd -a newuser developers
Output: No output; adds newuser to developers.
chown - Changes file ownership.
Example: sudo chown newuser file3.txt
Output: No output; changes file3.txt owner to newuser.
chage - Changes user password expiry information.
Example: sudo chage -M 30 newuser
Output: No output; sets newuser’s password to expire in 30 days.
chgrp - Changes file group ownership.
Example: sudo chgrp developers file3.txt
Output: No output; changes file3.txt group to developers.
chfn - Changes user information (e.g., full name).
Example: chfn newuser
Output: Prompts for details (e.g., Full Name []: New User).


Exp 4 Execution of Process Management Commands like ps, pstree, nice, kill, pkill, killall, xkill, fg, bg, pgrep, renice, etc.

Scenario-Based Usage of Process Management Commands
Command
Scenario
Usage
ps
You want to see all currently running processes for your user.
ps aux or ps -ef
pstree
You want to view the parent-child relationship of processes.
pstree
nice
You want to start a process with lower priority so it doesn't consume much CPU.
nice -n 10 myscript.sh
renice
You want to change the priority of an already running process.
renice -n 5 -p <PID>
kill
You want to terminate a process using its PID.
kill 1234
pkill
You want to kill a process by its name (not PID).
pkill firefox
killall
You want to kill all instances of a process.
killall chrome
xkill
A graphical app is frozen and you want to forcefully kill it by clicking on its window.
xkill (then click on the window)
fg
A process running in background needs to be brought to foreground.
fg %1
bg
A stopped process needs to be resumed in the background.
bg %1
pgrep
You want to find PID of a running process by name.
pgrep python


Case Study: Managing Application Performance in a Linux Server
Problem:
A software development company is running multiple apps (e.g., Python scripts, MySQL server, Firefox for testing) on a Linux server. Some scripts consume a lot of CPU, causing the system to slow down. The team needs to monitor and manage these processes efficiently.
Objectives:
Identify high-CPU usage processes


Reduce the CPU priority of some tasks


Kill non-responsive processes


Manage background/foreground jobs


Solution Using Process Management Command
Step 1: Monitor Active Processes
ps aux --sort=-%cpu

Lists all processes sorted by CPU usage.
Step 2: View Process Hierarchy
pstree -p

Visualizes how child processes are linked to parent processes.
Step 3: Run Heavy Script with Lower Priority
nice -n 10 python3 heavy_script.py

Prevents script from hogging CPU.
Step 4: Find the PID of a Resource-Hungry Process
pgrep -f heavy_script.py
Returns the PID of the script if you didn’t store it initially.
Step 5: Change the Priority of a Running Process
renice -n 15 -p 4567

Reduces priority of PID 4567, giving more CPU to others.
Step 6: Kill a Hung Firefox Browser
pkill firefox
Closes all Firefox processes.
OR
xkill

Click on a frozen window to forcefully close it.
Step 7: Background and Foreground Process Handling
./long_task.sh &
jobs       # View job list
fg %1      # Bring job 1 to foreground
bg %1      # Send job 1 to background again
Conclusion:
This case study shows how a Linux admin can use process management commands to:
Optimize system performance,


Reduce CPU load from non-critical tasks,


Handle frozen or unresponsive applications,


Maintain server health in a multi-user environment.

Exp 5 Execution of Memory Management Commands like free, /proc/meminfo, top, htop,df, du, vmstat, demidecode, sar, pagesize, etc.

Case Study: Diagnosing Memory Bottlenecks on a Production Server
Background:
A company runs a web server that has been responding slowly. The system administrator is assigned the task of diagnosing whether it's a memory issue or a disk usage problem.
SCENARIOS & COMMANDS USED
1. Monitor Available RAM in Real-Time
Scenario: You want to check whether your server is running out of memory.
Command:

free -h
Use: Displays free, used, and total memory (RAM and swap) in a human-readable format.


Solution: If free shows low "available" RAM and high swap usage, it indicates memory pressure.
2. Check Detailed Memory Information
Scenario: You need exact stats on memory breakdown.
Command:
cat /proc/meminfo
Use: Dumps detailed memory stats directly from the kernel.


Solution: Check MemAvailable, Buffers, Cached to understand actual memory usage.
3. Real-Time Process Monitoring
Scenario: Find out which processes consume the most memory.
Command:
top
Use: Lists running processes sorted by CPU/memory usage.


Solution: Identify memory-hogging processes (look under %MEM column).


Alternative Command:
htop
Use: Colorful, interactive version of top.


Note: May need to install it using sudo apt install htop.


4. Check Disk Space Usage
Scenario: Check if the system is running out of disk space, impacting swap and memory.
Command:
df -h
Use: Displays disk space usage for all mounted partitions.


Solution: Identify if / or /home is nearly full.


5. Check Directory Size to Clear Space
Scenario: You need to identify which directories are taking up space.
Command:
du -sh /var/*
Use: Displays size of folders under /var.


Solution: Delete large unnecessary logs from /var/log.


6. View Memory Statistics in Real-Time
Scenario: Need to observe memory usage pattern over time.
Command:
vmstat 5
Use: Displays memory, CPU, and I/O usage every 5 seconds.


Solution: Helps identify spikes in memory demand or swap usage.


7. Check Hardware Details
Scenario: Want to verify total physical RAM and memory slots.
Command:
sudo dmidecode -t memory
Use: Provides hardware-level details of memory modules.


Solution: Used to plan memory upgrades.


8. Check Page Size
Scenario: Need to know the system's memory page size (used in memory tuning).
Command:
getconf PAGE_SIZE
Output: Shows memory page size (e.g., 4096 bytes).


Use: Useful in understanding paging behavior.


9. Historical Resource Usage Report
Scenario: Need to analyze memory usage over the last few hours/days.
Command:
sar -r 1 5
Use: Reports memory usage (free, used, cache, buffer) at 1-second intervals, 5 times.


Note: You might need to install sysstat package.


Summary of the Case Study Execution
Problem Observed:
Web server slow and unresponsive.


Commands Used:
free -h, top, and vmstat revealed high memory usage.


cat /proc/meminfo confirmed low available memory and swap usage.


df -h showed root partition 90% full.


du -sh /var/* identified large logs in /var/log.


htop showed specific service using excessive RAM.


dmidecode checked if more RAM could be added.


Solution Taken:
Cleared unused logs.


Restarted memory-intensive service.


Scheduled system upgrade to add more RAM.
Conclusion:
These commands together provide a comprehensive diagnostic toolkit for identifying, analyzing, and resolving memory-related issues on Unix/Linux systems.














SHELL SCRIPTING
nano filename.sh
chmod +x filename.sh
./filename.sh
● Write a shell script to perform arithmetic operations.
echo "Enter the two numbers: "
read a b

SUM=$((a+b));
DIFF=$((a-b));
MUL=$((a*b));
DIV=$((a/b));

echo "Addition is: $SUM";
echo "Difference is: $DIFF";
echo "Multiplication is: $MUL";
echo "Division is: $DIV";


● Write a shell script to calculate simple interest and Compound Interest
calculation.
echo "Enter the principal amount , rate and time respectively: "
read p r t

si=$((p*r*t/100));
ci=$(echo "scale=2; $p * ((1 + $r / 100)^$t) - $p" | bc -l);

echo "Simple interest is: $si";
echo "Compound interest is: $ci";



● Write a shell script to determine largest among three integer numbers.
echo "Enter the three numbers";
read a b c
if [ $a -ge $b ] && [ $a -ge $c ]; then
echo "$a is the greatest number"

elif [ $b -ge $a ] && [ $b -ge $c ]; then
echo "$b is the greatest number"

else
echo "$c is the greatest number"
fi

● Write a shell script to determine if a given year is a leap year or not.
#!/bin/bash
echo "Enter the year"
read y

if (( ( $y % 400 == 0 ) || ( $y % 4 ==0 && $y % 100 != 0) )); then
echo "The given year $y is a leap year"

else
echo "The given year is not a leap year"
fi

● Write a shell script to determine Fahrenheit to Centigrade Conversion
#!/bin/bash

echo "Enter the temperture in Farenheit "
read t

ct=$(echo "scale=2; (( $t - 32 ) * ( 5.0 / 9.0 ))" | bc );

echo "The temperature in centrigrade is $ct "

● Write a shell script to determine Area & Circumference of Circle
#!/bin/bash
echo "Enter the radius: "
read r

a=$(echo "scale=2; ( 3.14 * $r * $r )" | bc)
c=$(echo "scale=2; (2 * 3.14 * $r )" | bc)

echo "The area of the circle is: $a"
echo "The circumference of the circle is: $c"



● Write a shell script to search whether an element is present in the list or not.
#!/bin/bash

echo "Enter the list of elements"
read -a arr

echo "Enter the element to be searched"
read key

found=0

for i in "${arr[@]}"; do
    if [ "$i" = "$key" ]; then
        found=1
        break
    fi
done

if [ $found -eq 1 ]; then
    echo "$key is present in the list"
else
    echo "$key is not present in the list"
fi

● Write a shell script to compare two strings.
#!/bin/bash
echo "Enter the two strings"
read str1 str2

if [ "$str1" == "$str2" ];then
echo "The two strings are equal"
else
echo "The two strings are not equal"
fi

● Write a shell script for Employee Pay calculation
#!/bin/bash
echo "Enter the basic salary: "
read basic

da=$(( $basic * 10 / 100 ));
hra=$(( $basic * 20 / 100 ));

total_sal=$(( $basic + $da + $hra ));

echo "The gross salary is: $total_sal "


● Write a Shell script to calculate Grade.
#!/bin/bash

echo "Enter the marks (0-100): "
read m

if [ $m -ge 80 ]; then
    echo "The grade is A"
elif [ $m -ge 60 ] && [ $m -le 79 ]; then
    echo "The grade is B"
elif [ $m -ge 30 ] && [ $m -le 59 ]; then
    echo "The grade is C"
else
    echo "Fail"
fi

● Write a shell script to implement a menu-driven calculator using a case
statement.
#!/bin/bash
echo "Enter two numbers:"
read a b

echo "1. Add 2. Subtract 3. Multiply 4. Divide"
read choice

case $choice in
  1) echo "Result = $((a + b))" ;;
  2) echo "Result = $((a - b))" ;;
  3) echo "Result = $((a * b))" ;;
  4) echo "Result = $((a / b))" ;;
  *) echo "Invalid choice" ;;
esac


● Write a shell script to perform operations on directory like: display name of
current directory; display list of directory contents; create another directory,
write contents on that and copy it to a suitable location in your home directory;
etc
#!/bin/bash
echo "The present working directory is: $pwd "
echo "The contents are given as: "
ls
echo "Creating new directory (demo_dir)..."
mkdir demo1_dir
echo "This is a test file." >demo1_dir/test.txt

sudo cp -r demo_dir /demo_copy
echo "Directory copied to home directory as demo_copy"



● Write a Shell script for a Menu Driven program to check if entered number is
   1.Even or Odd 2.Prime 3.Palindrome 4.Armstrong
#!/bin/bash

while true; do
    echo "Enter a number:"
    read n

    echo "Choose an operation:"
    echo "1. Even or Odd"
    echo "2. Prime/Not Prime"
    echo "3. Palindrome"
    echo "4. Armstrong"
    echo "5. Exit"
    read -p "Enter your choice (1-5): " choice

    case $choice in
    1)
        if (( n % 2 == 0 )); then
            echo "Even"
        else
            echo "Odd"
        fi
        ;;
    2)
        if (( n <= 1 )); then
            echo "Not a prime number"
        else
            is_prime=1
            for (( i=2; i*i<=n; i++ )); do
                if (( n % i == 0 )); then
                    is_prime=0
                    break
                fi
            done
            if (( is_prime == 1 )); then
                echo "The given number is a prime number"
            else
                echo "The given number is not a prime number"
            fi
        fi
        ;;
    3)
        rev=0
        num=$n
        original=$n
        while (( num > 0 )); do
            rem=$(( num % 10 ))
            rev=$(( rev * 10 + rem ))
            num=$(( num / 10 ))
        done
        if (( rev == original )); then
            echo "The given number is a palindrome"
        else
            echo "Not a palindrome"
        fi
        ;;
    4)
        sum=0
        num=$n
        original=$n
        while (( num > 0 )); do
            d=$(( num % 10 ))
            sum=$(( sum + d * d * d ))
            num=$(( num / 10 ))
        done
        if (( sum == original )); then
            echo "The number is an Armstrong number"
        else
            echo "Not an Armstrong number"
        fi
        ;;
    5)
        echo "Exiting the program. Goodbye!"
        break
        ;;
    *)
        echo "Invalid Choice. Please select between 1 to 5."
        ;;
    esac

    echo # Adds an empty line for better readability
done


Write a shell script to read and check if the directory / file exists or not, if not
make the directory / file.
#!/bin/bash

echo "Enter the name of the file or directory:"
read name

if [ -e "$name" ]; then
    echo "$name already exists."
else
    echo "$name does not exist."
    echo "What do you want to create?"
    echo "1. File"
    echo "2. Directory"
    read choice

    if [ "$choice" -eq 1 ]; then
        touch "$name"
        echo "File '$name' created."
    elif [ "$choice" -eq 2 ]; then
        mkdir "$name"
        echo "Directory '$name' created."
    else
        echo "Invalid choice."
    fi
fi


Execute the following scripts using grep / sed commands:
● Write a script using grep command to find the number of words character,
words and lines in a file.
#!/bin/bash

echo "Enter the filename:"
read file

if grep -q "" "$file"; then
    echo "File exists."
    echo "Characters: $(wc -m < "$file")"
    echo "Words: $(wc -w < "$file")"
    echo "Lines: $(wc -l < "$file")"
else
    echo "File does not exist."
fi


● Write a script using egrep command to display a list of specific types of files in
the directory.
#!/bin/bash

echo "Listing .txt, .sh, and .pdf files:"
ls | egrep "\.txt$|\.sh$|\.pdf$"

● Write a script using sed command to replace all occurrences of a particular
word in a given file.
#!/bin/bash

echo "Enter the filename:"
read file

echo "Enter the word to be replaced:"
read old_word

echo "Enter the new word:"
read new_word

sed -i "s/$old_word/$new_word/g" "$file"

echo "All occurrences of '$old_word' replaced with '$new_word'."


● Write a script using sed command to print duplicate lines in input.
#!/bin/bash

echo "Enter the filename:"
read file

sort "$file" | uniq -d


Experiment No.9(CPU Scheduling FIFO)
#include <stdio.h>

void findTimes(int processes[], int n, int at[], int bt[], int ct[], int wt[], int tat[]) {
    ct[0] = at[0] + bt[0];
    tat[0] = ct[0] - at[0];
    wt[0] = tat[0] - bt[0];
    
    for (int i = 1; i < n; i++) {
        if (at[i] > ct[i-1]) {
            ct[i] = at[i] + bt[i]; // CPU idle till process arrives
        } else {
            ct[i] = ct[i-1] + bt[i];
        }
        tat[i] = ct[i] - at[i];
        wt[i] = tat[i] - bt[i];
    }
}

void avgTime(int processes[], int n, int at[], int bt[]) {
    int ct[n], wt[n], tat[n];
    int total_wt = 0, total_tat = 0;

    findTimes(processes, n, at, bt, ct, wt, tat);

    printf("\nProcess\tArrival Time\tBurst Time\tCompletion Time\tWaiting Time\tTurn Around Time\n");
    printf("--------------------------------------------------------------------------------------------\n");

    for (int i = 0; i < n; i++) {
        total_wt += wt[i];
        total_tat += tat[i];
        printf("  P%d\t    %d\t\t   %d\t\t    %d\t\t    %d\t\t     %d\n",
               processes[i], at[i], bt[i], ct[i], wt[i], tat[i]);
    }

    printf("\nAverage Waiting Time = %.2f\n", (float)total_wt / n);
    printf("Average Turn Around Time = %.2f\n", (float)total_tat / n);
}

int main() {
    int n;
    printf("Enter the number of processes: ");
    scanf("%d", &n);

    if (n <= 0) {
        printf("Invalid number of processes.\n");
        return 1;
    }

    int processes[n], arrival_time[n], burst_time[n];

    for (int i = 0; i < n; i++) {
        processes[i] = i + 1;
        printf("Enter arrival time for Process %d: ", i + 1);
        scanf("%d", &arrival_time[i]);
        printf("Enter burst time for Process %d: ", i + 1);
        scanf("%d", &burst_time[i]);
    }

    avgTime(processes, n, arrival_time, burst_time);

    return 0;
}

Experiment No.10(Best Fit)
#include <stdio.h>

void bestFit(int blockSize[], int blocks, int processSize[], int processes) {
    int allocation[processes];

    // Step 1: Initialize allocation array to -1 (means not allocated)
    for (int i = 0; i < processes; i++) {
        allocation[i] = -1;
    }

    // Step 2: Pick each process and find the best-fit block
    for (int i = 0; i < processes; i++) {
        int bestIdx = -1; // Best block index

        for (int j = 0; j < blocks; j++) {
            if (blockSize[j] >= processSize[i]) { // Block can fit the process
                if (bestIdx == -1 || blockSize[j] < blockSize[bestIdx]) {
                    bestIdx = j; // Find the block with the least leftover space
                }
            }
        }

        // Step 3: If a suitable block was found
        if (bestIdx != -1) {
            allocation[i] = bestIdx;
            blockSize[bestIdx] -= processSize[i]; // Reduce available memory
        }
    }

    // Step 4: Print the allocation result
    printf("\nProcess No.\tProcess Size\tBlock No.\n");
    for (int i = 0; i < processes; i++) {
        printf("   %d\t\t   %d\t\t", i + 1, processSize[i]);
        if (allocation[i] != -1)
            printf("%d\n", allocation[i] + 1); // Block numbers start from 1
        else
            printf("Not Allocated\n");
    }
}

int main() {
    int blockSize[10], processSize[10];
    int blocks, processes;

    // Step 1: Input memory block details
    printf("Enter number of memory blocks: ");
    scanf("%d", &blocks);

    printf("Enter sizes of %d memory blocks:\n", blocks);
    for (int i = 0; i < blocks; i++) {
        scanf("%d", &blockSize[i]);
    }

    // Step 2: Input process details
    printf("Enter number of processes: ");
    scanf("%d", &processes);

    printf("Enter sizes of %d processes:\n", processes);
    for (int i = 0; i < processes; i++) {
        scanf("%d", &processSize[i]);
    }

    // Step 3: Call bestFit function
    bestFit(blockSize, blocks, processSize, processes);

    return 0;


Experiment No.12(Page Replacement FIFO)
#include <stdio.h>

int main() {
    int pages, frames, page_faults = 0, page_hits = 0;
    int frame[10];
    int i, j, k, flag;

    printf("Enter the number of pages: ");
    scanf("%d", &pages);

    printf("Enter the number of frames: ");
    scanf("%d", &frames);

    int page[pages];
    printf("Enter the reference string: \n");
    for (i = 0; i < pages; i++) {
        scanf("%d", &page[i]);
    }

    // Initialize all frames to -1
    for (i = 0; i < frames; i++) {
        frame[i] = -1;
    }

    printf("\nPage\tFrames\n");

    int front = 0; // FIFO uses 'front' to replace pages

    for (i = 0; i < pages; i++) {
        flag = 0;

        // Check if page is already in frame (page hit)
        for (j = 0; j < frames; j++) {
            if (frame[j] == page[i]) {
                flag = 1;
                page_hits++;
                break;
            }
        }

        if (flag == 0) { // Page Fault
            frame[front] = page[i];
            front = (front + 1) % frames;
            page_faults++;
        }

        printf("%d\t", page[i]);
        for (k = 0; k < frames; k++) {
            if (frame[k] == -1)
                printf("- ");
            else
                printf("%d ", frame[k]);
        }
        printf("\n");
    }

    printf("\nTotal no. of page faults: %d\n", page_faults);
    printf("Total no. of page hits: %d\n", page_hits);

    return 0;
}





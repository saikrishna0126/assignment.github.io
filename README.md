# Table of contents

1. [Day-1](#Day-1)
  - [Linux for DevOps](#Linux-for-DevOps)
2. [Day-2](#Day-2)
  - [Shell Scripting and Automation Basics](#Shell-Scripting-and-Automation-Basic)
3. [Day-3](#Day-3)
  - [Process Management, System Monitoring, and Networking](#process-management-system-monitoring-and-networking)
4. [Day-4](#Day-4)
  - [Introduction to Docker](#introduction-to-docker)
5. [Day-5,6](#Day-5)
  - [Working with Docker Volumes and Docker Networks](#working-with-docker-volumes-and-docker-networks)
6. [Day-7](#Day-7)
  - [Introduction to Docker Compose](#introduction-to-docker-compose)
7. [Day-8](#Day-8)
  - [Introduction to Terraform](#introduction-to-terrafform)
8. [Day-9,10](#Day-9,10)
  - [Create Resources with Terraform](#create-resources-with-terraform)
9. [Day-11,12](#Day-11,12)
  - [Terraform Modules](#terrafor-modules)
10. [Day-13,](#Day-13)
  - [Introduction to Ansible](#introduction-to-ansible)
11. [Day-14](#Day-14)
  - [Ansible Configuration and Inventory management](#ansible-configuration-and-inventory-management)
12. [Day-15](#Day-15)
  - [Writing Your First Ansible Playbook](#writing-your-first-ansible-playbook)
13. [Day-16](#Day-16)
  - [Working with Variables and Templates](#working-with-variables-and-templates)
14. [Day-17](#Day-17)
  - [Advanced Playbook Features](#advanced-playbook-features)
15. [Day-18](#Day-18)
  - [Ansible Vault and Best Practices](#ansible-vault-and-best-practices)
--------------------------------------------------------------------------------------------------------


## **Day 1** <a name="Day-1"></a>
## <center>LINUX FOR DEVOPS</center> <a name="LINUX FOR DEVOPS"></a>

--------------------------------------------------------------------------------------------
##### What is Operating System?
A operating system is system software that manages computer hardware and software resources and provides common services for computer programs. Operating system is a bridge between hardware of the computer and the users.</font>

###### What is Linux?
Linux is an open source operating system that is made up of the kernal, the base component o the OS and the tools, apps, and the services bundled along with it.<br>
- Linux is free and do not have to worry about paying anthing at all.
- Allowing you to make changes to its code and adding new functionality to be used by other users.
- It is one of the best secure and stable OS, and it is very low chance of getting attacked by any hackers or virus
- Linux does not require much memory and space effectively working. It  is very low system requirements.
- We can run along with linux and windows in one system and within windows using virtual machines.</font><br>
##### Why choose Linux?
- Linux is widely used for troubleshooting purpose for other computer.
- We want to build or host a website.
- It is one of the secure and robust operating system and most stable one.</font>

##### Linux for DevOps

Linux is important for DevOps because it provides an environment needed to manage infrastructure, automate tasks and troubleshoot issues. Linux is backbone of the devops.
- A core goal of DevOps is fast software delivery and building on existing infrastructure, linux is big part of that.
- Linux and any other OS is an essential component of any IT operation, to know how to configure Linux for DevOps is essential to a continual and speedy software delivery process.
- It enables the creation of design and security applications to a specific development environment or set of development objectives. Compared to Windows, there is a lot more control over how the operating system operates.
- Most of the DevOps tools are Linux based tools and supports linux. DevOps engineer may easily and internally do all testing using a Linux-based operating system
- Scalability enables fast delivery without forcing developers to compromise the quality of their codebase.</font>

###### **Linux Architecture**

![alt text](image-3.png)
 
- **Hardware**: It consists of all peripheral devices such as RAM, CPU, HDD etc... 
- **Kernal**: It is the central component of an operating system. It means harware resuorces, system calls and provide essential services to applications.
- **Shell**: Shell takes commands from the users and execute kernal functions. It is a commandline-interpreter that lets linux users control their operating systems with CLI (commandline interface).
- **Utilities**: Provides a set of functions and routines that application use to  interact   with the kernal and perform various tasks.</font>

##### Linux Filesystem Hierarchy Structure
![alt text](image-11.png)


  **`bin:`** it stores all the binary files and also it stores the commands that had been executed by the user.
  **`sbin:`** it stores the commands that had been executed by the super user.
  **`boot:`** it contains boot images & boot files.
  **`dev:`** it contains all the device files
  **`etc:`** it contains all the host specific system configuration files.
  **`lib:`** it contains all the library files of the system.
  **`lib64:`** it contains all the library files of the system of 64 bit.
  **`mnt:`** it is used for the mounting purpose.
  **`opt:`** it stores all the file details of the 3 rd party when it installed.
  **`proc:`** it is used to see all the processing related files (Hardware details).
  **`srv:`** it stores all the service related information provided by system.
  **`sys:`** it stores any new changes that obtained while changing Hardware.
  **`tmp:`** it stores temperory files and have access to all.
  **`usr:`** it contains local system files which are continuing with the old system architecture.
  **`var:`** it stores all the system services. 

###### **Basic Linux Commands**



- `ls :` This command is used to list the contents of the directory
- `cd :` This command used to change the directories
- `pwd :` This command will show present working directory
- `cp :` This command is used to copy the files
- `mv :` This command is used to rename the files and directiries and move files or directories one directory to another 
- `rm :` This command is used to remove file or directories 
- `mkdir :` This command is used to create directories </font>

###### **Linux File Permissions**



- `File Access Modes :-` The permissions of a file are the first line of defense in the security of a Unix system. The basic building blocks of Unix permissions are the read,write, and execute permissions, which have been explained below 
- `Read :-` Grants the capability to read, i.e., view the contents of the file.
- `Write :-` Grants the capability to modify, or remove the content of the file.
- `Execute :-` User with execute permissions can run a file as a program.
- `Directory Access Modes :-` Directory access modes are listed and organized in the same manner as any other file. There are a few differences that need to be mentione
- `Read :-` Access to a directory means that the user can read the contents. The user can look at the filenames inside the directory.
- `Write :-` Access means that the user can add or delete files from the directory.
- `Execute :-` Executing a directory doesn't really make sense, so think of this as a traverse permission.
![alt text](image-9.png)

| **NUMBER** | **PERMISSION REPRESENTATION**  |    **REFERENCE**     |  
|------------|--------------------------------|----------------------|
|     0      |     No permission              |        --            |
|     1      |     Execution permission       |        --x           |
|     2      |     Write permission           |        -w-           |
|     3      |  Execute & Write permission    |        -wx           |
|     4      |      Read permission           |        r--           |
|     5      |  Read & Execute permission     |        r-x           |
|     6      |  Read & Execute permission     |        rw-           |
|     7      |Read, Write & Execute permission|        rwx           |

###### **Changing File permissions and Ownership and groups**
Each file and directory in Linux has three types of permissions (read, write, execute) for three types of users (owner, group, others).
- **Changing Ownership:**
-  To change the owner and group of a file or directory:
  ```bash
  $ sudo chown saikrishna:voziq task.txt
  ```
  ```
  chmod +rwx filename: Adds permissions
  chmod -rwx directoryname: Removes permissions
  chmod +x filename: Allows executable permissions
  chmod -wx filename: Takes out write and executable permissions
  chmod +rwx filename: Allows Read and write execute permissions
  chmod g+w filename: Changes directory permissions for group owners 
  ```

##### **User and Group management**


In Linux, user and group management is essential for controlling access to files, directories, and system resources. Overview of the key concepts and commands related to user and group management.
User and group management in Linux allows administrators to control access to system resources efficiently. By assigning users to groups, administrators can manage permissions on files, directories, and processes, ensuring that the system is secure and users have appropriate levels of access.</font>

**1. Users in Linux**

 **`Users types:`**
 - **`Root User:`** This user is superuser. This user have complete control over the system. This user can perform any action, including administrative tasks.
 - **`Regular User:`** A non root users or non-priviliged user. This user have limited permissions. This user can have only permissions for modify files and directories they own.
 - **`System User:`** This users created by systems. This users don't have login access and used run background process.
- A user have Username, UID(user id), Home directory of a user and Shell.</font>

**2. Groups in Linux**

Groups are collections of users, which allow for easier management of file permissions and system access.
- **Primary Group:** Every user is a member of a primary group, which is specified when the user is created. Files created by the user are usually associated with this group.

- **Supplementary (Secondary) Groups:** Users can also belong to additional groups, which provide extra permissions.
- A group have Group Name and Group ID. </font>

###### **3. User and Group Files**

- **/etc/passwd:** Contains user account information.
- **/etc/group:** Contains group information.
- **/etc/shadow:** Contains encrypted password information.</font>

- **Create user and Password changing and changing one user to another**
  - Creating user in linux using `useradd` and `adduser` and check the users list in linux using `/etc/passwd` command
  ![alt text](<Screenshot 2024-09-11 131628.png>)
  ![alt text](<Screenshot 2024-09-11 131647.png>)
  
  - Change the password of the user using `passwd` command and change one user to another user
  how to change the password
  ![alt text](<Screenshot 2024-09-11 131908.png>) 
  changing one user to another user in linux
  ![alt text](<Screenshot 2024-09-11 132251.png>)
- **Create group and add that group to user**
    Create group using `groupadd` command and add user to that group using `usermod` command and check the group is created or not
    ![alt text](<Screenshot 2024-09-11 163207-1.png>)

    check the user is created or not using `cat /etc/group`
    ![alt text](<Screenshot 2024-09-11 163540.png>)


##### **EXERCISES  FOR DAY-1**

**1. Create, move and delete files and directories**
 - Created directories and files using `mkdir` and `touch` commands
![alt text](<Screenshot 2024-09-06 003013-1.png>) Created directories spet, abc1, abc2 and abc3
![alt text](<Screenshot 2024-09-06 003041.png>) Created fies file1.txt, file2.txt and file3.txt

- Changing one directory to another using `cd` command
![alt text](<Screenshot 2024-09-06 003336.png>)

- Moving a file to dirctory using `mv` command
![alt text](<Screenshot 2024-09-06 003107.png>)

- List files in a directory using `ls` command
![alt text](<Screenshot 2024-09-06 003117.png>)

- Removing or deleteing a directory or file using `rm` command
![alt text](<Screenshot 2024-09-06 003226.png>)

- Using `pwd` command for current working directory
![alt text](<Screenshot 2024-09-06 003351.png>)

**2. Practice using basic shell commands to interact with the file system**

- Finding and Searching
`find:` Finds files and directories based on conditions.

```bash
$ find /abc2 -name "file1.txt"
```
```bash
$ grep "test" file2.txt
$ grep -r "test" /abc1/file1.txt
```
- Viewing file contents

`less` This command allow you to view the content of file page by page
```bash
 $ less file3.txt
 ```
 `head & tail` These commands will display the first and last lines of a file. head is first lies and tail is last lines
```bash
$ head file1.txt
$ tail file2.txt
```
- Copy the files or directories

`cp` This command is used to copy the files or directories
```bash
$ cp file3.txt abc3
```
**3. Create files with different permission settings and modify them using `chmod`**
- I am giving a directory to some permissions like `644` users=read+write, group=read, others=read
![alt text](<Screenshot 2024-09-06 002712.png>)
- Giving permissons to a file for `755` users=read+write+execute, group=read+execute, others=read+execute
```bash
$ chmod 755 file2.txt
```
---------------------------------------------------------------------------------------------------------------------------
## **Day-2**

## <center>**Shell Scripting and Automation Basics**</center>
- Shell scripting is an important part of process automation in Linux. Scripting helps write a sequence of commands in a file and then execute them.
- Shell scripting is primarily used to automate repetitive system tasks, such as backing up files, monitoring system resources, and managing user accounts. 
- Generally all the shell scripts will have extensions of `.sh`

##### **What is shebang`#!/bin/bash`**
- It is called the shebang
- It tells the linux system which binary to use to execute the script
- Since we are executing the shell scripts on bash prompt our shebang is `#!/bin/bash`
- Remember file permissions in linux (RWX) to execute scripts we need execute permissions
  ![alt text](image-23.png)
  ![alt text](image-24.png)

##### **What is variable**
- Variable is a standard building block in scripting languages, They allow you to store information, so that we can retrieve/change multiple times during the execution of script.
- Assigning the value variable <variable_name>=<variable_value>
  - **System Defined variables:** System-defined variables, also called environment variables, are generally Capitalised. We can view all the current environment variables using the printenv command. 
  - **User-Defined Variables.** User-Defined variables are set by the user, and they exist only during script execution


##### **Parameters & arguments**
- **Argument** is something which you pass to a script.
  - **Arguments**
    `$#`	Number of arguments
    `$*`	All positional arguments (as a single word)
    `$@`	All positional arguments (as separate strings)
    `$1`	First argument
    `$_`	Last argument of the previous command
- **Parameter** What you define in a script to hold argument value is parameter

- **Positional arguments in shell scripts**
  The arguments which are passed to the shell script after the filepath of shell becomes positional arguments
  ex:-
  ```
  ./myscript.sh 12 13
  ```

##### **Comparison Operators**
We do these comparisons to make decisions, we will see how to do that later in this article, but before that, here is a list of some comparison operators.
- **Integer operators**
    - `-eq` is equal to
    - `-ne` is not equal to
    - `-gt` is greater than
    - `-ge` is greater than or equal to 
    - `-lt` is less than
    - `-le` is less than or equal to 
- **String comparison**
    - `==` is equal to
    - `!=` is not equal to
  
##### **Loops and Conditional statements**

- **Loops**
Looping in shell scripting  executing commands repeatedly based on certain conditions or over a set of values. The primary types of loops in shell scripting include for, while, and until loops, each loop have different works
- **for loop** 
The for loop operates on lists of items. It repeats a set of commands for every item in a list. 
- **do loop**
In shell scripting, the do loop is commonly used in conjunction with control structures like for, while, and until loops to execute a block of commands repeatedly.






--------------------------------------------------------------------------------------------------------

## **Day-3**
## <center>**Process Management, System Monitoring and Networking**</center>

##### **Process Management**
- **Process** A process is basically a program that is executing. Executing the program happens in sequentials. To run anything on OS, a process has to be created 
      - **Process Life cycle** 
        - Start
        - Ready
        - Running 
        - Waiting
        - Terminated or exited  
- **What is Process Management**
The fundamental functions of process management include starting, stopping, and arranging processes within an operating system. Consider a process as an instance of a program currently running, complete with its execution environment, memory, and CPU state. Due to its ability to manage several processes concurrently, Linux is a multitasking operating system that enables users to run multiple programs simultaneously.
  - **There are two types of processes :**
    - **1.Foreground :** These are the processes which are to be executed or initiated by the user or the programmer, they can not be initialized by system services. Such processes take input from the user and return the output.
    - **2.Background :** These are the processes that are to be executed or initiated by the system itself or by users, though they can even be managed by users. These processes have a unique PID or process if assigned to them and we can initiate other processes within the same terminal from which they are initiated.
    - **3.Stopped**
  - **Commands and examples**
    - `jobs:` List the jobs
    - `fg %n:` Bring the current or specified job in the foreground
    - `bg %n:` Place the current or specified job in the background
    - `Conytol-z` Stops the foreground job & places it in the background as stopped job
  - **Examples**
    - `sleep 1d &`  job placed in the background
    - `fg %1` job placed in the foreground (1 is job id number)
     ![alt text](image-18.png)

- **Commands for Process Management in Linux**
  - Linux provides several commands for managing processes
  - **`ps`** Report the snapshot of the current process. This command will show static info
    **`ps x`** This command will show all of the our process regardless of what terminal they are controlled by.
    **`ps aux`** 
    **a**= All board: Every process, regardless of its owner, is displayed, democratizing process management.
    **u**= Know they user: It adds a human touch, showing the user behind each process, along with vital stats like CPU and memory usage.
    **x**= The hidden: Even processes lurking in the shadows, without a terminal to call home, are brought into the light. 
    ![alt text](<Screenshot 2024-09-13 114437.png>)
    ![alt text](<Screenshot 2024-09-13 115224.png>)
      - Explaination of the above proces `State`
        R : Running
        S : Sleeping
        D : Uninterruptible sleep
        T : Stopped
        < : A priority process
        N : A low priority process
    ![alt text](image-19.png)
      - Explanation of the above process
        USER : User ID this is owner of the process
        %CPU : Cpu usage in percent
        %MEM : Memory usage in percent
        VSZ  : Virtual memory size
        RSS  : Resident set size. This is amount of physical memory the process is using in kilobytes
        START: Time when the process is started 

###### **Managing process commands**

  - **`top`** This command will provides all running Linux process. This command will show dynamic info. 
              It helps in monitoring system usage and performances It is mainly used to detect load on the server by system administration. I
              The top command stands for table of processes. It is a task manager program, detected in several Unix-like operating systems, that shows information about memory and CPU utilization.
  - **`htop`** This command will provide real time monitoring of process and performs every tasks to monitor the process in the linux system. It is new and updated command of top command

  - **`kill`** The `kill` command used to kill the process in linux. Every process will have process ID. To kill a process in linux use `kill` command and PID.

  - **`pkill`** This command uses name of the process instead of PID. Signal can be send to a process either by typing full name or partial name.

  ###### **System monitoring commands and tools**

  - **`df`** Check the status of various partitions and drives on server to see how full they are. To see the mounted partitions, their mount points and amount of disk space.
    - `-a, --all` Includes all file systems, including dummy file systems with zero block sizes. `df -a` & `df -all`.
    - `-B, --block-size=S` Scales sizes by the specified size (e.g., -BM shows sizes in megabytes). `df -B`
    - `--total` Displays a grand total of all file systems. `df --total`
    - `-h, --human-readable` Prints sizes in human-readable format (e.g., KB, MB, GB).`df -h` & `df --human-readable`
    - `-H, --si` Uses powers of 1000 (e.g., kB, MB) instead of 1024. `df -H`
    - `-i, --inodes` Displays information about inodes instead of block usage. `df -i` & `df --inodes`
    - `-k`  Displays file system information and usage in 1K blocks (default behavior). `df -k`
    - `-l, --local` Displays only local file systems, excluding network file systems. `df -l` & `df --local`
    - `-P, --portability`  Uses the POSIX output format. `df -P` & `df --portability`
    - `-t, --type=TYPE` Displays only file systems of the specified type. `df -t squashfs`
    - `-T, --print-type` Displays the type of each file system. `df -T <file>`
    - `-x, --exclude-type=TYPE` Excludes file systems of the specified type from the output. `df -x <file>`
    - `--no-sync`  Does not invoke sync before getting usage info (default). `df --no-sync`
    - `--sync`  Invokes sync before getting usage info, ensuring the output is fully up to date. `df --sync`
    - `--help`  Displays a help message and exits. `df --help`
    - `--version` Displays version information and exits. `df --version`
    - `-V`  Ignored, included for compatibility reasons. `df -V`</br>
  

  - **`du`** To see the disk usage of the each file in bytes.
    - `-a`          Show disk usage of all files, not just directories.                      `du -a <path>`        
    - `-c`          Produce a grand total.                                                   `du -c <path>`        
    - `-h`          Display sizes in human-readable format (e.g., KB, MB).                   `du -h <path>`        
    - `-s`          Display only a total for each argument.                                  `du -s <path>`        
    - `-S`          Do not include size of subdirectories.                                   `du -S <path>`        
    - `-x`          Skip directories on different file systems.                              `du -x <path>`        
    - `--max-depth=N` Show the total for a directory (or file, with -a) only if it is N or fewer levels below the  command line argument.                                                                 `du --max-depth=1<path>`
                                                                                                      
    - `--exclude=PATTERN`  Exclude files that match PATTERN. `du --exclude=PATTERN`                                                            
                                                                                                  


  - **`free`** This command which displays the total amount of free space available along with the amount of memory used and swap memory in the system. It displays the all details regarding the RAM usage such as how is the total, what is used and free memory including buffers and cached data, aiding in real time monitoring of memory resources.
      - `-k (kilo)`  Display the memory usage in kilobytes. `free -k`
      - `-m (mega)`  Display the memory usage in megabytes. `free -m`
      - `-g (giga)`  Display the memory usage in gigabytes. `free -g`
      - `-tera`      Display the memory usage in terrabytes.`free -tera`
      - `-h (human)` Automatically scales all output columns to the shortest three-digit unit and display the units. `free -h`
      - `-c (count)` Display the output `c` number of times
      - `-l (lohi)`  It will show detailed low and high memory statistics. `free -l`
      - `-o (old)`   It will Disables the display of the buffer-adjusted line. `free -o`
      - `-s (seconds)` It will continuously displays the output after `s` seconds delay. Uses the usleep system call for microsecond resolution delay times. `free -s`
      - `-t (total)` Adds an additional line in the output showing column totals. `free -t`
      - `-help`      Displays a help messege and exits. `free -help`
      - `-V (version)` Displays version information and exits. `free -V`


  - **`uptime`** This command will display the information from how long the system is running, how many users login and load average
      - `-p (pretty)` It will show the uptime in pretty. `uptime -p`
      - `-h (help)`   It will display the help and exit
      - `-s (since)`  It will show the when system is up since
      - `-V (version)`It will display the version information and exit   

  ###### **Networking commands**

  - **`ifconfig`** This command will display all the active network interface configuration details that includes their assigned IP addresses, netmask, and other relevant information.
      - `-a`   Display all interfaces, including those that are down. `ifconfig -a`
      - `-s`   Display a short list, instead of details. `ifconfig -s`
      - `-v`   Run the command in verbose mode. `ifconfig -v`
      - `up`   To assign an IP address to a network interface. `ifconfig eth0 <IP Address> netmask <> up`
      - `down` To remove an IP address to a network interface. `ifconfig eth0 <IP Address> down`
      - `arp, [-]arp` Enable/disable the use of ARP protocol on an interface. 
      - `netmask` Changes the network mask for a specific interface. `ifconfig interface netmask <mask_IP>`
      - `broadcast` Sets the broadcast address for a specific interface. `ifconfig interface broadcast <broadcast_IP>`
      - `-promisc, [-]promisc`  Enable/disable promiscuous mode on an interface. The promiscuous mode lets a network device receive all types of packets. It’s commonly used for checking network activities. `ifconfig interface promisc`
      - `-allmulti, [-]allmulti`  Enable/disable all-multicast mode for an interface. `ifconfig interface -allmulti`
      - `-mtu`  Sets the Maximum Transfer Unit (MTU) of an interface. The maximum transmission unit (MTU) restricts the size of packets that can be sent via an interface. Use the mtu argument with the ifconfig command to specify a value. `ifconfig interface mtu <number>`

      
  - **`ip`** This command is the newer version of the `ifconfig` command. It can be used to assign and remove addresses, take the interfaces up or down and much more useful tasks.

  - **`ping`** ping stands for (packet internet groper) is used to check the network connectivity between the host and server. This command takes as input the IP address or domains and sends a data pocket to the specified address with the message "PING" and get response from the server.
      - `-c` By default, ping sends unlimited packets until the user terminates the process. To send a specific number of packets, use the -c option. `ping -c 5 google.com`
      - `-a` The -a option will play a sound when the ping command receives a response from the target device. Since keeping Terminal open until it receives a response is inconvenient, this option is useful for network troubleshooting. `ping -a google.com/destination`
      - `-i`  To change the ping interval’s default value, use the -i option and specify the number of seconds. To set it faster than a second, use a decimal. `ping -i 0.5 destination`
      - `-s`  Specifies the number of data bytes to be sent. `ping -s 30 google.com`
      - `-v`  enables verbose output. `ping -v google.com`
      - `-V`  Check the ping version. `ping -V`
      - `-q`  Continuous ping monitoring can be tedious due to Terminal’s long output. To simplify the results, use the -q option. The command will summarize all the ping statistics in a single output, simplifying analysis. `ping -q google.com`
      - `-f`  The ping command lets you rapidly send packets in large quantities using the -f option. It helps simulate your server performance during a traffic spike or distributed denial-of-service (DDoS) attack. `ping -f google.com`
      - `-4, -6`  Due to internet development, the IPv4 IP addresses are running out, and IPv6 is becoming more common. The ping command’s default setting uses IPv4, but you can use either internet protocol.Add the -4 option to use the IPv4 address and -6 to send an IPv6 ping. `ping 4 google.com` & `ping 6 google.com `
      - `-s` By default, the ping command sends a packet with 56(84) bytes of data. 56 represents your packet size in bytes. Meanwhile, 84 specifies the total ping byte size, including all headers, which add 28 bytes. `ping -s 123 google.com`
      - `-D` To simplify network performance monitoring, the ping command lets you add a timestamp to the packet response. To do so, add the -D option using the following command. `ping -D google.com`
      - `-w, -W` The ping command has two timeout options, -W and -w. The -W option determines the time each ping will wait until the specified host sends a response. If it exceeds the time, the request is timed out. `ping -w google.com` & `ping -W google.com`


  - **`netstat`** netstat stands for (network statistics) This command helps for understand and check things about how our computer connects to the internet. It can tell you about the connections our computer is making, the paths it uses to send information, and even some technical details like how many pockets of data are being sent or received. It allows users to display network related information and diagnose various networking issues.
      - `-a`    Represents every socket, both non-listening and listening, and every protocol, like UDP, TCP, etc.`netstat -a`
      - `-at`   Represents TCP connections only (-au represents UDP connections only). `netstat -at`
      - `-ant`  Represents every TCP connection without DNS resolution (rather than displays IP addresses). `netstat -ant`
      - `-al`   Displays listening sockets only. `netstat -al`
      - `-aep`  Displays PID and to which function all sockets belong; e includes extra information like the user. Execute as root to check every PID. `netstat -aep`
      - `-s`   Displays network statistics and we can redirect out put to a file. `netstate -s > <file-name>`
      - `-i`   Shows a table of every network interface. Include -e to receive the result, which is the same as ifconfig. `netstat -i`
      - `-r`   Displays the information on kernel routing. It is a similar result as route -e. `netstat -r`
      - `-ct`  Shows TCP connections regularly. `netstat -ct`
      - `-g`   Shows the information of multicast group membership for IPv6 and IPv4. `netstat -g`
      - `-atnp`  Shows every "established" connection of TCP currently. `netstat -atnp | grep ESTA`
      - `-lntu`  Shows every service listening UDP and TCP, every free open port over the local device. `netstat -lntu`

  - **`curl`** This command is used to transfer data using various protocols such as HTTP, HTTPS, FTP, SCP, SFTP and more
      - `-X`  <HTTP_METHOD> – specifies which HTTP method to use. `curl -X GET <URL>/reource`
      - `-H`  “HeaderName: HeaderValue” sets custom HTTP headers for the request. `curl -H "HeaderName:HeaderValue" <URL>`
      - `-d`  “Data” – sends data in the request body. `curl -d <URL>`
      - `-o`  <output_file> – saves the response to a file. `curl -o <file-name> <URL>`
      - `-O`  Saves a remote file and save file it with the same name as in the URL. `curl -O <URL>` 
      - `-i`  Includes HTTP response headers in the output. `curl -i <URL>`
      - `-L`  Follows HTTP redirects. `curl -L <URL>/redirected-page`  
      - `-k`  Allows connections to SSL sites without certificates. `curl -k --head <URL>/login`
      - `-v`  Provides verbose output for debugging. `curl -v <URL>`
      - `-T`  In addition to downloading, `curl` can also upload files to a server using various protocols. `curl -T <uploadfile.txt> ftp:<URL>/upload`
      - `-u`  The curl -u command is used for making HTTP requests with authentication. The -u option is followed by a username and an optional password, separated by a colon. This allows you to include credentials in your request. `curl -u <UserName>:<Password> <URL>/resource`

  ###### **SSH (Secure Shell/Secure Socket Shell)**

  - **SSH** Stands for **Secure socket shell** and **Secure shell**. SSH is a widely used network protocol that provides a secure way to connect remote servers and computers. It provides a secure encrypted connection between two hosts over an insecure network. This connection can also be used for terminal access, file transfers, and for tunneling other applications.
  - SSH protocol uses symmetric encryption, asymmetric encryption and hashing in order to secure transmission of information.
      - Encryption and Decryption have two ways
        - Symmetric encryption
        - Asymmetric encryption
      - **Symmetric encryption :** In symmetric encryption both users will have same key to encrypt and decrypt.
      - **Asymmetric encryption :** In asymmetric encryption both users will create a keypair and both keys are different. One key is called public and other key is called private.
        - If the message is encrypted with public key it can be decrypted with private key and other way arount
  - **Telnet** was used to communicated with a remote server, Telnet is not secure communication protocol & it transfers the data over network/internet in a plane text, so to overcome this issue **SSH** came into existence.
  - **SSH** protocol provides the secure way of accessing remote servers.

  ###### **How SSH works** 
  -  SSh Protocol uses symmetric encryption, asymmetric encryption and hashing in order to secure transmission of information.
  - SSH Connection between client and server happens 3 stages
     **1.** Verification of server by the client
     **2.** Generation of session key to encrypt all the communication
     **3.** Authentication of the client by server

     **Process for Verification of the server by client**
       Client initiates ssh connection with server. Server listens to ssh connections by default on port 22. At this point is server identity verified, but we have two cases 
       **1.** Communication b/w client and server for the first time:
           - client is asked to authenticate the server manually by verifying the public key of the server. Once the key is verified, the server will be added to ~/.ssh/known_hosts.
       **2.** If the client is not accessing the server for the first time server’s identity will be matched with previously recorded information on known_hosts file

  ###### **Package Management In Linux**
  - package manager is a software tool used for package management in Linux i.e. to manage the installation, removal, and updating of various software packages. It can be thought of as a hub for all software packages available for your system. The package manager keeps track of all the installed packages on the system, including their dependencies, and uses this information to resolve conflicts and handle updates.
  - Software packages are collections of files, including executables, libraries, configuration files, and documentation, that are bundled together for easy distribution and installation. Package managers keep track of these packages, making it easier to manage software on a Linux system.
  - Functionality of package manager in linux
    - Installation
    - Dependency resolution
    - Upgrading
    - Remove
    - Querying 
##### **Package managers in linux**



1. **Repository :**
    - A linux repository is a storage location from which our system can install applications as well as Operating system updates.
    - Each repository is collection of software hosted on remote server so that it can be used my many systems for installing/updgrading softwares (packages)

2. **RPM (Red Hat Package Manager):** 
    - RPM is a software management system that is used for installation & removal of software packages.
    - A package typically consists of archive of files and other metadata, includes configuration files, binaries.
    - RPM is pre-install on all redhat flavors like centos, rhel, fedora, Amazon linux etc…
    - Query, verify, update, install and uninstall software
   
3. **DPMS (Debian Package Management System):**
    - DPMS is the framework for managing software on Debian or Debian-like systems. Debian packages end with .deb
    - At the core of DPMS is the dpkg application which works with the system providing several command line options.</font>

  ###### **Automatic updates and package installers**
  

1. **YUM (Yellowdog Updater Modified):**
    - yum is a popular packaging/updating tool for managing software on Linux systems. It is basically a wrapper program for RPM with enhancements.
    - Yum is pre installed on rhel family like centos, redhat, amazon linux
    - Yum configuration is located at /etc/yum.conf provides system-wide configuration options for yum.
    - Yum configuration is located at /etc/yum.conf provides system-wide configuration options for yum.
    - If you want to add a repo create a file with .repo extension in `/etc/yum.repos.d`
2. **APT (Advanced Package Tool):**
    - APT is a tool for managing packages on ubuntu based systems
    - APT is a powerful and widely used package manager in the Linux world. It’s the default package manager for Debian-based distributions, including Debian itself, Ubuntu, and Linux Mint. APT simplifies software management, ensuring that users can easily install, update, and remove packages while taking care of dependencies.
    - APT cheat sheet link for more commands how to use [Link](https://blog.packagecloud.io/apt-cheat-sheet/#apt-get-high-level-package-handling-utility)
3. **DNF (Dandified YUM):**
    - DNF makes it easy to maintain packages by automatically checking for dependencies and determines the actions required to install packages. This method eliminates the need to manually install or update the package, and its dependencies, using the rpm command. DNF is now the default software package management tool in Fedora.
    - DNF cheat sheet link for more commands how to use [Link](https://opensource.com/sites/default/files/gated-content/osdc_cheatsheet-dnf-2021.5.15.pdf).</font>

##### **Configuration files**
1. **/etc/hosts :**
  - The /etc/hosts file in Linux or any other operating system is used to map connections between IP addresses and domain names.
  - In the earlier days of networking, the /etc/hosts file was used to translate the IP addressed (192.168.1.0) to human-readable form (google.com) and over time it lost its relevance. In modern systems, the whole process of resolving domain names is done through DNS (Domain Name System).
  - Use cases
      - When you want to block certain websites.
      - It can be used as a backup in the case when DNS is broken.
      - You can also use it as a local DNS server.
      ![alt text](image-21.png)
2. **/etc/fstab :** 
  - Fstab is a file system table used by the kernel during boot time to mount the file system. To put it in simple terms, we will create one or more partitions on our hard drive and you will make an entry for each partition in fstab which will be read by the kernel during boot time and the file system will be automatically mounted.
  - By default, any partitions you create during the OS installation will be automatically added to the fstab file.
  ![alt text](image-22.png)

3. **/etc/ssh/sshd_config :**
  - This file contains a wide range of configuration parameters that define how the SSH server operates. These parameters include settings related to authentication, encryption, logging, access control, and more.
  - Security Configuration: We can define various security related settings like authentication methods, allowed ssh protocol versions,encryption algorithm, user access permissions etc to ensure that only authorized users have access to the server. Also, can change the default SSH port number.
  - SSH user access control : Through this sshd_config, administrators can control the user's SSH access by specifying rules for user authentication, IP-based access restrictions and access permission.
  - Enable/Disable SSH logs : We can configure settings related to logging levels, log file locations, and log file formats etc in sshd_config file to facilitate auditing, troubleshooting, and monitoring of SSH server activities.
  - Customization: We can customize the behavior of SSH server (session timeout, maximum number of concurrent connections, and banner messages etc) by modifying the parameters in sshd_cofig file. 
    ![alt text](<Screenshot 2024-09-28 071116.png>)

#### **EXERCISES FOR DAY-3**
1. **Check disk usage, memory usage, and system uptime**
  - **df :** 
  ![alt text](<Screenshot 2024-09-19 171955-1.png>)
  ![alt text](<Screenshot 2024-09-19 191331-1.png>)
  ![alt text](<Screenshot 2024-09-19 191356-1.png>)

  - **du :**
  ![alt text](<Screenshot 2024-09-19 191356-2.png>)
  ![alt text](<Screenshot 2024-09-20 105230.png>)
  ![alt text](<Screenshot 2024-09-20 105408.png>)
  ![alt text](<Screenshot 2024-09-20 105306.png>)
  ![alt text](<Screenshot 2024-09-20 105320.png>)

  - **uptime :**
  ![alt text](<Screenshot 2024-09-20 105559.png>)
  ![alt text](<Screenshot 2024-09-20 105659.png>)

2. **Use basic networking commands to check connectivity**
  - **ifconfig :**
  ![alt text](<Screenshot 2024-09-20 123543.png>)
  ![alt text](<Screenshot 2024-09-20 123600.png>)

  - **ping :** 
  ![alt text](<Screenshot 2024-09-22 162944.png>)
  ![alt text](<Screenshot 2024-09-22 163013.png>)

  - **netstat :**
  ![alt text](<Screenshot 2024-09-22 163107.png>)
  ![alt text](<Screenshot 2024-09-22 163152.png>)

  - **curl :**
  ![alt text](<Screenshot 2024-09-22 163519.png>)
  ![alt text](<Screenshot 2024-09-22 163629.png>)
  ![alt text](<Screenshot 2024-09-22 163735.png>)

3. **SSH into a remote server and run commands**
  - **SSH :** 
  ![alt text](<Screenshot 2024-09-22 163828.png>)

4. **Managing packages on Linux**
  - **APT :**
  ![alt text](<Screenshot 2024-09-22 163849.png>)
  ![alt text](<Screenshot 2024-09-22 163918.png>)














---------------------------------------------------------------------------------------------------------------------
## **Day-4**
## <center>**INTRODUCTION TO DOCKER**</center>

##### **What is Docker?**
- Docker is a open-source containerization tool that allow you to build, test, deploy and manage virtualized application in containers on a common operating system.

##### **How Docker works**
- Docker works by providing a standard way to run your code. Docker is an operating system for containers. 
- Similar to how a virtual machine virtualizes server hardware, containers virtualize the operating system of a server.
- Docker is installed on each server and providers simple commands you can use to build, start, or stop containers.
![alt text](image-16.png)

##### **Docker Arcitecture**
![alt text](image-17.png)

- **What is Dockerfile**
A Dockerfile is a script that contains instructions for building a customized docker image. Each instruction in a Dockerfile creates a new layer in the image, and the final image is composed of all the layers stacked on top of each other.
  - **Dockerfile Instructions**
`FROM`	: to get the os for conatiner.
`RUN`		: to execute linux commands(image creation)
`CMD`		: to execute linux commands(container creation)
`ENTRYPOINT`	: high priority than CMD
`COPY`		: it will copy local files to conatiner.
`ADD`		: it will copy internet files to conatiner.
`WORKDIR`		: to go specific foilder inside container
`LABEL`		: used to attach labels for image
`ENV`		: to pass env variables inside the container
`ARG`		: to pass env variables outside the container
`EXPOSE`		: used to allocate port number

- **What is Docker Image**
It is a file, comprised of multiple layers, used to execute code in a Docker container. They are a set of instructions used to create docker containers. Docker Image is an executable package of software that includes everything needed to run an application.

- **What is Docker Container**
Docker container is a runtime instance of an image. Allows developers to package applications with all parts needed such as libraries and other dependencies. Docker Containers are runtime instances of Docker images.

- **What is Docker Hub**
Docker Hub is a repository service and it is a cloud-based service where people push their Docker Container Images and also pull the Docker Container Images from the Docker Hub anytime or anywhere via the internet.

- **Docker Engine**
The software that hosts the containers is named Docker Engine. Docker Engine is a client-server based application. The docker engine has 3 main components:
**Server:** It is responsible for creating and managing Docker images, containers, networks, and volumes on the
              Docker. It is referred to as a daemon process.
**REST API:** It specifies how the applications can interact with the Server and instructs it what to do.
**Client:** The Client is a docker command-line interface (CLI), that allows us to interact with Docker using the docker commands.

- **Docker daemon** The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.

-   **Docker client** The Docker client (docker) is the primary way that many Docker users interact with Docker. When you use commands such as docker run, the client sends these commands to dockerd, which carries them out. The docker command uses the Docker API. The Docker client can communicate with more than one daemon.

#### **EXERCISES  FOR DAY-4**

1) **Docker Installation on Linux Ubuntu**

- Follow the official documentation [refer here](https://docs.docker.com/desktop/install/linux-install/)

```bash
# Add Docker's official GPG key: for import and verify the authenticity of docker repository package.
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```bash
# List the available versions:
$ apt-cache madison docker-ce | awk '{ print $3 }'

# VERSION_STRING= You want specific versrion then enter the above command the docker versions list will appear in that select what you want ex:5:26.1.0-1~ubuntu.22.04~jammy
$ sudo apt-get install docker-ce=$VERSION_STRING docker-ce-cli=$VERSION_STRING containerd.io docker-buildx-plugin docker-compose-plugin

# Now check the Docker version
$ docker --version
```
2) **Pull image and Run container**

- Pull the nginx image 
![alt text](<Screenshot 2024-09-10 144113.png>)
- Run the container 
![alt text](<Screenshot 2024-09-10 144501.png>)

3) **Docker basic commands**

- basic docker commands 
![alt text](<Screenshot 2024-09-10 144835.png>)

- Stoppin and removing container 
![alt text](<Screenshot 2024-09-10 144917.png>)

4) **Simple `Dockerfile` for nignx image taking base image ubuntu deploy it at access in your web browser,and push to docker registry.**
- `Dockerfile`
```bash
FROM ubuntu:latest
RUN apt update && apt install nginx -y
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```
- Build docker image 
![alt text](<Screenshot 2024-09-10 152349.png>)

- Run as container 
![alt text](<Screenshot 2024-09-10 152414.png>)

- Accessing via browser port number 32769
![alt text](<Screenshot 2024-09-10 152232.png>)

- Tag docker image 
![alt text](<Screenshot 2024-09-10 162540.png>)

- Login your dockerhub credentials and push tagged image to dockerhub
![alt text](<Screenshot 2024-09-10 162617.png>) 

- In dockerhub new image `test` is present
![alt text](<Screenshot 2024-09-10 162511.png>)

---------------------------------------------------------------------------------------------------------------------
## **DAY-5,6**

## <center>**Working with Docker Volumes and Docker Networks**</center>


#### **Docker Volumes:-**
 - In docker, we use volumes to store the data. Volume is nothing but a folder inside a container, we can share a volume from one container to another.
- The volume contains the files which have data, we can attach the single volume to multiple containers but at a time we can attach only one volume to one container. Volumes are decoupled (loosely attached) if we delete the container volume will not be deleted.

 ###### **Types of Docker Volumes**
 

- **Named Volumes:** Named volumes are the most commonly used type of volume in Docker. They are created and managed by Docker itself. We can give a volume a specific name, and Docker takes care of creating and maintaining the volume for us. Named volumes are easy to use and provide better readability in your Docker commands.
- **Host Bind Mounts:** Host bind mounts allow you to mount a directory from our host machine into a Docker container. With this type of volume, the directory's contents on the host are directly accessible to the container. Changes made in the container will be reflected on the host. Host bind mounts provide a way to share data between the host and the container.
- **Tmpfs Mounts:** Tmpfs mounts are stored in the host's memory and not written to the host filesystem. They are useful when you need a lightweight and temporary storage option. Tmpfs mounts are created and managed by Docker, and their data resides in the host's memory. Once the container is stopped or removed, the data in a tmpfs mount is lost.


#### **Docker Networking:-**


- Docker networks are used to make communication between the multiple containers that are running on same or different docker hosts. 
- Docker networking enables containers to communicate with each other and with external systems. It provides isolation, security, and flexibility by creating virtual networks that connect containers, allowing them to share data, services, and resources while maintaining separation.


###### **Types of Docker Networks**

- ###### **There are 4 types of Networks are available in Docker**

- `bridge:-` It is a default network that container will communicate with each other within the same host.
- `host:-` When you Want your container IP and ec2 instance IP same then you use host network.
- `null:-` When you don’t Want The container to get exposed to the world, we use none network. It will not provide any network to our container.
- `overlay:-` Used to communicate containers with each other across the multiple docker hosts.

##### **EXERCISES FOR DAY-5,6**

- ###### **Create a docker image, that should be able to run the systemctl commands**
  - 

- ###### **Build a Docker image from Dockerfile that includes a simple ubuntu base image**

  -  Created a Docker image from a `Dockerfile` using simple ubuntu base image and run the container and expose to the host machine

      **Dockerfile**

      ```
      FROM ubuntu:latest
      LABEL created="saikrishna"
      WORKDIR /voziq
      RUN apt-get update && apt-get install python3 -y && apt-get clean
      COPY hello.py .
      CMD ["python3", "hello.py"]
      ```



      ![alt text](<Screenshot 2024-09-27 212749.png>)
      ![alt text](<Screenshot 2024-09-27 212551.png>)
      ![alt text](<Screenshot 2024-09-27 212532.png>)


- ###### **Create and manage Docker Volumes to persist data**
  1. **Docker volume creation Named volumes**
  ![alt text](image-20.png)
  
  - Docker volume create using `docker volume create <volume-name>`command and inspect this volume using `docker volume inspect <volume-name>` 
  ![alt text](<Screenshot 2024-09-26 172644.png>) ![alt text](<Screenshot 2024-09-26 172727.png>)

  - Attach Docker volume to a container container name=voziq and inspecting that container and verify the volume is mounted or not to the container 
  ![alt text](<Screenshot 2024-09-26 175537.png>) ![alt text](<Screenshot 2024-09-26 173049.png>) ![alt text](<Screenshot 2024-09-26 175146.png>)

  2. **Bind mounts volumes**
  - Create Docker volume `voziq` mounting this docker volume in the process of container creation. Container name= "test" using this command  `docker run -d --name <container-name> --mount source=<volume-name>,destination=<path in container> <image name>` 
  - Inspect and created some files in this container then deleted container because how working volumes and after delete that container the files are presented or not in the above volume `voziq`
    - Volume creation
  ![alt text](<Screenshot 2024-09-26 181619.png>) 
    - Inspecting above volume
  ![alt text](<Screenshot 2024-09-26 181717.png>)
    - Mounting volume to container in the process of container creation path in container is `data`
  ![alt text](<Screenshot 2024-09-26 181843.png>)
    - Inspect the container
  ![alt text](<Screenshot 2024-09-26 181922.png>) 
    - Interact with the container using `docker exec -it test /bin/bash` command and create 2 files `abc.txt` `file.txt`
  ![alt text](<Screenshot 2024-09-26 183437.png>) ![alt text](<Screenshot 2024-09-26 182211.png>)
    - Stop and delete the container 
  ![alt text](<Screenshot 2024-09-26 182454.png>)
    - Check the files are present or not in the volume
  ![alt text](<Screenshot 2024-09-26 182504.png>)

  - Another 
    ![alt text](<Screenshot 2024-09-27 192026.png>)
    ![alt text](<Screenshot 2024-09-27 192008.png>)

  3. **tmfps mounts**
    - Attaching `tmfps` volume in the process of container creation container path is `app`
    ![alt text](<Screenshot 2024-09-26 191121.png>) 

    - Interacting the container for volume path properly mounted or not and created one file `test.txt` with some content in this file `Testing`
    ![alt text](<Screenshot 2024-09-26 184954.png>)

    - Stop and restart the container and check the file is present or not. To see the files are not presented
    ![alt text](<Screenshot 2024-09-26 185106.png>)

- ###### **Set up a simple Docker network and connect multiple containers**
  - Created a **bridge** `voziq-vpn` docker network and inspected that network . It is the Docker default networking mode which will enable the connectivity to the other interfaces of the host machine as well as among containers.

    - Usage of docker network commands
    ![alt text](<Screenshot 2024-09-26 211118.png>)

    - List the docker networks
    ![alt text](<Screenshot 2024-09-26 210121.png>)

    - Created docker network **bridge** `voziq-vpn` and inspected that network. Created docker network two ways
      1. ![alt text](<Screenshot 2024-09-26 211215.png>) 
      2. ![alt text](<Screenshot 2024-09-26 211313.png>)

      - Inspected that network
      ![alt text](<Screenshot 2024-09-27 095625.png>)
    
    - Connect above network to a container and inspect that container
      ![alt text](<Screenshot 2024-09-27 100108.png>)
      ![alt text](<Screenshot 2024-09-27 100044.png>)
      ![alt text](<Screenshot 2024-09-27 100832.png>)

    ###### **Dynamically providing IP address for network**
      - Created a docker network and provided an IP address and inspect that network
        ![alt text](<Screenshot 2024-09-27 195605.png>)
        ![alt text](<Screenshot 2024-09-27 195605-1.png>)
      
      - Checking two containers in `bridge` network are able to communicate with containers  names 
        ![alt text](<Screenshot 2024-09-27 201120-1.png>)

        - Now attached two containers to a `voziq` network
        ![alt text](<Screenshot 2024-09-27 201120.png>)

        - Now communicae containrs with IP address
          ![alt text](<Screenshot 2024-09-27 201249.png>)


  - Connect **None** docker network to a container and inspected that network. This mode will not configure any IP for the container and doesn’t have any access to the external network as well as for other containers. It does have the loopback address and can be used for running batch jobs.
    - Connect **None** docker network to a container and  inspect this network
      ![alt text](<Screenshot 2024-09-27 105529.png>)
    
    - Inspect above network 
      ![alt text](<Screenshot 2024-09-27 105513.png>)

  - Connect **host** docker network to a container and inspected that network. In this mode container will share the host’s network stack and all interfaces from the host will be available to the container. The container’s host name will match the host name on the host system
    - Connect **host** docker network to a container and inspec this network
      ![alt text](<Screenshot 2024-09-27 105529-1.png>)

    - To see the container host name will match the host name on the host system
      ![alt text](<Screenshot 2024-09-27 110321.png>)
      ![alt text](<Screenshot 2024-09-27 110351.png>)

    - Inspect above network
      ![alt text](<Screenshot 2024-09-27 110351-1.png>)

--------------------------------------------------------------------------------------------------------

## **DAY-7**

## <center>INTRODUCTION TO DOCKER COMPOSE</center>

##### **What is Docker Compose**
Its a tool used to launch multiple conatiners, We can create multiple conatiners on single hosts and all of the services informatiom we are going to write on a file called **docker-compose/compose file**. It will be on yaml format, We use key-value pair (dictionary) (.yml or .yaml)
used to manage multiple servivces with help of a file.
##### **What is Docker-compose file**
A Docker Compose file is a YAML file used to define and manage multi-container Docker applications. It allows you to configure your application’s services, networks, and volumes in a single file, making it easier to manage and deploy applications.

#### **EXERCISES FOR DAY-7**

- **Install Docker Compose**
  - Installation steps

    ```
    mkdir -p ~/.docker/cli-plugins/
    curl -SL https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose
    chmod +x ~/.docker/cli-plugins/docker-compose
    docker compose version
    ```
    ![alt text](<Screenshot 2024-09-28 120213.png>)


- **Write a `docker-compose.yaml` file to define a muli-container application**

  -  **docker-compose.yaml**

```
    version: '3.8'

    services:
      frontend:
        image: saikrishna38721/frontend 
        container_name: frontend
        restart: always
        ports:
          - "3000:3000"
        depends_on:
          - backend
        networks:
          - voziq-network
   
      backend:
        image: saikrishna38721/backend 
        container_name: backend
        restart: always
        ports:
          - "5000:5000"
        depends_on:
          - db
        networks:
          - voziq-network

      db:
        image: mysql:5.7
        container_name: mysql
        restart: always
        environment:
          MYSQL_ROOT_PASSWORD: 12345
          MYSQL_DATABASE: mydb
          MYSQL_USER: saikrishna
          MYSQL_PASSWORD: 12345
        ports:
          - 3306:3306
        volumes:
          - mydb_data:/var/lib/mysql
        networks:
          - voziq-network

    networks:
      voziq-network:
        driver: bridge

    volumes:
      mydb_data:
      
```

- **Use `docker-compose up` and `docker-compose down` to start and stop application**
  - Start and stop the application using `docker compose up -d` and `docker compose down`
    ![alt text](<Screenshot 2024-09-28 125925.png>)
    ![alt text](<Screenshot 2024-09-28 125955.png>)
    ![alt text](<Screenshot 2024-09-28 130016.png>)
    ![alt text](<Screenshot 2024-09-28 132103.png>)

- **Explore additional Docker Compose commands like `docker compose logs`, `docker compose ps`, and `docker compose exec`**

    `docker compose up -d	:` to run all services
    `docker compose down	:` to remove all services
    `docker compose stop	:` to stop all services
    `docker compose kill	:` to kill all services
    `docker compose rm	  :` to remove all services which is on stopped state
    `docker compose start	:` to start all services
    `docker compose pause	:` to pause all services
    `docker compose unpause:` to unpause all services
    `docker compose images :` to get all images managed by compose file
    `docker compose ps -a	:` to get all containers managed by compose file
    `docker compose logs	:` to get all logs managed by compose file
    `docker compose scale dth=10:` to create 10 containers of dth
    `docker compose top	  :` to get all process managed by conatiners on compose file
  - Checking logs
  ![alt text](<Screenshot 2024-09-28 130016-1.png>)

  - Interacting with 2 container 
  ![alt text](<Screenshot 2024-09-28 130523.png>)
  ![alt text](<Screenshot 2024-09-28 130523-1.png>)

  - Connecting to mysql container using username and password
  ![alt text](<Screenshot 2024-09-28 130817.png>)

---------------------------------------------------------------------------------------------------------------------

## **DAY-8**

## <center>**INTRODUCTION TO TERRAFFORM**</center>

##### **What is Terraform and Use cases and benifits**

Its a tool used to make infrastructure automation its a free and opensource. Terraform is a tool for provisioning, managing, and deploying infrastructure resources. We can manage infrastructure for your applications across multiple cloud providers - AWS, Azure, GCP, etc Its platform independent and comes on year 2014 innovated mitchel hasimoto and Company hasicorp. Terraform is written on go language we can call terraform as IAAC TOOL.
  **Advantages**
1. Reuseable 
2. Time saving
3. Automation
4. Avoiding mistakes
5. Dry run

##### **How it's work**
- Terraform is developed in Google Go language
- Terraform is a single executable.
- Terraform can interact with specific providers (AWS, Azure, Vmware) to create/manage infrastructure
- Each Provider will have lots of resources which we can define to create infra.
- Terraform uses code to automate the infra.
- we use HCL : HashiCorp Configuration Language.
- What terraform can do is (as of our understanding)
    - init (initialize => downloading providers)
    - apply (create/update infra)
    - destroy (delete infrawork)


##### **What is IAC (Infrastructure as Code)**
The process of creating infrastructure by experessing our infra needs in a declarative way and then executing the template to create infra structure (Virtual) Declarative way.
- IAC is a concept where you express your infrasturcture in a declarative way, We need to express what we want to create/manage (Resource) and Outputs.

##### **HCL (HashiCorp Configuration Language)**
**Resource Block**These are containers that group related configurations. They start with a keyword indicating the type (like resource or variable) and are enclosed in curly braces {}.
  - In terraform, the language which we use is called as HCL (Hashicorp configuration language)
  - Data types: 
      - String (write in quotes)
      - Numbers (It can be different format)
      - Lists (we can write in square brackets `[]`)
      - Maps (we can write in curly brackets `{}`)
    
  - Variable : Terraform provides variables where user can set values while applying
Variable definition



##### **Working with priviers in terraform**
- Terraform supports 130 above clouds 
- provider: A Terraform provider is a plugin that facilitates communication between Terraform and external services or platforms (like AWS, Azure, Google Cloud, etc.). Each provider translates your configuration written in HashiCorp Configuration Language (HCL) into API calls to manage resources
- From terraform block we can restrict provider versions which terraform version is required to run the template.
- In Terraform configuration file, you need to declare which providers you will use. This is done in the terraform block:

**VERSION CONSTARINT:** Used to change the provider version.

```
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 3.0"
    }
  }
}
```
**Commands:**
`terraform init	:` to download provider plugins for resource craetion
`terraform plan  :` to create execution plan
`terraform apply :` to create resource by terraform
`terraform destroy:` to delete resource 

#### **EXERCISES FOR DAY-8**
- **Install terraform and set up working environment**
  ```
  # Install the `gnupg`, `software-properties-common` and `curl` for. We will see these packages to verify Hshicorp GPG signature and install Hashicorp debian package repository

  sudo apt-get update && sudo apt-get install -y gnupg software-properties-common

  # Install the Hashicorp GPG key

  wget -O- https://apt.releases.hashicorp.com/gpg | \
  gpg --dearmor | \
  sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null

  # Verify the key's fingerprint and The `gpg` command will report the key fingerprint 

  gpg --no-default-keyring \
  --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
  --fingerprint

  # Add the Official Hashicorp repository to our system

    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
    https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
    sudo tee /etc/apt/sources.list.d/hashicorp.list

  # Update and install the terraform the new repository

    sudo apt update
    sudo apt-get install terraform
  
  ```



- **Create a basic terraform configuration to provision a simple resource and write a terraform configuration file using a provider**
**
  **provider.tf**
```
    terraform {
      required_providers {
        aws = {
          source  = "hashicorp/aws"
          version = "~> 4.16"
        }
      } 

      required_version = ">= 1.2.0"
   }

    provider "aws" {
      region = "us-west-2"
    }

  ```
   **main.tf**
  ```
   #Create a security group to allow SSH, HTTP, and HTTPS access   
    resource "aws_security_group" "allow_ssh_http_https" {
    name        = "allow_ssh_http_https"
    description = "Allow SSH, HTTP, and HTTPS access"

    ingress {
      from_port   = 22
      to_port     = 22
      protocol    = "tcp"
      cidr_blocks = ["0.0.0.0/0"] # Open to the anyone
    }

    ingress {
      from_port   = 80
      to_port     = 80
      protocol    = "tcp"
      cidr_blocks = ["0.0.0.0/0"] # Open to the anyone
    }

    ingress {
      from_port   = 443
      to_port     = 443
      protocol    = "tcp"
      cidr_blocks = ["0.0.0.0/0"] # Open to anyone
    }

    egress {
      from_port   = 0
      to_port     = 0
      protocol    = "-1" # All traffic
      cidr_blocks = ["0.0.0.0/0"]
    }
  }

    #Create an EC2 instance
    resource "aws_instance" "example" {
      ami           = "ami-05134c8ef96964280"
      instance_type = "t2.micro"
      #Associate the security group
      vpc_security_group_ids = [aws_security_group.allow_ssh_http_https.id]
      tags = {
        Name = "test-1"
      }
  }
```





- **Intialize and apply the configuration to provision resources** 
  - intialize
  ![alt text](<Screenshot 2024-09-29 145505.png>)

  - Format terraform configuration files using `terraform fmt` command
    ![alt text](<Screenshot 2024-09-29 151128.png>)
  
  - Check the script is valid or not using `terraform validate` command
    ![alt text](<Screenshot 2024-09-29 150854.png>)

  - To see the execution plan of resources using `terraform plan` command
    ![alt text](<Screenshot 2024-09-29 145932.png>)

--------------------------------------------------------------------------------------------------------------------

## **DAY-9,10**

## **Create Resources with Terraform**

- **Terraform State file**
Used to store the resource information which is created by terraform to track the resource activities in real time entire resource info is on state file. We need to keep it safe if we lost this file we cant track the infra.
  ![alt text](<Screenshot 2024-09-29 162401.png>)
  ![alt text](<Screenshot 2024-09-29 162418.png>)

- **Terraform import**
  Used to import and track the resources which is created manually.

- **Terraform taint**
  Used to recreate specific objects in real time some resource we need to recrete if it will not work properly 
then we can use taint concetp.

- **Prevent_destroy** 
   Used to keep secure our resources without destroying.

- **Terraform local**
  Its a block used to define the values. We can define the vaule once and used it for multiple times.

- **Terraform workspace**
  Where we write the code and execute operations. It is used to isolate the env in real time all the works we do on workspaces only. If we perform an operation on one workspace it wont affect another workspace.

  **Commands**
  `terraform workspace list	:`         to list workspaces
  `terraform workspace new dev	:`     to create a new workspace	
  `terraform workspace show	:`         to show current workspace
  `terraform workspace select prod	:` to switch the workspaces
  `terraform workspace delete prod	:` to delete the workspaces

- **Terraform graph** 
  Used to show the flow chart of our infra

- **Ignore changes**
  It will not replicate the changes we have done to server

- **Depends on** 
  It will depend on another resource to create


- **Terraform refresh** Used to refresh and replicate the changes to state file it will compare terraform state file with resource if it is exsits it will show, otherwise it will not show.



- **Terraform backend setup**
  When we create infra the information of resources will store on state file so it will be tracking the infra information, So we need to take backup of that file. If we lost that file we cant track the infra so we prefer to locate the state file on remote loaction.
  here im using s3 as remote backend.
  **Note:** while using new block always we need to run terraform init otherwise, plugins will not be downloaded
  after removing backend setup run this command:
  `terraform init -migrate-state`

```
  provider "aws" {
  region = "ap-south-1"
  }

  terraform {
    backend "s3" {
      bucket = "testaprodbcuket0088"
      key    = "prod/terraform.tfstate"
      region = "us-west-2"
    }
  }

  resource "aws_instance" "test" {
    ami = "ami-06006e8b065b5bd46"
    instance_type = "t2.micro"
    tags = {
      Name = "demo"
    }
  }
```

#### **Exercises for Day-9,10**

- **Create multiple resources using terraform**

  - Created vpc, subnets, route tables, internet gateway, nat gateway, security groups, ec2

    **provider.tf**
    ```
    terraform {
      required_providers {
        aws = {
          source  = "hashicorp/aws"
          version = "5.43.0"
        }
      }
    }

    provider "aws" {
      region = var.region
    }
    ```
   **main.tf**
  ```
    resource "aws_vpc" "test-vpc" {
      cidr_block = var.vpc_cidr
      tags = {
        Name = "test-vpc"
      }
    }

    resource "aws_subnet" "private-subnet-1" {
      vpc_id            = aws_vpc.test-vpc.id
      cidr_block        = var.private_subnet_cidr
      availability_zone = element(var.availability_zone, 0)
        tags = {
          Name = "private-subnet-1"
        }
    }

    resource "aws_subnet" "public-subnet-1" {
      vpc_id            = aws_vpc.test-vpc.id
      cidr_block        = var.public_subnet_cidr
      availability_zone = element(var.availability_zone, 1)
      tags = {
        Name = "public-subnet-1"
      }
    }

    resource "aws_internet_gateway" "test-igw" {
      vpc_id = aws_vpc.test-vpc.id
      tags = {
        Name = "test-vpc-IGW"
      }
    }

    resource "aws_route_table" "public-route-table" {
      vpc_id = aws_vpc.test-vpc.id
      tags = {
        Name = "public-route-table"
      }
    }

    resource "aws_route" "public-route" {
      route_table_id         = aws_route_table.public-route-table.id
      destination_cidr_block = "0.0.0.0/0"
      gateway_id             = aws_internet_gateway.test-igw.id
    }

    resource "aws_route_table_association" "public-subnet-1-association" {
      subnet_id      = aws_subnet.public-subnet-1.id
      route_table_id = aws_route_table.public-route-table.id
    }

    resource "aws_eip" "nat-eip" {
      vpc = true
      tags = {
        Name = "nat-eip"
      }
    }

    resource "aws_nat_gateway" "nat-gateway" {
      allocation_id = aws_eip.nat-eip.id
      subnet_id     = aws_subnet.public-subnet-1.id
      tags = {
        Name = "nat-gateway"
      }
    }

    resource "aws_security_group" "web-sg" {
      vpc_id = aws_vpc.test-vpc.id
      name   = "web-sg"

      ingress {
        from_port   = 80
        to_port     = 80
        protocol    = "tcp"
        cidr_blocks = ["0.0.0.0/0"]
      }

      egress {
        from_port   = 0
        to_port     = 0
        protocol    = "-1"
        cidr_blocks = ["0.0.0.0/0"]
      }

      tags = {
        Name = "web-sg"
       }
     }

    resource "aws_security_group" "db-sg" {
      vpc_id = aws_vpc.test-vpc.id
      name   = "db-sg"
      ingress {
        from_port   = 3306
        to_port     = 3306
        protocol    = "tcp"
        cidr_blocks = ["10.0.1.0/24", "10.0.2.0/24"]
      }

      egress {
        from_port   = 0
        to_port     = 0
        protocol    = "-1"
        cidr_blocks = ["0.0.0.0/0"]
      }

        tags = {
          Name = "db-sg"
        }
      }

    resource "aws_instance" "private-instance" {
      ami           = var.ami_private
      instance_type = "t2.micro"
      subnet_id     = aws_subnet.private-subnet-1.id
      tags = {
        Name = "private-instance"
      }
    }

    resource "aws_instance" "public-instance" {
      ami             = var.ami_public
      instance_type   = "t2.micro"
      subnet_id       = aws_subnet.public-subnet-1.id
      security_groups = [aws_security_group.web-sg.name] # Attach the security group
      tags = {
        Name = "public-instance"
      }
    }
  ```
 **variable.tf**
  ```
    variable "region" {
      description = "The AWS region to deploy to"
      default     = "us-west-1" # Change as needed
    }

    variable "vpc_cidr" {
      description = "CIDR block for the VPC"
      default     = "10.0.0.0/16"
    }

    variable "private_subnet_cidr" {
      description = "CIDR block for the private subnet"
      default     = "10.0.1.0/24" 
    }

    variable "public_subnet_cidr" {
      description = "CIDR block for the public subnet"
      default     = "10.0.2.0/24"
    }

    variable "ami_public" {
      description = "AMI ID for the public instance"
      default     = "ami-09fd16644beea3565" 
    }

    variable "ami_private" {
      description = "AMI ID for the private instance"
      default     = "ami-00aa9d3df94c6c354"
    }

    variable "availability_zone" {
      description = "Availability zone for subnets"
      type        = list(string)
      default     = ["us-west-2a", "us-west-2b"]
    }
  ```
- **Inspect and manage the state file**
![alt text](<Screenshot 2024-09-29 162401-1.png>)
![alt text](<Screenshot 2024-09-29 162418-1.png>)

--------------------------------------------------------------------------------------------------------

## **DAY-11,12**

## <center>**Terrafor modules**</center>

###### **What is terraform module**
Used to divide the terrafrom code to multiple folders it makes our work easy and flexiblue, it can be reusable


--------------------------------------------------------------------------------------------------------

## **Day-13**

## <center>**Introduction to ansible**</center>
- Its a free and open-source tool its an it engine that automates from server creation to deployment.
  It is also called a configuration management tool. 
  configuration: cpu, memory and os
  management: update, delete, install ----
- Ansible invented by Maichel dehaan in 2012 ansible is taken by RedHat. We have both free and paid versions of ansible it is platform independent. Ansible works with YAML language, ansible dependency is Python. GUI for ansible is Ansible-Tower.

##### **Ansible use cases**
- **Configuration Management** Ansible can be used to automate the configuration of servers and network devices, ensuring that systems are set up and maintained according to a defined and consistent configuration.
- **Software Deployment** Automate the deployment and installation of software and applications across multiple servers or devices.
- **Server Provisioning** Ansible can automate the entire process, from creating virtual machines to configuring them.
- **Continuous Integration and Continuous Deployment (CI/CD)** Ansible can be integrated into CI/CD pipelines to automate the building, testing, and deployment of applications.
- **Security and Compliance Automation** Implement security policies and compliance standards across your infrastructure by using Ansible to enforce security configurations, scan for vulnerabilities, and look over system settings.

##### **How ansible works**
- Architecture: 
  - `ANSIBLE SERVER` used to communicate with worker nodes and install pkgs, deployment
  - `WORKER NODES` takes commands from ansible server and works according to it
  - `INVENTORY` conatains info about worker nodes and group. List of nodes and their information
  - `PLAYBOOK` conatins the code which is used to perform action.

#### **EXERCISES FOR DAY-13**

- **Install Ansible and create a simple inventory file**
- **Run ad-hoc commands to check connectivity with remote server**

--------------------------------------------------------------------------------------------------------

## **DAY-14**

## <center>**Ansible configuration and Inventory management**</center>

###### **ad-hoc commands**
- These are simple linux comands used for temp works these commands will be over rided.
- This uses the following structure and it is used for non repetitive tasks
  `ansible -m "<module-name>" -a "<arguments>" <where>`

###### **Types of inventory files**
- Inventory is collection of nodes 
- Inventory is two types
  - Static
  - Dynamic
- Inventory written in two formats
  - ini formats
  - yaml format

  - **ini format example**
    ```
    ipaddress/name

    [group1]
    ipaddress/name
    ipaddress/name

    [group2]
    ipaddress/name
    ipaddress/name
    ```
  - **yaml format example**
    ```
    ---
    local:
      hosts:
        172.31.30.90:
    nodes:
      hosts:
        172.31.17.52:
        172.31.23.151:
    ubuntu:
      hosts:
        172.31.17.52:
        172.31.30.90:
    redhat:
      hosts:
        172.31.23.151:
    ```

##### **EXERCISES FOR DAY-14**
- **Set up and customize your `ansible.cfg` file**
- **Use different ansible inventories**
- **Use ad-hoc commands to gather information from remote servers**

--------------------------------------------------------------------------------------------------------

## **DAY-15**

## <center>**Writing Your First Ansible Playbook**

###### **YAML format**
- This is data representation language which uses name values
  `<name>: <value>`
- YAML is inspired from python, so indentation’s become mandatory
- YAML files generally have .yaml or .yml as extensions

###### **Ansible playbook**
- Playbook is a collection of modules we can execute multiple modules at same time.We can reuse the playbook.
- playbook will be written on YAML language.

##### **EXERCISES FOR DAY-15**

- **Create a playbook to install and configure a package on remote servers**

- **Run the playbook and verify the results**

--------------------------------------------------------------------------------------------------------

## **DAY-16**

## **Working with Variables and Templates**
Ansible uses variables to manage differences between systems. With Ansible, you can execute tasks and playbooks on multiple different systems with a single command. To represent the variations among those different systems, you can create variables with standard YAML syntax, including lists and dictionaries. You can define these variables in your playbooks, in your inventory, in reusable files or roles, or at the command line.

###### **Using variables in ansible playbooks**

###### **Managing configurations with Jinja2 templates**
- **jinja template**
  Used to get the customized op, here its a text file which can extract the variables and these values will change as per time

###### **Organizing playbooks with roles**
- **Roles**
  Used to divide the playbook into directory structures we can organize the playbooks, we can encapsulate the data and we can reduce the playbook length.
  ```
  .
    ├── master.yml
    └── roles
        ├── file
        │   └── tasks
        │       └── main.yml
        ├── one
        │   └── tasks
        │       └── main.yml
        └── sai
            └── tasks
                └── main.yml
  ```

# LINUX COMMAND LINE CHEAT SHEET

# 1 - SYSTEM INFORMATION

## uname -a
    Display Linux system information
    
    e.g:Linux dell-Inspiron-15-3515 6.5.0-26-generic #26~22.04.1-Ubuntu SMP PREEMPT_DYNAMIC Tue Mar 12 10:22:43 UTC 2 x86_64 x86_64 x86_64 GNU/Linux
## uname -r
    Display kernel release information
    
    e.g:6.5.0-26-generic
## lsb_release -a
    Show which version of ubuntu installed
    
    e.g:No LSB modules are available.  
    Distributor ID:	Ubuntu  
    Description:	Ubuntu 22.04.4 LTS  
    Release:	22.04
    Codename:	jammy

 ## uptime
    Show how long the system has been running + load    

    e.g: 12:43:57 up  2:10,  1 user,  load average: 0.86, 0.58, 0.54


## hostname
    Show system host name   

    e.g: dell-Inspiron-15-3515


## hostname -I
    Display the IP addresses of the host

    e.g:192.168.1.39 2402:e280:3e72:338:816a:d70e:6577:3a14 2402:e280:3e72:338:1a60:9d0b:dee2:887b 


## last reboot
    Show system reboot history

    e.g:
reboot   system boot  6.5.0-26-generic Wed Apr 10 10:33   still running
reboot   system boot  6.5.0-26-generic Mon Apr  8 14:51 - 18:49  (03:58)
reboot   system boot  6.5.0-26-generic Mon Apr  8 10:01 - 14:03  (04:02)
reboot   system boot  6.5.0-26-generic Sun Apr  7 16:24 - 10:00  (17:36)
reboot   system boot  6.5.0-26-generic Sat Apr  6 11:10 - 18:39  (07:28)
reboot   system boot  6.5.0-26-generic Fri Apr  5 09:58 - 11:10 (1+01:12)
reboot   system boot  6.5.0-26-generic Thu Apr  4 10:04 - 18:39  (08:34)
reboot   system boot  6.5.0-26-generic Wed Apr  3 22:09 - 23:52  (01:42)
reboot   system boot  6.5.0-26-generic Wed Apr  3 10:06 - 19:09  (09:03)
reboot   system boot  6.5.0-26-generic Tue Apr  2 17:08 - 18:46  (01:37)
reboot   system boot  6.5.0-26-generic Tue Apr  2 09:58 - 17:08  (07:09)
reboot   system boot  6.5.0-26-generic Mon Apr  1 10:11 - 23:48  (13:36)
reboot   system boot  6.5.0-26-generic Sat Mar 30 17:20 - 18:05  (00:44)
reboot   system boot  6.5.0-26-generic Sat Mar 30 10:08 - 17:20  (07:11)
reboot   system boot  6.5.0-26-generic Thu Mar 28 21:25 - 22:45 (1+01:19)
reboot   system boot  6.5.0-18-generic Fri Mar 29 05:44 - 18:59  (-10:45)
reboot   system boot  6.5.0-18-generic Fri Mar 29 05:41 - 05:44  (00:02)

wtmp begins Fri Mar 29 05:41:40 2024


## date
   Show the current date and time

    e.g:Wednesday 10 April 2024 12:58:21 PM IST


## cal
   Show this month's calendar
    e.g:April 2024       
Su Mo Tu We Th Fr Sa  
    1  2  3  4  5  6  
 7  8  9 10 11 12 13  
14 15 16 17 18 19 20  
21 22 23 24 25 26 27  
28 29 30          
 

## w
   Display who is online

    e.g: 13:00:36 up  2:27,  1 user,  load average: 1.04, 0.86, 0.61
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
malik    tty2     tty2             10:34    2:27m  0.06s  0.05s /usr/libexec/gn


## whoami
   Who you are logged in as

    e.g: malik

# 2 - FILE AND DIRECTORY COMMANDS

## ls -al
   List all files in a long listing (detailed) format

## pwd
    Display the present working directory

    e.g:/home/malik

 
## mkdir directoryname
    Create a directory

    e.g: mkdir linux1 this will create new directory as linux1

## rm file
   Remove (delete) file

   e.g: rm 1.txt this will remove 1.txt file 


## rm -r directory
   Remove the directory and its contents recursively


## rm -f file
   Force removal of file without prompting for
   confirmation



## rm -rf directory
   Forcefully remove directory recursively


## rmdir
   Delete a file or files


## cp file1 file2
   Copy file1 to file2

   e.g: When you run the command cp file1 file2, it will copy the contents of file1 into a new file named file2. If file2 already exists, it will be overwritten with the contents of file1. If file2 does not exist, a new file named file2 will be created with the contents of file1.

## cp -r source_directory destination
     cp -r source_dir dest_dir
  

   e.g: This command will recursively copy all files and directories from source_dir to dest_dir, including subdirectories and their contents. If dest_dir does not exist, it will be created. If it already exists, the contents of source_dir will be copied into it, potentially overwriting any existing files with the same names.



## mv file1 file2
   Rename or move file1 to file2. If file2 is an existing
   directory, move file1 into directory file2
    
   
# 3 - USER INFORMATION AND MANAGEMENT


## id
    Display the user and group ids of your
    current user.
    
    e.g:uid=1000(malik) gid=1000(malik) groups=1000(malik),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),135(lxd),136(sambashare)


## last
    Display the last users who have logged onto the system.
    
    

## who
    Show who is logged into the system.
    


## groupadd test
    Create a group named "test".
    
    e.g:The groupadd command in Linux is used to create a new group on the system. When you run the command groupadd test, it creates a new group named "test".

## useradd -c "John Smith" -m john
    Create an account named john, with a
    comment of "John Smith" and create the user's home
    directory.
    

## userdel john
    Delete the john account.


## usermod -aG sales john
    Add the john account to the sales group


# 4 - FILE PERMISSIONS


##  chmod 
   The chmod command is used to change the permissions of a file or directory. You can use symbolic or numeric mode to specify the permissions to be changed.

    
    e.g:chmod u+x file.txt
    This command grants execute permission to the file file.txt for the file owner (user).


##  chown 
   The chown command is used to change the owner and group of a file or directory.

    
    e.g:chown user:group file.txt
    This command changes the owner of file.txt to user and the group to  group.


##  chgrp 
   The chgrp command is used to change the group ownership of a file or directory.

    
    e.g:chgrp group file.txt
    This command changes the group ownership of file.txt to group.



##  umask 
   The umask command is used to set the default permissions for newly created files and directories.
 
    e.g:umask 022
    This command sets the default permissions for newly created files to 644 (readable and writable for the owner, readable for the group and others) and for directories to 755 (readable, writable, and executable for the owner, readable and executable for the group and others).


##  getfacl 
    The getfacl command is used to display the Access Control Lists (ACLs) for files and directories. 

    e.g:getfacl file.txt

    This command displays the ACLs for the file file.txt, including any additional permissions beyond the traditional Unix permissions.


# 5 - NETWORKING



## ifconfig -a
    Display all network interfaces and ip address
    
    e.g:The command ifconfig -a is used to display information about all network interfaces, including those that are currently down, on a Linux system. It provides detailed information about each network interface, such as its IP address, MAC address, network mask, and more.


## ifconfig eth0
    Display eth0 address and details
    
    e.g:The command ifconfig eth0 is used to display detailed information about a specific network interface named eth0 on a Linux system.


## ping host
    Send ICMP echo request to host
    
    e.g:This command sends ICMP echo request packets to the specified host and waits for ICMP echo reply packets. It measures the round-trip time (RTT) between the source and destination and reports any packet loss.

## whois domain
    Display whois information for domain
    
    e.g:This command will query the WHOIS database and retrieve registration information for the specified domain name, including details such as the domain registrar, registration status, registration date, expiration date, and contact information for the domain owner.



## whois domain
    Display whois information for domain
    
    e.g:This command will query the WHOIS database and retrieve registration information for the specified domain name, including details such as the domain registrar, registration status, registration date, expiration date, and contact information for the domain owner.


# 6 - ARCHIVES (TAR FILES)


## tar cf archive.tar directory
    Create tar named archive .tar containing
    directory.
    
    e.g:The command tar cf archive.tar directory is used to create a tar archive named archive.tar containing the contents of the specified directory.


## tar xf archive.tar
    Extract the contents from archive.tar. tar czf
    
    e.g:When you run tar xf archive.tar, it will extract the contents of the archive.tar file into the current directory. The extracted files and directories will be created in the current directory, preserving their original paths and permissions.



## archive.tar.gz directory
    Create a gzip compressed tar file name
    archive.tar.gz
    
    e.g:To create a compressed tar archive (also known as a tarball) of a directory using the tar command and gzip compression, and name it archive.tar.gz,


## tar xzf archive.tar.gz
    Extract a gzip compressed tar file.
    
    e.g:The command tar xzf archive.tar.gz is used to extract the contents of a compressed tar archive named archive.tar.gz



## tar cjf archive.tar.bz2 directory
    Create a tar file with bzip2 compression
    
    e.g:The command tar cjf archive.tar.bz2 directory is used to create a compressed tar archive (tarball) with bzip2 compression


## tar xjf archive.tar.bz2
    Extract a bzip2 compressed tar file.
    
    e.g:When you run tar xjf archive.tar.bz2, it will extract the contents of the archive.tar.bz2 file into the current directory. The extracted files and directories will be created in the current directory, preserving their original paths and permissions.


# 7 - INSTALLING PACKAGES FOR UBUNTU


## apt search keyword
    To search for packages containing a specific keyword on Ubuntu using apt, you can use the apt search command.
    
    e.g:apt search 'nginx'
    This will search for packages whose names start with "nginx".



## sudo apt install package_name

    To install a package on Ubuntu using apt
    
    e.g:sudo apt install vim
    used to install the vim text editor.



## apt show package_name

    To get information about a package using apt.
    
    e.g:apt show vim
    to get information about the vim text editor package



## sudo apt remove package_name

    To remove a package on Ubuntu.
    
    e.g:sudo apt remove vim
    to remove the vim text editor package
    


## sudo apt remove package_name

    To remove a package on Ubuntu.
    
    e.g:sudo apt remove vim
    to remove the vim text editor package


# 8 - SEARCH


## grep pattern file
    Search for patternin file.
    
    e.g:grep example text.txt
    if you want to search for the word "example" in a file named text.txt, Above command will display all lines in text.txt that contain the word "example".


## grep -r pattern directory
    Search recursively for pattern in directory
    
    e.g:grep -r example ~/documents
    if you want to search for the word "example" in all files within the directory ~/documents,This command will recursively search for the pattern "example" in all files within the ~/documents directory and its subdirectories, and display the lines where the pattern is found


## locate name
    Find files and directories by name
    
    e.g:locate example.txt
    to search for files or directories with the name "example.txt" By default, locate searches for matches of name anywhere in the filesystem. It's important to note that locate relies on a database that is updated periodically (typically daily) by a system cron job. If you've just created or modified a file, it may not immediately appear in the locate results until the next database update.



## find /path/ -name 'prefix*'

    The find command is used to search for files and directories in a directory hierarchy based on various criteria.



## find /path/ -size +100M
    
    Searches for files within the /path/ directory (and its subdirectories) that are larger than 100 megabytes.



# 9 - SSH LOGINS


## ssh host
    Connect to hostas your local username.
    
    e.g:if you want to connect to a machine with the hostname example.com: ssh john@example.com

    If you want to connect using an IP address instead of a hostname, you would use: ssh john@192.168.1.100



## ssh -p port user@host
    If the remote SSH server is running on a port other than the default port 22, you can specify the port using the -p option. 
    
    e.g:if you want to connect to a machine with the hostname example.com: ssh -p 2222 john@example.com

    If you want to connect using an IP address instead of a hostname, you would use: ssh -p 2222 john@192.168.1.100



# 10 - DIRECTORY NAVIGATION


## cd /path/to/directory

    cd: Stands for "change directory." To navigate to a specific directory we use above command

## cd ~

    cd: Stands for "change directory." To navigate to the home directory we use above command


## cd ..

    cd: Stands for "change directory." To navigate up one directory level (to the parent directory), we use above command

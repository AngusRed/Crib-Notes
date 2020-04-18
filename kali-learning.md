ls = See files  
-a = Include hidden/all  
cd = Change Directory  
cp = move, remove or copy file or directory  

-a - all (Reveals hidden files prefixed with " . ")  
-R - Recursive  
X = right to execute  
ps aux - Process list  
PID - Process Identifier  
TERM - gracefully stops a .exe  
KILL - force kill .exe  

pwd = print working directory  
editor = opens editor  
CTRL = Up Arrow  

echo (Creates a file) ($ echo "Kali rules!" > kali.rules.txt)  
************ > replaces >> adds below previous ************  
cat - reveals contents of a file in cli  
find = find  
"hosts*" - The " * " makes a search wildcard  

chown - Change Owner  
chgrp - Change Group  
chmod - Change Rights  

setuid = Set super user id  
setgid = Set rights to group files in a set directory  
sticky = a permission that is only useful in directories  

umask = restrict permissions on newly created files  

~/.bash_profile), it will effectively change the default mask for your
work sessions.  

free = free command displays information on memory  
df = disk free (df) reports on the available disk space  
-h = option (for human readable) converts the sizes into a more legible unit  
-m = mebibytes  
-g = gigibytes  

id = identity of the user running the session  
uname -a  = returns a single line documenting the kernel name (Linux), the hostname, the kernel release, the kernel version, the machine type (an architecture string such as x86_64), and the name of the operating system (GNU/Linux)
dmesg - ring buffer log  

Systemd’s journal also stores multiple logs (stdout/stderr output of daemons, syslog messages,
kernel logs) and makes it easy to query them with journalctl. Without any arguments, it just
dumps all the available logs in a chronological way.   
With the -r option, it will reverse the order so that newer messages are shown first.   
With the -f option, it will continuously print new log entries as they are appended to its database.   
The -u option can limit the messages to those emitted by a specific systemd unit (ex: journalctl -u ssh.service).  

-v =   
lsdev =    


##  RIGHTS  

u - user 
g - group  
o - others  

r - read  
w - write  
x - eXecute  

+Add Right  
-Remove Right  (Boolean)  

***Octal***  
4 for read   
2 for write  
1 for execute  

**4754**  
4= setuid (4), setgid (2), sticky (1)  

7=User  
5=Group  
4=Other  


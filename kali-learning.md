## Commonly used commands  

**Got all this from the [Kali Linux Revealed](https://www.kali.org/download-kali-linux-revealed-book/)**    
`ls` = See files  
`-a` = Include hidden/all  
`cd` = Change Directory  
`cp` = move, remove or copy file or directory  
`-E` = Gives an ASCI next the Hex

`-a` - all (Reveals hidden files prefixed with " . ")  
`-R` - Recursive  
`X` = right to execute  
`ps aux` - Process list  
`PID` - Process Identifier  
`TERM` - gracefully stops a .exe  
`KILL` - force kill .exe 
`dirb http://ip.ip.ip.ip` - Runs a scan of common sub-directories  (dirb= Directory Buster)  
`nc -nvlp 9001` - netcat listener port 9001  
n=numeric-only IP addresses, no DNS  
v=verbose [use twice to be more verbose]  
l=listen mode, for inbound connects    
p=local port number  

[https://gtfobins.github.io/](GTFO Bins)    
`find / -name *flag* -type f 2>/dev/null` - find"find cmd" / -name(Specify Name) *flag*(Wildcard "flag") -type(Specify Type) f(Specifies it is a file) 2>/dev/null (Output, 2 is standard error) Then cat the flag directories  





`pwd` = print working directory  
`editor` = opens editor  
`CTRL` = Up Arrow  

`echo` (Creates a file) (`$ echo "Kali rules!" > kali.rules.txt`)  
************ > replaces >> adds below previous ************  
`cat` - reveals contents of a file in cli  
`find` = find  
"`hosts*`" - The " `*` " makes a search wildcard  

`chown` - Change Owner  
`chgrp` - Change Group  
`chmod` - Change Rights  

`setuid` = Set super user id  
`setgid` = Set rights to group files in a set directory  
`sticky = a permission that is only useful in directories  

`umask` = restrict permissions on newly created files  

`~/.bash_profile`), it will effectively change the default mask for your
work sessions.  

`free` = free command displays information on memory  
`df` = disk free (df) reports on the available disk space  
`-h` = option (for human readable) converts the sizes into a more legible unit  
`-m` = mebibytes  
`-g` = gigibytes  

`id` = identity of the user running the session  
`uname -a ` = returns a single line documenting the kernel name (Linux), the hostname, the kernel release, the kernel version, the machine type (an architecture string such as x86_64), and the name of the operating system (GNU/Linux)
`dmesg` - ring buffer log  

Systemd’s journal also stores multiple logs (stdout/stderr output of daemons, syslog messages,
kernel logs) and makes it easy to query them with journalctl. Without any arguments, it just
dumps all the available logs in a chronological way.   
With the `-r` option, it will reverse the order so that newer messages are shown first.   
With the `-f` option, it will continuously print new log entries as they are appended to its database.   
The `-u` option can limit the messages to those emitted by a specific systemd unit (ex: `journalctl -u ssh.service`).  

`-v` =   
`lsdev` =    


##  RIGHTS  

`u` - user 
`g` - group  
`o` - others  

`r` - read  
`w` - write  
`x` - eXecute  

`+` Add Right  
`-` Remove Right  (Boolean)  

***Octal***  
`4` for read   
`2` for write  
`1` for execute  

**4754**  
`4` = setuid (`4`), setgid (`2`), sticky (`1`)  

`7` =User  
`5` =Group  
`4` =Other  
## Changing Username from Default "Kali" and your Default password "kali", also Date/Time (DTG)

The easiest way is to create a new user with `$ sudo adduser YourChoiceUsername`  

To change a username in an existing/running machine the cmd is 

`$ sudo usermod -l YourChoice kaliDefault`  This usually will return something about a process running and a number. You can run another command to kill that process but then your kali will shutdown.

Thanks to @rogan and @InitRoot From #HackSouth we now know how to change it.

Manually reboot or in your command line run  
`$ sudo reboot`  

When the reboot starts, hit `F3`, this will take you to `initroot` so basically like the bios. In there, you will run the same command as above, and it should work.  

`$ sudo usermod -l YourChoice kaliDefault`  
Once thats done run `sudo reboot`  

When you then log in use your new username. Should work! So now you are back in your kali. You need to change your root user now.  

It started with `$  kali@kali`  
Then you changed it to `$ YourChoice@kali`  
Now we want to make it `$ YourChoice@YourChoice`  

In your command line run:  

To see what your details are run `$ cat /etc/hosts`  

`$  nano /etc/hosts`  nano brings up a GUI. In there you use up/down/left/right arrows to go to the `hostname` that says kali. You will manually change it to whatever you want. Next we need to change the hostname. To test that you are half way run `$  pwd` It will take a few seconds.  

Next run `$ nano /etc/hostname` in there, change the name in the gui. To test success you can run `$  Reboot` or open a new Terminal and run `$ pwd`, this should be almost instant cause you have resolved

Next we need to change your password, this is USUALLY easier than the above. The command is:  

`$  sudo passwd`  
Enter new PW
Retype new PW
Success/Failure  

**DTG**

`$  sudo  date -s "11/20/2003 12:00:00"`





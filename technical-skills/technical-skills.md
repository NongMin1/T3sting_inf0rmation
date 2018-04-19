# Technical skills for testers
No matter whether you are working on stand-alone project or web project, operating systems and networking knowledge is must for testers. Many testing activities like installation testing, performance testing are dependent on operating system knowledge. Nowadays most of the web servers are Unix based. So Unix knowledge is mandatory for a tester.

## Unix basics
### Unix command line
For the beginners in Unix, learning basic Unix commands is a good start. 
The best way to learn Unix commands is to read and simultaneously practice them on Unix operating system (see [Linux in Windows 10](https://github.ibm.com/Balandin/test_wiki/blob/master/technical-skills/technical-skills.md#linux-in-windows-environment) and [Linux in VirtualBox](https://github.ibm.com/Balandin/test_wiki/blob/master/technical-skills/technical-skills.md#linux-in-virtual-environment)).
These are the Unix commands that are mostly used while interacting with Unix servers. Most of the time you might be interacting with Unix OS through remote windows machines using software like ‘Putty’. Read following [article](https://github.ibm.com/Balandin/test_wiki/raw/master/technical-skills/unix-basics-for-testers.doc) if you want to learn basics of Unix command line.

This [funny game](http://www.mprat.org/Terminus/) tests your command line skills, try it out when you feel ready.

[Another one](https://cmdchallenge.com) is more challenging, but still worth a try! 

### Pipes and redirects
Redirection is the transferring of standard output to some other destination, such as another program, a file or a printer, instead of the display monitor (which is its default destination). Standard output, sometimes abbreviated stdout, is the destination of the output from command line (i.e., all-text mode) programs in Unix-like operating systems. 

[Read more](http://www.westwind.com/reference/os-x/commandline/pipes.html) about pipelines and redirects.

### GUI-less text editors
When you are looking at GUI-less or headless server, you'll probably won't have other choice but to use __vi__ or __Nano__. Read a short article about these most popular text editors - 
[Vim vs. Nano](https://www.linux.com/learn/sysadmin/introduction-text-editors-get-know-nano-and-vim)

### Secure shell
Sometimes we are asked to test some kind of software in headless mode on a remote server, in such cases SSH is way to go. SSH is a network protocol for securely communicating between computers.  Often when people refer to 'using SSH', they are referring to using an SSH client to connect to another computer's SSH server in order to remotely run commands on that computer. If you are running Unix-like operating system, then you just use system terminal and connect to remote server. If you are running MS Windows, then go for [putty](https://www.putty.org). Another option is a [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about), which lets run Linux environemnt directly on Windows.

[This artice](http://blog.robertelder.org/what-is-ssh/) provides basic understanding of how  SSH is be used for remote connections, copying files between computers, tunneling services and many more.

## Windows command prompt
[Windows command prompt](https://www.cs.princeton.edu/courses/archive/spr05/cos126/cmd-prompt.html)

### Windows DOS vs. Unix commands
<details><summary><i>Command comparisson</i></summary><p>

UNIX | WINDOWS
-----|-----
cat | type, copy 
cd | cd (plus if changing drives, type the drive letter first), e.g. `C:>D:`, `D:>cd D:\test`
cp | copy, xcopy
cron | at, Task Scheduler
ftp | ftp
grep | find, findstr
ls | dir
man | help
mkdir | mkdir
more | more
mv | rename  - to rename,   move  -  actually move a file
netstat | netstat
nslookup | nslookup
ping | ping
ps | Task Manager, tasklist
pwd | cd
rm | del
rmdir | rmdir
telnet | telnet
traceroute | tracert
who | net session
</p></details>

## Virtualization
### Docker
In [this workshops](https://bolcom.github.io/docker-for-testers/) you will become familiar with the basic concepts of Docker and how you can use Docker to create isolated test environments.

### VirtualBox
Oracle VM VirtualBox  is a free and open-source hypervisor for x86 computers currently, and it's your best choice due to it's free license or prepare to pay ~$80 every year.

### VM Ware, Parallels (paid)
Workstation/Fusion is obviously the better choice, it's more stable, it's better optimized, but be ready to pay for the Pro version.
Though Parallels does not lose much to VMware, it is only for Mac users and it isn't any cheaper.

#### Linux in Windows environment
If you are running on Windows 10 x64bit version, you can use the built-in solution and install a virtual version of Ubuntu Linux from the Microsoft application store. Before starting make sure that your computer matches requirements, after that follow [the installation guide](https://docs.microsoft.com/en-us/windows/wsl/about) provided by Microsoft.

#### Linux in virtual environment
Another option is to use VirtaulBox. Before you start you will need:
<details><summary><i>show</i></summary><p>

* Virtual Box installer and Virtual Box Extension Pack [Download](https://www.virtualbox.org/wiki/Downloads)
* Ubuntu Linux distribution ISO [Download](https://www.ubuntu.com/download/desktop)

#
Download, install and run VirtualBox application.  Click __New__, select __Linux__ from dropdown menu, select Ubuntu either __32-bit__ or __64-bit__ and specify any name you like.

<img width="827" alt="createnew" src="https://media.github.ibm.com/user/57353/files/55c9b2c6-286e-11e8-8645-2d21d3430fcd">

#
Select the amount of memory (RAM) to be allocated to the virtual machine, 1024Mb should be enough.

<img width="826" alt="newharddisk" src="https://media.github.ibm.com/user/57353/files/d9b4209a-286d-11e8-9cb9-dd6bc5b027c3">

#
Add a new virtual hard disk to your machine, recommended size is 10Gb. The type of the new virtual hard disk can be left as is (VDI).

<img width="766" alt="harddisktype" src="https://media.github.ibm.com/user/57353/files/d903ec3e-286d-11e8-93a5-9e6fa2b2d4ef">

#
On the following step select __Dynamically allocated__ as the physical storage type and then click __Create__. 

<img width="827" alt="createnew" src="https://media.github.ibm.com/user/57353/files/d718352e-286d-11e8-8206-0521920ae05e">

#
The newly-created virtual machine should be listed in Oracle VM VirtualBox Manager. Though virtual machine is created, no operating system has been installed yet. 

<img width="825" alt="newvm" src="https://media.github.ibm.com/user/57353/files/da3804fa-286d-11e8-9829-9afb2785b806">

#
Click __Settings__ and select __Storage__. Here click __Empty optical drive__ as shown below, click __Choose virtual optical disk__ and select the location of the installation media (Ubuntu.iso).

<img width="646" alt="addoptical" src="https://media.github.ibm.com/user/57353/files/d667736a-286d-11e8-8a41-84c6b383057b">

#
Save Settings

<img width="647" alt="savestorage" src="https://media.github.ibm.com/user/57353/files/da8f5eb2-286d-11e8-8978-27117114d0bb">

#
Now click __Start__ and follow [Canonical's guide](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop?_ga=2.115723905.608073637.1521120793-420353266.1518886423#2).

</p></details>

## Databases
[Squirrel SQL](http://squirrel-sql.sourceforge.net)

## Networking
TODO: 

## Programming skills
See the separate [article](../programming-skills.md).
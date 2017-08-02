# LPIC-1
## Linux+ and LPIC-1: System Administrator - Exam 101
Topic 103: GNU and Unix Commands

103.1 Work on the command line

Weight: 4

Description: Candidates should be able to interact with shells and commands using the command line. The objective assumes the Bash shell.

Key Knowledge Areas:

Use single shell commands and one line command sequences to perform basic tasks on the command line
Use and modify the shell environment including defining, referencing and exporting environment variables
Use and edit command history
Invoke commands inside and outside the defined path
Terms and Utilities:

bash
echo
env
export
pwd
set
unset
man
uname
history
.bash_history
 

103.2 Process text streams using filters

Weight: 3

Description: Candidates should should be able to apply filters to text streams.

Key Knowledge Areas:

Send text files and output streams through text utility filters to modify the output using standard UNIX commands found in the GNU textutils package

Terms and Utilities:

cat
cut
expand
fmt
head
join
less
nl
od
paste
pr
sed
sort
split
tail
tr
unexpand
uniq
wc
 

103.3 Perform basic file management

Weight: 4

Description: Candidates should be able to use the basic Linux commands to manage files and directories.

Key Knowledge Areas:

Copy, move and remove files and directories individually
Copy multiple files and directories recursively
Remove files and directories recursively
Use simple and advanced wildcard specifications in commands
Using find to locate and act on files based on type, size, or time
Usage of tar, cpio and dd
Terms and Utilities:

cp
find
mkdir
mv
ls
rm
rmdir
touch
tar
cpio
dd
file
gzip
gunzip
bzip2
xz
file globbing
 

103.4 Use streams, pipes and redirects

Weight: 4

Description: Candidates should be able to redirect streams and connect them in order to efficiently process textual data. Tasks include redirecting standard input, standard output and standard error, piping the output of one command to the input of another command, using the output of one command as arguments to another command and sending output to both stdout and a file.

Key Knowledge Areas:

Redirecting standard input, standard output and standard error
Pipe the output of one command to the input of another command
Use the output of one command as arguments to another command
Send output to both stdout and a file
Terms and Utilities:

tee
xargs
 

103.5 Create, monitor and kill processes

Weight: 4

Description: Candidates should be able to perform basic process management.

Key Knowledge Areas:

Run jobs in the foreground and background
Signal a program to continue running after logout
Monitor active processes
Select and sort processes for display
Send signals to processes
Terms and Utilities:

&
bg
fg
jobs
kill
nohup
ps
top
free
uptime
pgrep
pkill
killall
screen
 

103.6 Modify process execution priorities

Weight: 2

Description: Candidates should should be able to manage process execution priorities.

Key Knowledge Areas:

Know the default priority of a job that is created
Run a program with higher or lower priority than the default
Change the priority of a running process
Terms and Utilities:

nice
ps
renice
top
 

103.7 Search text files using regular expressions

Weight: 2

Description: Candidates should be able to manipulate files and text data using regular expressions. This objective includes creating simple regular expressions containing several notational elements. It also includes using regular expression tools to perform searches through a filesystem or file content.

Key Knowledge Areas:

Create simple regular expressions containing several notational elements
Use regular expression tools to perform searches through a filesystem or file content
Terms and Utilities:

grep
egrep
fgrep
sed
regex(7)
 

103.8 Perform basic file editing operations using vi

Weight: 3

Description: Candidates should be able to edit text files using vi. This objective includes vi navigation, basic vi modes, inserting, editing, deleting, copying and finding text.

Key Knowledge Areas:

Navigate a document using vi
Use basic vi modes
Insert, edit, delete, copy and find text
Terms and Utilities:

vi
/, ?
h,j,k,l
i, o, a
c, d, p, y, dd, yy
ZZ, :w!, :q!, :e!

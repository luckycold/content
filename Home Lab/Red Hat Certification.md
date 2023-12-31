# Stuff to review:
- [ ] Manage Networking
- [ ] Install & Update Software
	- [ ] create repos
- [ ] Improve command line productivity
- [ ] Schedule future tasks
- [ ] Tune System Performance
- [ ] Controlling access to files with ACL
- [ ] Managing SELinux Security 

# Side Notes:
- ls -ltr
	- List all files with full details, the time, and in reverse order
- df
	- List file systems
- du
	- Disk usage
- df/du -h
	- Make human-readable
- wc -l
	- Word Count with -l meaning count lines
- rpm -qa
	- -q means query
	- -a means all
	- List all packages installed
- rpm -ihv /location/of/file/here
	- Install a rpm package
- rpm -e packageName
	- Remove a package
- rpm -qi
	- Information about the package
- rpm -qc
	- List config files for that package
- rpm -qf /binary/file/here
	- Get associated package name from binary
- which commandNameHere
	- Get command's binary file location
- ![[Bash Scripting]]
- grep
	- global regular expression print
	- Basic search for given text
	- Flags
		- -c
			- Keyword count
		- -i
			- Ignore case-sensitive
		- -n
			- Give line numbers
		- -v
			- Everything except given search term
- awk
	- Used for dividing lines by spaces
	- Often used with grep 
	- e.g.
		- `awk '{print $1}'`
			- Will output the first item in a line
		- `awk '{print $1}'`
			- Prints everything in the file (Essentially does `cat`)
	- Can change dividing points from spaces to something else by doing
		- `awk -F ":" '{print $1}'`
			- This converts from spaces to `:`
- cut
	- Used to cut off beginning or end of line
	- Also often used with grep
	- e.g.
		- `cut -c1-3`
			- Spits back only the first 3 characters
- egrep
	- Same as grep but allows for more than one keyword in order found in the file
	- e.g. `egrep -i "keyword|keyword2" file`
- crontab
	- Used to regularly schedule tasks
	- e.g.
		- `crontab -e`
			- Creates a crontab file that enables you to make a script for that cron
- tuned (pronounced tune-dee)
	- Used to tune Linux system performance
	- e.g.
- nice
	- Used to set user priority to certain tasks
	- e.g.
		- nice -n # process-name
- renice
	- Used to change active process priority
	- e.g.
		- renice -n # process-name
- setfacl -m u:lucky:rw /tmp/tx
	- Set user specific permission
- setfacl -b /tmp/tx
	- Resets permissions to just basic file permissions
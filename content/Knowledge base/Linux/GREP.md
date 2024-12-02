---
title: GREP
draft: false
tags:
---
 


![[Pasted image 20241203072605.png|400]]

- grep (globally search a regular expression and print)
	- very old utility, you will be hard pressed to find a linux distro that doesn't have grep. There can be variations like egrep and fgrep but you can pretty much guaranteed to have grep.
	- where `find` and `locate` will find file names across a hard drive , `grep` has the ability to search not only across a hard drive but inside of files. 
	- 
		- `man grep`
			- pulls up the manual page for grep
		- *grep can do both egrep and fgrep*
		- *a lot of distros have started doing aliases of egrep and fgrep*
		- `egrep`
			- searches for an extended regular expression
				- eg `egrep N*` will search for anything starting with N
		- `fgrep`
			- searches for a regular fixed string
				- eg `fgrep NNNNN` will search for 5 capital N's no more no less
				- on most systems `fgrep` is aliased to `grep` becoming the default, `-E` invokes `egrep`
	- `alias` will show you a list of alias's, this way you can tell how `grep` will behave on your system
	- `type egrep` will show you an alias
	- `which egrep` will show you an alias and where the binary is located
		- some systems wont have a binary for egrep opting insted to alias `grep -E`, this can also be seen with `fgrep`
	- grep can be pointed at a single file or a whole directory
		- `grep -r [search term]` will recursively search the current working directory
			- its a good idea to get in the habit of specifying where you want to search and not rely on defaults or assumptions
				- `.` current working directory
				- `..` one level above current working directory
				- `~` users home directory
				- `/` root level directory
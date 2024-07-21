:se nu 	->		extended mode - line numbers
shift + g 	->		go to last line
gg 		->		go to first line (no esc mode, just like that)
yy		->		copy line
dd		->		delete / cut
p		->		paste
n+yy	->		n is n_of lines below the current cursor position you want to copy
n+dd	->		n is n_of lines below the current cursor position you want to 
ls -l -> more detailed 
file <file_path> -> purpouse, char fmt , type
![[Pasted image 20240717135722.png]]
>_**
>"-" as the first char means text file_type
>"d" means directory
> **_

# file_type
- ## "-" :
	- text
- ## "d" :
	- directory
- ## "c" :
	- Mechanism used for i/o such as /dev files
- ## "b" :
	- block
	- /sda/ is our hard dsk
	- Storage dissks are usually Block storage type
- ## "l":
	- ![[Pasted image 20240717141146.png]]
# Links
- Instead of using a long ass path for a file like so:
	- ![[Pasted image 20240717140741.png]]
- you can link them with:
- ln -s <file_path_to_link> <link_file_name>
	- ln -> link
	- -s -> "shortcut"
	- unlink -> unlinks file & deletes shortcut file 

---

21/07/2024 Sunday 2:50pm

---
# System info
- uptime
	- free -m : memory utilization ram
	- df -h : hard-disk partition utilization

# Other
- wc -l <_file_path_> : counts lines in file
- ls | wc -l : gets output from command left to the  "|" (pipe)
	- this allows us to send commands as arguments (i imagien it is said like that xD)
-
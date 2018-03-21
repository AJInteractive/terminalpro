HOW TO BE A TERMINAL PRO - 100 COMMANDS TO KNOW
[https://code.tutsplus.com/courses/how-to-be-a-terminal-pro](https://code.tutsplus.com/courses/how-to-be-a-terminal-pro) and [https://code.tutsplus.com/courses/advanced-command-line-techniques](https://code.tutsplus.com/courses/advanced-command-line-techniques)

In the SHELL:
### hello terminal
1. echo "hello world" or with with options echo -n "hello world"
2. ctrl a and ctrl e (start and end of line)
3. Up key for previous command
4. !! for repeating previous command
5. tab and double tab
6. ~ (home directory)
7. clear
8. man echo (manual for each command)

### navigation
9. pwd (print working directory)
10. cd .. and cd folder (clear directory)
11. ls directory1 directory2 or ls -lat (list, all, time)
12. open . (open current directory)
13. open -a "Sublime Text 2" beans.txt (open beans.txt with application sublime)
14. open http:aljazeera.com/interactive (open website)
15. "file name" or file\ name (escaping spaces)
16. Drag file into terminal for path (super useful)
17. open -R file.txt (reveal)
18. killall Finder (reopen filder)

### make copy move
19. touch anewfile.txt (make a new file) or touch directory/anewfile.txt (make a new file in this directory)
20. nano afile or vim afile or vi afile
21. mkdir newdirectory
22. cp beans1.txt beans2.bak (copy a backup) or cp -r beans1 beans2 (copy recursive)
23. mv afile adirectory (rename a file) or mv afile adirectory/afilenew (move a file to a new directory)
24. mv file* adir/ (globbing)
25. cat anewfile.txt (view the contents)
26. rm santa.txt (remove it) or rm -r santa (remove and remove recursive)
27. rmdir (delete a directory) could also use rm -r (to delete a folder)
28. ln -s beans1 beans2 (soft symbolic link to point to another)
29. ln beans1 beans2 (hard shortcut link)
#### Revision up to here 28 Feb 2018
### finding files and text in files
30. find . -name "*.txt" (search current directory)
31. find . -type f (find all the files)
32. find . -iname "beans" (case insensitive file)
33. find . -size +2048 (1mb size files)
34. find . -mtime -1 (-atime -ctime) (modified, access, created)
35. find . -iname "*.txt" -or -iname "*.doc" -and mtime -1 (.doc or .txt file last modifiend one day ago)
36. find . -prune -print (only find direct children)
37. grep "hello" afile.txt (shows you which line in the code)
38. grep -ilr "hello" * (find all "hellos") (-i case insensitive -l just the files -r recursively)
39. find . -name "*.txt" -exec grep -il "Hello" {} \; (grep and find at the same time)

### finding files and text in files
40. -rw-r--r-- js staff - file, user, group, anyone else
41. drwxrwxrwx (everyone has access to read, write and execute on the directory)
42. chmod u+w (user) or chmod g+w (group) or chmod o+w (others) or chmod a+w(anyone)
43. chmod og-x afile.txt (take execution rights from othrs and from the group)
44. chmod u=rw,g=r,o=, text.txt (user can rw, group can r, others can do nothing)
45. chmod 644 text.txt (444 is equal to read for everyone)(4 read, 2 write, 1 execute)(700 user can do everything everyone else nothing)

### editing file
46. Nano poem.txt (arrow keys, control k to cut, control u to paste, control o to save file, control x to exit)
47. vim index.php (normal mode or insert mode)
48. vim NORMAL MODE (beginning gg) (shift curly brace - moves to the end of paragraph) (^ beginning of line or $ end of line) (shift colon - :set number, :syntax on, :5 (line 5), :) (shift o or shift O add a new line) (shift s - wipe out lines) (shift r - replace text) (dd - delete) (p - paste) (yy - copy) (%s/print/echo/g) (up and down arrows in :) (:w newname.php) (:wq)
49. vim INSERT MODE (you escape with esc) (u - undo ) (ctrl r - redo)
50. vim ~/.rc (type in set number, syntax on, set ignorecase)

### making tar
51. MAKING TAR FILES
	1. tar -zxvf nameoftar.tar.gz (unzip)
	2. cd nameoftar (open)
	3. ./configure (dot slash configure)
	4. make (make the files)
	5. make install (make install the files)
	6. nameoftar --version (now check it worked)

### piping-redirecting-output
52. echo "hello world" > afile.txt (append to a file >>)
53. ls fakefile 2> log (save to a log)
53. ls documents >> log  2>&1
54. translate tr a e
55. tr a e < afile.txt (replace all a's with e's in this file)
56. PIPING - ls -a | grep "\." (only find hidden files and directories)

### managing processes
57. top (sample of processes on your mac)(exit with q)
58. top -o cpu (order by CPU usage)
59. ps -cvx (c- name, x- owned by user, v- other info)(process statuses)
60. ps -cvx | grep "Google" (finds all Google processes)
61. term 35157 (quits Google Chrome)
62. kill -s KILL 35178 (force quits)

### ssh keygens
63. ssh-keygen -t rsa (creates id_rsa, id_rsa.pub, known hosts)
64. scp id_rsa.pub js@10.0.0.201:~/.ssh/authorized_keys (securely copy to the remote server)
65. login user2
66. (dont' overwrite the pubkey) cat id_rsa.pub |ssh js@10.0.1.201 "cat >> ~/.ssh/authorized_keys"
67. SSH host alias (cd .ssh, nano config, Host server, Hostname 10.1.1.1, User Haddad)

### sftp scp curl
68. scp file1.txt server:~/remote
69. sftp server
70. lpwd (locally print out my working directory)
71. put file1.txt
72. get random.txt (exit or quit)
73. curl (supports many protocols)(scrapes web pages or get files)
74. curl http://aljazeera.com > afile.html
75. curl -Of http://aljazeera.com (fail silently)

### bash scripting
76. nano .bash_profile - function helloworld(){ echo "hello, $1"}
77. SHELL SCRIPTS - nano newSite.sh (#!/bin/bash) (chmod +x newSite.sh)(./newSite.sh someexample)
78. sudo cp /usr/local/bin (super user do)
79. echo $PATH
80. alias runthis="ssh js@10.0.1.201"





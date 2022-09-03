

	All my scripts were to be exactly two lines long ($ wc -l file should print 2)
	The first line of all my files were to be exactly #!/bin/bash
		
		TASKS

0. To create a script that switches the current user to the user betty, assuming  that the user betty will exist when I run my script 
#!/bin/bash
su betty

1. To write a script that prints the effective username of the current user.
#!/bin/bash
whoami

2. To write a script that prints all the groups the current user is part of.
#!/bin/bash
groups

3. To write a script that changes the owner of the file hello to the user betty.
#!/bin/bash
chown betty hello

4. To write a script that creates an empty file called hello.
#!/bin/bash
touch hello

5. To write a script that adds execute permission to the owner of the file hello. 
The file hello will be in the working directory.
#!/bin/bash
chmod u+x hello

6. To write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello. The file hello will be in the working directory
#!/bin/bash
chmod ug+x,o+r hello

7. To write a script that adds execution permission to the owner, the group owner and the other users, to the file hello. 
The file hello will be in the working directory
I am not allowed to use commas for this script
#!/bin/bash
chmod a+x hello

8. To write a script that sets the permission to the file hello as follows:
Owner: no permission at all
Group: no permission at all
Other users: all the permissions 
#!/bin/bash
chmod 007 hello

9. To write a script that sets the mode of the file hello to this:
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
The file hello will be in the working directory
I am not allowed to use commas for this script
#!/bin/bash
chmod 753 hello

10. To write a script that sets the mode of the file hello the same as olleh’s mode
The file hello will be in the working directory
The file olleh will be in the working directory
Note: the mode of olleh will not always be 664. Make sure your script works for any mode.
#!/bin/bash
chmod --reference=olleh hello

11. To create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.
#!/bin/bash
chmod -R a+X .

12. To create a script that creates a directory called my_dir with permissions 751 in the working directory.
#!/bin/bash
mkdir -m 751 my_dir

13. To write a script that changes the group owner to school for the file hello
The file hello will be in the working directory
#!/bin/bash
chgrp school hello

14. To write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.
#!/bin/bash
chown vincent:staff *

15. To write a script that changes the owner and the group owner of _hello to vincent and staff respectively.
The file _hello to be in the working directory
The file _hello to be a symbolic link
#!/bin/bash
chown -h vincent:staff _hello

16. To write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.
The file hello will be in the working directory
#!/bin/bash
chown --from=guillaume betty hello

17. To write a script that will play the StarWars IV episode in the terminal. A friend helped me out with a useful link:
#!/bin/bash
telnet towel.blinkenlights.nl

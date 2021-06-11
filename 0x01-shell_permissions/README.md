# Understanding the Linux access and permissions

#### The Unix-like operating systems, such as Linux differ from other computing systems in that they are not only multitasking but also multi-user. This means that more than one user can be operating the computer at the same time. While a desktop or laptop computer only has one keyboard and monitor, it can still be used by more than one user.
  - chmod - modify file access rights
  - su - temporarily become the superuser
  - sudo - temporarily become the superuser
  - chown - change file ownership
  - chgrp - change a file's group ownership
---
On a Linux system, each file and directory is assigned access rights for the owner of the file, the members of a group of related users, and everybody else. Rights can be assigned to read a file, to write a file, and to execute a file (i.e., run the file as a program).

To see the permission settings for a file, we can use the ls command. As an example, we will look at the bash program which is located in the /bin directory:

![image](https://user-images.githubusercontent.com/52496180/121659869-324bfd00-ca4f-11eb-91af-539b8e8fad11.png)
---
### understanding missions patterns

![image](https://user-images.githubusercontent.com/52496180/121660694-f6fdfe00-ca4f-11eb-9515-c97d7ac8caa0.png)

  - r means read with a value of 4
  - w means write with a value of 2
  - x means execute with a value of 1

Octal notation method; think of the permission settings as a series of bits.

  - the first three sets of rwx is for the owner(called the user represented with u)
  - the second three sets of rwx is for the group(represented with g)
  - the first three sets of rwx is for the others(represented with o)

![image](https://user-images.githubusercontent.com/52496180/121661574-ce2a3880-ca50-11eb-856e-d80b8b0e8409.png)
---
### let's do some exercise

##### Task 0 - Create a script that switches the current user to the user betty
```
#!/bin/bash
su betty
```
##### Task 1 - Write a script that prints the effective username of the current user

```
#!/bin/bash
whoami
```
##### Task 2 - Write a script that prints all the groups the current user is part of

```
#!/bin/bash
groups
```
##### Task 3 - Write a script that changes the owner of the file hello to the user betty

```
#!/bin/bash
chown betty hello
```
##### Task 4 - Write a script that creates an empty file called hello

```
#!/bin/bash
touch hello
```
##### Task 5 - Write a script that adds execute permission to the owner of the file hello

```
#!/bin/bash
chmod u+x hello
```
##### Task 6 - Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello

```
#!/bin/bash
chmod u+x hello | chmod g+x hello | chmod o+r hello
```
##### Task 7 - Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

```
#!/bin/bash
chmod u+x hello | chmod g+x hello | chmod o+x hello
```
##### Task 8 - Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

```
#!/bin/bash
chmod 007 hello
```
##### Task 9 - Write a script that sets the mode of the file hello to this
```
#!/bin/bash
chmod 753 hello
```
##### Task 10 - Write a script that sets the mode of the file hello the same as olleh’s mode
```
#!/bin/bash
chmod --reference=olleh hello
```
##### Task 11 - Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed
```
#!/bin/bash
chmod -R +111 */

#!/bin/bash
chmod -R ugo+X ./
```
##### Task 12 - Create a script that creates a directory called dir_holberton with permissions 751 in the working directory
```
#!/bin/bash
mkdir -m751 dir_holberton

#!/bin/bash
mkdir -m 751 dir_holberton
```
##### Task 13 - Write a script that changes the group owner to holberton for the file hello
```
#!/bin/bash
chgrp holberton hello
```
##### Task 14 - Write a script that changes the owner to betty and the group owner to holberton for all the files and directories in the working directory
```
#!/bin/bash
chown -R betty . | chgrp -R holberton .

#!/bin/bash
chown -R betty:holberton 0x01-shell_permissions

#!/bin/bash
chown betty:holberton *
```
##### Task 15 - Write a script that changes the owner and the group owner of _hello to betty and holberton respectively
```
#!/bin/bash
chown -h betty:holberton _hello
```
##### Task 16 - Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume
```
#!/bin/bash

```
##### Task 17 - Write a script that will play the StarWars IV episode in the terminal
```
#!/bin/bash

```

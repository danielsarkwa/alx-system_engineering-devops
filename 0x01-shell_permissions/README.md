## Understanding the Linux access and permissions

The Unix-like operating systems, such as Linux differ from other computing systems in that they are not only multitasking but also multi-user. This means that more than one user can be operating the computer at the same time. While a desktop or laptop computer only has one keyboard and monitor, it can still be used by more than one user.
---
  - chmod - modify file access rights
  - su - temporarily become the superuser
  - sudo - temporarily become the superuser
  - chown - change file ownership
  - chgrp - change a file's group ownership
---
On a Linux system, each file and directory is assigned access rights for the owner of the file, the members of a group of related users, and everybody else. Rights can be assigned to read a file, to write a file, and to execute a file (i.e., run the file as a program).

To see the permission settings for a file, we can use the ls command. As an example, we will look at the bash program which is located in the /bin directory:

![image](https://user-images.githubusercontent.com/52496180/121659869-324bfd00-ca4f-11eb-91af-539b8e8fad11.png)

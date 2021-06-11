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

![image](https://user-images.githubusercontent.com/52496180/121661574-ce2a3880-ca50-11eb-856e-d80b8b0e8409.png)

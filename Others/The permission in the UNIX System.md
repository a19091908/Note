The permission in the UNIX system

File Access Modes
The permissions of a file are the first line of defense in the security of a Unix system. The basic building blocks of Unix permissions are the read, write, and execute permissions, which have been described below −

Read
Grants the capability to read, i.e., view the contents of the file.

Write
Grants the capability to modify, or remove the content of the file.

Execute
User with execute permissions can run a file as a program.

---------------

Directory Access Modes
Directory access modes are listed and organized in the same manner as any other file. There are a few differences that need to be mentioned −

Read
Access to a directory means that the user can read the contents. The user can look at the filenames inside the directory.

Write
Access means that the user can add or delete files from the directory.

Execute
Executing a directory doesn't really make sense, so think of this as a traverse permission.

A user must have execute access to the bin directory in order to execute the ls or the cd command.

---------------

For example: 
the file displays in the following: /home/userA/testfile

1. cp /home/userA/testfile /home/userB/testdir

If the executer is userA:
	the required permission:
	* user should have READ permission for testfile
	* user should have EXECUTE permission for /home, /home/userB, /home/userB/testdir
	* user should have WRITE permission for /home/userB/testdir

If the executer is userB:
	the required permission:
	* user should have READ permission for /home/userA
	* user should have EXECUTE permission for /home, /home/userA, /home/userA/testdir
	* user should have WRITE permission for /home/userB/testdir(user may have already had the ALL permission for the own folder)

2. The two ways above always need a lot of permissions in different files and folders, 
	so the common way to do this thing is in the following:

	As UserA: cp testfile /tmp/
	As userB: cp /tmp/testfile ~
	As userA: rm /tmp/testfile




# Permissions

#### There are three types of access restrictions:

Permission  |  Action  |    chmod option
-------|----------|----------
read    |      (view)    |  r or 4
write    |     (edit)    |  w or 2
execute   |    (execute) |  x or 1

#### There are also three types of user restrictions:

User  |  ls output
----------|-----------
owner  | -rwx------
group  | ----rwx---
other  | -------rwx

#### Folder/Directory Permissions

Permission  |  Action   |                            chmod option
------------|------------|------------
read     |     (view contents: i.e., ls command)  |    r or 4
write      |   (create or remove files from dir)    |  w or 2
execute   |    (cd into directory)                  |  x or 1

#### Numeric notation

Another method for representing Linux permissions is an octal notation as shown by `stat -c %a`. This notation consists of at least three digits. Each of the three rightmost digits represents a different component of the permissions: owner, group, and others

Each of these digits is the sum of its component bits in the binary numeral system:

Symbolic Notation   | Octal Notation  |  English
----------------|-------------------|-------
----------      |      0000          |     no permissions
---x--x--x      |      0111          |     execute
--w--w--w-      |      0222          |     write
--wx-wx-wx      |      0333          |     write execute
-r--r--r--      |      0444          |     read
-r-xr-xr-x      |      0555          |     read  execute
-rw-rw-rw-      |      0666          |     read  write
-rwxrwxrwx      |      0777          |     read. write  execute

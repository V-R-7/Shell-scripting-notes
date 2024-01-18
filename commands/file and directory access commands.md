# File & Directory Access Management commands

There are 2 commands for file and directory management,
- chmod
- chown

## chmod

The chmod command is used to change the permissions of a file or directory. 

It allows you to specify who can read, write, and execute a file or directory. 

The basic syntax of the chmod command is as follows:

```
chmod [options] mode file
```
Options:

- -c: Display a message only if changes are made.
- -f: Suppress error messages.
- -v: Be verbose, show the file's mode after changes.

Mode:

- Numeric Mode: Represented as a three-digit octal number (e.g., 755).
- Symbolic Mode: Uses symbols to represent permissions (e.g., u=rwx,go=rx).
- File: The file or directory whose permissions you want to change.

Numeric Mode:
The numeric mode consists of three digits, each representing the permission for the file owner, group members, and others. 

Each digit is a sum of the permissions:

- 4: Read (r)
- 2: Write (w)
- 1: Execute (x)

The possible values for each digit are:

- 0: No permission
- 1: Execute
- 2: Write
- 3: Write and execute
- 4: Read
- 5: Read and execute
- 6: Read and write
- 7: Read, write, and execute

Examples:

```
chmod 755 file    # Owner has read, write, and execute. Group and others have read and execute.
chmod 644 file    # Owner has read and write. Group and others have read.
chmod 600 file    # Owner has read and write. Group and others have no permission.
```

Symbolic Mode:

The symbolic mode allows you to use symbols to represent changes to permissions.

- u: Owner
- g: Group
- o: Others
- a: All (equivalent to ugo)
- +: Add permission
- -: Remove permission
- =: Set exact permission

```
chmod u+rwx file          # Add read, write, and execute permission for the owner.
chmod go-w file           # Remove write permission for group and others.
chmod a=rx file           # Set exact permission: read and execute for all.
chmod u=rw,go=rx file     # Set read and write for owner, read and execute for group and others.
chmod -R ugo+rX directory # Recursively add read and execute permissions for directories, not files.
```

## chown

The chown command is used to change the ownership of files and directories.

It allows you to specify the new owner and/or group for one or more files or directories. 

The basic syntax of the chown command is as follows:

```
chown [options] new_owner[:new_group] file...
```
Options:

- -c: Display a message only if changes are made.
- -f: Suppress error messages.
- -v: Be verbose, show the file's mode after changes.
- -R: Recursively change ownership of directories and their contents.

- new_owner: The username or user ID of the new owner.
- new_group: The group name or group ID of the new group. If not specified, the file's group remains unchanged.

Examples:

```
# files
chown new_owner file            # To change the owner of a file.
chown :new_group file           # To change the group of a file.
chown new_owner:new_group file  # To change both the owner and group of a file.

#directory
chown -R new_owner directory              # To change the owner of a directory and its contents recursively.
chown -R :new_group directory             # To change the group of a directory and its contents recursively.
chown -R new_owner:new_group directory    # To change both the owner and group of a directory and its contents recursively.
```

### Note:
- It's important to use the correct usernames or user IDs and group names or group IDs when using chown.
- The -R option is used for recursive operations, applying changes to the specified directory and its contents.
- The chown command requires superuser privileges to change ownership of files that you don't own.

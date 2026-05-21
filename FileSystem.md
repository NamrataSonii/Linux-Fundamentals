# Linux File System Commands

## `pwd`
Displays the current directory.

## `cd [directory]`
Changes into the given directory, or into the home directory when no parameter is provided.

## `ls [-alR] [file/directory]`
Displays the names and optionally the properties of files or lists the contents of a directory.

### Options
- **`-a`** : Lists hidden files/directories beginning with `.`
- **`-l`** : Long listing format. Displays permissions, user, group, timestamp, size, etc.
- **`-R`** : Displays all subdirectories recursively.

## `mkdir directory`
Creates an empty directory.

## `rmdir directory`
Deletes an empty directory.

## `cp file1 file2`
Copies `file1` to `file2`.

## `cp file1 [file2 file3] dir`
If `dir` exists, `file1`, `file2`, and `file3` are copied into `dir`.

If `dir` does not exist:
- More than two arguments → Error warning
- Two arguments → `dir` is interpreted as a file name

## `cp -r dir1 dir2`
- If `dir2` exists → `dir1` is recursively copied into `dir2`
- If `dir2` does not exist → a recursive copy of `dir1` is created and named `dir2`

## `cp -r dir1 dir2 dir3 dir4`
If `dir4` exists, `dir1`, `dir2`, and `dir3` are copied into `dir4`.

Otherwise an error warning is generated.

## `mv file1 file2`
Renames or moves files/directories.

Similar to `cp`, but the original file is removed after moving.

## `rm [-irf] file(s)/directory(ies)`
Deletes files and/or directories.

### Options
- **`-i`** : Delete only after confirmation
- **`-r`** : Recursively delete directories and subdirectories
- **`-f`** : Force deletion and suppress warnings

---

# File Permissions / Access Rights

## Permission Types

- **`r` (read)** → Permits reading file contents or listing directory contents.
- **`w` (write)** → Permits modification or deletion of files.
- **`x` (execute)** → Permits execution of programs and shell scripts.

## Access Rights

- **`u`** → Owner of the object
- **`g`** → Group owner
- **`o`** → Other users
- **`a`** → All users (`u + g + o`)

## `chmod [ugoa][+-=][rwx] file(s)/directory(ies)`

Changes access rights of files or directories.


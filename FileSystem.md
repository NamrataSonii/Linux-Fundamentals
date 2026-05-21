# Linux File System Commands

## `pwd`

Displays the current directory.

---

## `cd [directory]`

Changes into the given directory, or into the home directory when no parameter is provided.

---

## `ls [-alR] [file/directory]`

Displays the names and optionally the properties of files or lists the contents of a directory.

| Option | Description |
|--------|-------------|
| `-a` | Lists hidden files/directories beginning with `.` |
| `-l` | Long listing format — shows permissions, user, group, timestamp, size, etc. |
| `-R` | Displays all subdirectories recursively |

---

## `mkdir directory`

Creates an empty directory.

---

## `rmdir directory`

Deletes an empty directory.

---

## `cp file1 file2`

Copies `file1` to `file2`.

---

## `cp file1 [file2 file3] dir`

Copies one or more files into a directory.

```
cp file1 dir/
cp file1 file2 file3 dir/
```

- If `dir` exists → files are copied into it
- If `dir` does not exist and more than two arguments → **error**
- If `dir` does not exist and exactly two arguments → `dir` is treated as a filename

---

## `cp -r dir1 dir2`

Recursively copies a directory.

- If `dir2` **exists** → `dir1` is copied inside `dir2`
- If `dir2` **does not exist** → a copy of `dir1` is created and named `dir2`

---

## `cp -r dir1 dir2 dir3 dir4`

Copies multiple directories into a target.

- If `dir4` **exists** → `dir1`, `dir2`, and `dir3` are copied into it
- If `dir4` **does not exist** → **error**

---

## `mv file1 file2`

Renames or moves files/directories. Behaves like `cp`, but removes the original after moving.

---

## `rm [-irf] file(s)/directory(ies)`

Deletes files and/or directories.

| Option | Description |
|--------|-------------|
| `-i` | Prompt for confirmation before each deletion |
| `-r` | Recursively delete directories and their contents |
| `-f` | Force deletion; suppress warnings |

---

# File Permissions / Access Rights

## Permission Types

| Symbol | Name | Effect on files | Effect on directories |
|--------|------|-----------------|-----------------------|
| `r` | read | Read file contents | List directory contents |
| `w` | write | Modify or delete files | Create or remove files in directory |
| `x` | execute | Run programs/scripts | Enter the directory |

---

## Access Rights (Who)

| Symbol | Applies to |
|--------|------------|
| `u` | Owner of the file/directory |
| `g` | Group owner |
| `o` | Other users |
| `a` | All users (`u + g + o`) |

---

## `chmod [ugoa][+-=][rwx] file(s)/directory(ies)`

Changes the access rights of files or directories.

```bash
# Syntax
chmod [who][operator][permissions] target

# Operators
+   add permission
-   remove permission
=   set exact permission
```

**Examples:**

```bash
chmod u+x script.sh        # Give owner execute permission
chmod go-w file.txt        # Remove write from group and others
chmod a=r file.txt         # Set read-only for everyone
chmod u+rwx,go+rx dir/     # Full owner access; read+execute for others
```

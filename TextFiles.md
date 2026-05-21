# Linux Command Reference

## File Viewing

| Command | Description |
|---------|-------------|
| `cat file` | Displays the content of a file on the standard output channel |
| `more file` | View larger files page by page. Use `b` to scroll back, `q` to quit |

---

## Printing

| Command | Description |
|---------|-------------|
| `lpr -Pprintername file` | Print a file on the printer named `printername` |
| `lpq -Pprintername` | List all print jobs on `printername` with their job IDs |
| `lprm job_id` | Delete the print job with the given `job_id` from the queue |

---

## File Comparison & Timestamps

| Command | Description |
|---------|-------------|
| `diff file1 file2` | Compare two files. Produces no output if they are identical |
| `touch file` | Set the current timestamp on a file. Can also create an empty file |

---

## User & Display Utilities

| Command | Description |
|---------|-------------|
| `finger account` | Display additional info for a user account (name, project, etc.) |
| `gv file.ps` | Display PostScript files and related formats (`*.eps`, `*.pdf`) |
| `acroread file.pdf` | Display PDF files; allows simple manipulations (e.g., copy text/figures) |
| `gimp file` | Start the GIMP image editor. View, manipulate, and print images (`*.jpg`, `*.tif`, `*.png`) |

---

## File Conversion & Compression

| Command | Description |
|---------|-------------|
| `ps2pdf file.ps` | Convert a `.ps` file to `.pdf`. Output file is created automatically |
| `gzip file` | Compress a file using the Lempel-Ziv algorithm. Creates `file.gz`, removes original. ~3x compression |
| `gunzip file.gz` | Decompress a `.gz` file |

---
## Archiving with `tar`

```bash
# Create archive from directory
tar -cvf direc.tar direc

# Extract archive (restores original directory)
tar -xvf direc.tar

# Create compressed archive (gzip)
tar -zcvf direc.tgz direc

# Extract compressed archive
tar -zxvf direc.tgz
```
| Flag | Meaning |
|------|---------|
| `c` | Create archive |
| `x` | Extract archive |
| `v` | Verbose (show progress) |
| `f` | Specify filename |
| `z` | Compress/decompress via gzip |

---

## Searching Files
| Command | Description |
|---------|-------------|
| `locate expr` | List all files/directories matching the expression from the local database |
| `find path -name 'pattern'` | Recursively search for files matching a pattern |
| `grep 'text' files` | Search for text within files |

**Examples:**

```bash
# Find all .txt files starting from current directory
find . -name '*.txt'
# Search for "test" in all .f90 files in the parent directory
grep 'test' ../*.f90

# Case-insensitive search
grep -i 'test' ../*.f90
```

---

## Printing Text with `a2ps`

```bash
# Convert ASCII text to PostScript
a2ps [options] textfile

# Options
-1, -2, ..., -9    # Predefined font size and page layout
                   # e.g., -2 displays two pages side-by-side
-o output.ps       # Write output to a file
-P NAME            # Send output directly to printer NAME
```

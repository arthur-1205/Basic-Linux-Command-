
# Basic Linux command - TiDiAy


## Roadmap

- df/du command

- Add more integrations

## df/du command
## - df command

The `df` command in Linux/Unix is used to display information related to file systems about total space and available space.
`df` is an abbreviation for "disk free".

### Syntax

```
df [OPTION]... [FILE]...
```

### Some option 
|**Short Flag**|**Long Flag**|**Description**|
|:--|:--|:--|
|`-a`|`--all`|Include pseudo, duplicate, inaccessible file systems.|
|`-h`|`--human-readable`|Print sizes in powers of 1024 (e.g., 1023M).|
|`-i`|`--inodes`|List inode information instead of block usage.|
|`-t`|`--type=TYPE`|Limit listing to file systems of type `TYPE`.|
|`-T`|`--print-type`|Print file system type.|
|<center>-</center>|`--help`|Display help message and exit.|
|<center>-</center>|`--version`|Output version information and exit.|

### Examples:
1. Show available disk space

**Action:**
--- Output the available disk space and where the directory is mounted

**Details:**
--- Outputted values are not human-readable (are in bytes)

**Command:**
```
df
```
![image](https://user-images.githubusercontent.com/63574039/170960326-04e04216-7633-4ea6-828a-c04251537d11.png)

2. Show available disk space in human-readable form

**Action:**
--- Output the available disk space and where the directory is mounted

**Details:**
--- Outputted values ARE human-readable (are in GBs/MBs)

**Command:**
```
df -h
```
![image](https://user-images.githubusercontent.com/63574039/170962243-e92b3225-5b73-43b5-b1d6-fa41b32d8238.png)

3. Show available disk space for the specific file system

**Action:**
--- Output the available disk space and where the directory is mounted

**Details:**
--- Outputted values are only for the selected file system

**Command:**
```
df -hT file_system_name
```
![image](https://user-images.githubusercontent.com/63574039/170967260-b2f674ba-8558-40d6-8409-16b3b94ccbfd.png)


## - du command
The `du` command, which is short for `disk usage` lets you retrieve information about disk space usage information in a specified directory. In order to customize the output according to the information you need, this command can be paired with the appropriate options or flags.

### Examples:

1. To show the estimated size of sub-directories in the current directory:

```
du
```

2. To show the estimated size of sub-directories inside a specified directory:

```
du {PATH_TO_DIRECTORY}
```

### Syntax:

```
du [OPTION]... [FILE]...
```

### Additional Flags and their Functionalities:

*Note: This does not include an exhaustive list of options.*

|**Short Flag**   |**Long Flag**   |**Description**   |
|:---|:---|:---|
|`-a`|`--all`|Includes information for both files and directories|
|`-c`|`--total`|Provides a grand total at the end of the list of files/directories|
|`-d`|`--max-depth=N`|Provides information up to `N` levels from the directory where the command was executed|
|`-h`|`--human-readable`|Displays file size in human-readable units, not in bytes|
|`-s`|`--summarize`|Display only the total filesize instead of a list of files/directories|

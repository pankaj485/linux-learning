# 04. Getting Help

# Table Of Commands

| Command | Application |
| --- | --- |
| man <command_name> | prints documentation about the command |
| man <command_name> | prints documentation about the command |

## 01. What actually matters in these sections

| Important  | Useful  | Nice To Have |
| --- | --- | --- |
| The Man Pages | Type Command | The 7 Manual Page Sections |
| Navigating A Man Page | Which Command |  |
|  | Help Command |  |
|  |  |  |

## 02. Introducing The Manual

### man pages

- The `man pages` are short for manual pages. These are built-in documentation available on nearly all UNIX like OS
- `man pages` include information on commands and their usage
    - For example, `man ncal` will show documentation about the `ncal` command.
    - To exit, press `q`.

## 03. Navigating and Searching a Man page

- while we are on `man` page, we can navigate the up and down of pages using up and down arrow keys.

### basic shortcuts inside man page

- we can scroll forward one-page using `space` or `f`key
- we can scroll backward one-page using `b` key
- we can use `/` to search in the documentation.

## 04. Parsing Man Page Synopses

- It’s a brief summary of the command or function's interface. For commands, this shows the syntax of the command and its arguments (including options)
- example: `man ncal` gives,
    
    ```jsx
    cal [-31jy] [-A number] [-B number] [-d yyyy-mm] [[month] year]
    ```
    
    - Anything listed inside of square brackets is optional except for the command used `ncal`
    - if something is not listed inside of a square bracket, then it is considered non-optional.
    - first commands of the square brackets can be used without providing additional parameters.
    - other commands are expected to be used by the expected parameter.

## 05. Manual Sections

- The manual is broken into 8 different sections, each covering a specific topic in depth.
    1. User commands 
    2. System calls 
    3. C library functions 
    4. Special files 
    5. File forms 
    6. Games 
    7. Miscellaneous 
    8. System admin commands 
- we can search for specific keywords which belong to a specific section and then get to know about that by specifically providing num of sections.
- example:
    - `man -k cd` will give a list of sections where it is present.
        - output;
            
            ```jsx
            apt-cdrom (8)        - APT CD-ROM management utility
            cd-create-profile (1) - Color Manager Profile Creation Tool
            cd-fix-profile (1)   - Color Manager Testing Tool
            cd-it8 (1)           - Color Manager Testing Tool
            hex2hcd (1)          - Broadcom Bluetooth firmware converter
            hipercdecode (1)     - Decode a HIPERC stream into human readable form.
            mcd (1)              - change MSDOS directory
            rsyncd.conf (5)      - configuration file for rsync in daemon mode
            systemd-timesyncd (8) - Network Time Synchronization
            systemd-timesyncd.service (8) - Network Time Synchronization
            timesyncd.conf (5)   - Network Time Synchronization configuration files
            timesyncd.conf.d (5) - Network Time Synchronization configuration files
            ```
            
    - to get to a specific command, we use `man <section_number> command` as `man 1 mcd` will print the details about `mcd` command from section 1.

## 06. The Type and Which command

### Type

- It gives information on where or how the command is defined.
- There are 4 types of commands.
    1. An executable program which are compiled binary files.*(usually stored in /bin, /usr/bin, usr/local/bin)* 
    2. A built-in shell command 
    3. A shell function 
    4. An alias 
- example:
    1. `type clear` will output `clear is hashed (/usr/bin/clear)` is executable program. 
    2. `type cd` will output `cd is a shell builtin` is a built-in shell command. 

### Which

- It gives the location of the executable command

## 07. Using the help  command

- not all commands have support to the `man` like built-in shell commands
- for shell built-in commands, we use help commands
- example: `help cd`
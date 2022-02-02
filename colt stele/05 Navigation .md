# 05. Navigation

## commands

| command  | application |
| --- | --- |
| xdg-open / | open graphical file system from root directory |
| xdg-open ~ | open graphical file system from home directory  |
| pwd | prints the path of current working directory starting from the root |
| ls  | list the contents of current directory |
| ls <direcotry_path> | list the contents of passed directory |
| cd <dir_name> | move to passed directory |
| cd ../ | move back one directory above |

## 01. What actually matters in this section

- we will explore file systems and navigations.

## 02. The Root directory

- The root directory is a top-level folder. It is the starting point of the file system for the root folder. It is not having a name but just a `/` as naming.
- There is a separate directory called `root` as a sub-directory of the root directory `/` .
- the file structure in ubuntu:
    
    ![Untitled](05%20Navigation%20519fbfd5654d4e429d3a8ff7f9b2ae8e/Untitled.png)
    

## 03. The Home Directory

- `/home` contains a home folder for each user on the system. For example, my home folder is located at `/home/pank`
- Anything related to a specific user is inside of `home/dirname`
- Both root directory and home directory have their own shorthands.
- `/`: root directory
- `~`: home directory

## 04. PWD

- The command prints the working directory
- prints the path of the current working directory starting from the root

## 05. Using ls

- It prints lists of fields of the contents of a directory.

## 06. Helpful options for ls

- `ls -l` : prints in a long listing format. Shows far more information about each file/folder.
- `ls -a`: prints hidden files as well which begins with`.`
- `ls -la`: prints detailed information including hidden files which begins with`.`

## 07. Changing directories with cd

- The `cd` command is used to change the current working directory, “moving” into another directory.
- we can use `cd ../` to move to one level up directory

## 08. Relative vs Absolute paths

### Relative paths

- Relative paths are paths that specify a directory/file relative to the current directory.
- The path we use as relative is only usable from the directory level
- example: Suppose I’m in directory `pank>folder1` which has folders `f1, f2, f3` then to move to any of them by `cd f1/f2/f3`. But if I’m outside of `pank>folder1` then it can’t be done since the previous path was relative to the directory I was working with.

### Absolute paths

- Absolute paths start from the root directory `/`
- Since these paths start from the root directory it can be relevant to use from any directory from the system
- example: to go to `folder1` which is on `pank>desktop>folders`
    
    ```jsx
    cd /home/pank/desktop/folders/folder1
    ```
    

## 09. Overview of other folders

- Inside of `bin` there are binary commands like man, PWD, ls
- inside of `etc` there are configuration files and initialization scripts
- inside of `media` there are attachable media contents and configs
- inside of `var` there are logs, caches, and other related files
- inside of `root` it is accessible for superusers only. It is the home folder the superuser
- inside of  `usr` there are lots of executable files which contains files which is related to the installed programs
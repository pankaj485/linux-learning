# 06. Creating Files and Folders

## commands table

| command | application |
| --- | --- |
| touch <filename> | creates the file if not already created and if already created then changes modification for the file.  |
| file <filename/s> | Specifies the filetype of specific file type |
| mkdir <dirname/s> | creates num of directories passed with command as a parameter  |

## 01. What actually matters in this section

- `touch` and `mkdir` commands
- good and horrible file namings
- `file` command

## 02. Touch Command

- The command is used to create a new file. We can create multiple files using the touch command.
- we can create file inside of children directories using relative paths like `touch somefolder/hello.txt`
    - If the directory doesn’t exist then we can create on the go with arguments as `mkdir -p <dirname/dirname/filename>`. Here `-p` means to be a parent directory that will be created if not already existing for the file we want to create.
- example: `touch hello.txt new.txt`
- If you use touch with a file that already exists, it will simply update the access and modification dates to the current time.

## 03. Why touch is called touch

- it updates the access and modification time of each file to the current time.

## 04. Exploring File Types, Extensions, & the file command

### file

- `file <filename>` will give information about the file type
- example: `file hello.pdf` gives `hello.pdf: PDF document, version <version_number>`
- even if we change the file format extension, Linux will process information according to the file contents present on it. For example: if I edit an HTML file into .jpg and use the file command, it will still print as an HTML document.

## 05. File Names Good, Bad, & Ugly

- avoid spaces
- avoid special characters
- avoid symbols
- These can cause issues while reading files and using to type names since we need to use escaping keys in order to skip spaces.

## 06. Creating Directories With mkdir

- we can use `mkdir` to create directories. We can create multiple directories at once.
- example: `mkdir dir1 dir2`
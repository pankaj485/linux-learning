# 07. Nano

## commands table

| command (nano editor) | application |
| --- | --- |
| nano <file_name.file_format> | opens nano editor right on the terminal  |
| ctrl + o  | write out (makes the changes to the files) |
| ctrl + x | gets out of the nano editor  |
| ctrl + w  | find and replace |
| meta key(alt for windows) + $ | wrap texts inside the editor  |

## 01. What actually matters in this section

- `useful:` opening nano, nano shortcuts
- `nice to have:` configuring nano and spellcheck

## 02. Introduction to Nano

- It is a simple text editor that we can access right from the terminal. It is alternative to vim and emacs.
- It includes all the basic text editing functionalities like search, spellcheck, syntax highlighting, etc.

## 03. The basics of Nano

- to open Nano, run `nano <file_name.file_format>`
- We can also edit the file which doesn’t yet exist.

## 04. Creating File With Nano

- with nano if we try to edit a file that doesn’t exist, it will create that file and then open an editor for the file it just created.

## 05. Mastering nano shortcuts

- meta key is used for a lot of shortcuts. which is `alt` key
- all the commands are available with `ctrl + G` key while being inside on nano. It gives a huge list of shortcuts

## 06. Searching and Replacing in nano

### searching

- to search in nano, use `ctrl + w` which will open the search prompt
- search is completely case insensitive by default but it can be changed later on

### replacing

- to replace in nano, use `ctrl + \` which will open a search prompt. After submitting the content to search, replacing prompt will appear.
- On hitting enter after replacing the key, it will ask to replace for the first instance. On deciding on that the second one appears and then another and so on.
- we also get the option to replace all occurrences at once.

## 07. Configuring Nano and spellchecking

- spellcheck is disabled by default with nano
- to enable it, we need to configure file located at `/etc/nanorc`
    - with Sudo, go speller setting and uncomment by removing `#` on the line and enabling speller
- After enabling `speller` we can go and use spell checking with `ctrl + t` to start speller and follow acc to the commands.
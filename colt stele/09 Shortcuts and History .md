# 09. Shortcuts and History

## commands table

| command | application |
| --- | --- |
| ctrl + l  | clear screen  |
| ctrl + a  | move to the beginning of the line  |
| ctrl + e | move to the ending of the line  |
| ctrl + f | move one character forward(just like an arrow right key)  |
| ctrl + b | move one character backward(just like an arrow left key) |
| alt + f | move one word forward(just like a ctrl + arrow left key) |
| alt + b | move one word backward(just like a ctrl + arrow left key) |
| alt  + t  | to swap present word with a left to it  |
| ctrl + k | to kill the text from the current cursor location until the end of the line  |
| ctrl + u | to kill the text from the current cursor location to the beginning of the line  |
| alt + d | to kill the whole word from the cursor position to end of the word  |
| ctrl + d | to kill present character on cursor  |
| ctrl + w | to kill the text from the cursor to the beginning of the word |
| ctrl + y | to retrieve most recently killed text using the yanking library  |
| history  | to show the commands used previously  |
| history | less  | to show limited history with the option to expand  |
| !<index_of_command>  | to re-execute the command again  |
| ctrl + r  |  to find command acc to the keyword being passed |

## 01. What actually matters in this section

- nothing critical to know in this section
    - `useful`:
        1. clear shortcut 
        2. jump line shortcut 
        3. jump character shortcut 
        4. jump word shortcut 
        5. kill line shortcut 
        6. yank shortcut 
        7. history command 
        8. history expansion 

## 02. Clearing & Jumping Lines

- `ctrl + l` to clear screen
- `ctrl + a` to move to beginning of the line
- `ctrl + e` to move to ending of the line

## 03. Jumping Characters and Words

- `ctrl + f` to move forward one character *(just like an arrow key)*
- `ctrl + b` to move backward one character *(just like an arrow key)*
- `alt + f` to move forward one word*(just like ctrl + right arrow)*
- `alt + b` to move backward one word*(just like ctrl + left arrow)*

## 04. Swapping Characters

- `ctrl + t` to swap present character with a left to it
    - the present letter will move left and left to it char will come to the right of it
- `alt  + t` to swap present word with the left to it
    - present word will move to left and left to it will come to the right of it

## 05. Killing Lines, Words, & More

- `ctrl + k` to kill the text from the current cursor location until the end of the line
- `ctrl + u` to kill the text from the current cursor location to the beginning of the line
- `alt + d` to kill the whole word from the cursor position to end of the word
- `ctrl + d` to kill present character on cursor
- `ctrl + w` to kill the text from the cursor to the beginning of the word

## 06. Yanking From The Kill-Ring

- kill ring is the temporary zone where recently deleted commands are present.
- we can yank the commands back using the yanking method
- The concept is similar to the clipboard but is not actually
- `ctrl + y` to retrieve most recently killed text using the yanking library

## 07. History command & History expansion

- `history` to show the commands used previously
- `history | less` to show limited history with option to expand
- the command will print the commands being used with respective index of it
- `!<index_of_command>` to re-execute the command again
- `ctrl + r`  to find command acc to the keyword being passed
    - use `ctrl + r` to go to another result if one result is not what we need
    - hit `enter` to execute the command
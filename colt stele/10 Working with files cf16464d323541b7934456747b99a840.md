# 10. Working with files

## commands table

| command | application |
| --- | --- |
| cat <filename>  | will read, concat, and prints the contents of the files  |
| cat <file1> <file2>   | will concat files and prints content. order matters  |
| less <filename>  | will display the contents of the file one page at a time  |
| tac <filename>  | will print the contents of the file from the last line or in reverse order. |
| rev <filename> |  will print contents of the file, reversing the order of each line.  |
| head  | prints portion of the file starting from the beginning of the file  |
| tail |  prints portion of the file starting from the ending of the file |

## 01. What actually matters in this section

- `imoprtant`: cat, less, head, tail, sort
- `useful`: wc, fancy sort
- `nice to have`: tac, rev

## 02. The cat command

- `cat <filename>` will read, concat, and prints the contents of the files
- `cat <file1> <file2>`  will concat files and prints content. order matters

## 03. Working with less

- `cat` will concat and print all the contents of the file.
- `less <filename>` will display the contents of the file one page at a time
- we can use `f` to go forward one page, `b` to go backward one page, `/` to search for contents

## 04. Tac and Rev

### Tac

- `tac <filename>` will print contents of the file from the last line or in reverse order. It doesn’t change or module the contents of the file at all

### Rev

- `rev <filename>` will print the contents of the file, reversing the order of each line.
- Think rev as horizontal reverse and tac as vertical reverse

## 05. Head and Tail

### Head

- `head` prints portion of the file starting from the beginning of the file

### Tail

- `tail` prints portion of the file starting from the ending of the file
- we can specify nums of lines to print with `-n <Number>`  or `-<number>` option to print first or last `<Number>` lines. work with both head and tail

## 06. The WC command

- `wc` can tell us a number of words, lines, or bytes in files. By default, it prints lines, words, and bytes in a file
- use `-l` to limit the output to the number of lines and `-w` to limit num of words in a file
- example:
    
    `wc -l <filename>` gives lines only
    
    `wc -w <filename>` gives words only
    
    `wc -m <filename>` gives nums of characters 
    
    `wc -c <filename>` gives nums of bytes 
    

## 07. The sort command

- `sort <filename>` gives the output of sorted content of the file in alphabetical order
- `sort <filename> -r` gives the output of sorted content of the file in reverse alphabetical order
- `sort -n <filename>` to sort files acc to numerical order.
- use option `-u` to output unique values only

## 08. Advanced sorting by field

- we can sort any particular column using `-k` option followed by a field number.
- example: `sort -n -k3 <filename>` will sort filenames numerically acc to the fields present at column 3
-
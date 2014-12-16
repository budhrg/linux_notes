#### File and its manipulation related commands
##### File Ownership
1. `chown`
<br>Used to change user ownership of a file or directory

2. `chgrp`
<br>Used to change group ownership of file/directory

3. `chmod`
<br>*Used to change the permissions on the file which can be done separately for owner, group and the rest of the world (often named as other.)*

##### File manipulation
1. `cat`: `cat` is short for concatenate. It is often used to read and print files as well as for simply viewing file contents.
<br>To view a file, use the following command:
  - `cat file1 file2` :
  <br>Concatenate multiple files and display the output; i.e., the entire content of the first file is followed by that of the second file.
  - `cat file1 file2 > newfile`:
  <br>Combine multiple files and save the output into a new file.
  - `cat file >> existingfile`:
  <br>Append a file to the end of an existing file.
  - `cat > file`
  <br>Any subsequent lines typed will go into the file until CTRL-D is typed.
  -`cat >> file`:
  <br>Any subsequent lines are appended to the file until CTRL-D is typed.

2. `sort`: Used to rearrange the lines of a text file either in ascending or descending order, according to a sort key. You can also sort by particular fields of a file. The default sort key is the order of the ASCII characters (i.e., essentially alphabetically).
**Usage:**
  - `$ sort <filename>`: Sort the lines in the specified file
  - `$ cat file1 file2 | sort`:  Append the two files, then sort the lines and display the output on the terminal
  - `$ sort -r <filename>`: Sort the lines in reverse order
  - `$ sort -u <filename>`: Sort the lines removing duplicate lines

3. `uniq`: Used to remove duplicate lines in a text file and is useful for simplifying text display. uniq requires that the duplicate entries to be removed are consecutive. Therefore one often runs sort first and then pipes the output into uniq; if sort is passed the -u option it can do all this in one step.
**Usage**:
 - `$uniq <filename>`: Display the filename data without duplicate entries(if duplicate entries are consecutive)
 - `$ uniq -c <filename>`: Diplay the number of duplicate entries ahead of lines.

4. `paste`: Used to combine fields (such as name or phone number) from different files as well as combine lines from multiple files. For example, line one from `file1` can be combined with line one of `file2`, line two from `file1` can be combined with line two of `file2`, and so on.
**Usage**:
 - `$ paste file1 file2`: Combile fields of file1 and file2
 - `$ paste -d, file1 file2`: Use delimiter while comibining
*Common delimiter are: `tab`, `space`, `|`, `comma`, etc.

5.  `join`: Used to combine two files on a common field.<br>
**Usage**:
  `$join file1 file2` and press the Enter key<br>
*NOTE: file1 and file2 must have one common field and sorted*

6. `split`: Used to break up (or split) a file into equal-sized segments for easier viewing and manipulation, and is generally used only on relatively large files. *By default split breaks up a file into 1,000-line segments.* The original file remains unchanged, and set of new files with the same name plus an added prefix is created. *By default, the `x` prefix is added.*<br>
**Usage**:
 - `$ split <filename>`: Split file into segments
 - `$ split <filename> <prefix>`: Split a file into segments using a different prefix

7. `Regular Expressions and Search Patterns`: Regular expressions are text strings used for matching a specific pattern, or to search for a specific location, such as the start or end of a line or a word. Regular expressions can contain both normal characters or so-called `metacharacters`, such as `*` and `$`.

8. `grep`: Extensively used as a primary text searching tool. It scans files for specified patterns and can be used with regular expressions as well as simple strings.<br>
**Usage**:
 - `$ grep [pattern] <filename>`: Search for a pattern in a file and print all matching lines
 - `$ grep -v [pattern] <filename>`: Print all lines that do not match the pattern
 - `$ grep [0-9] <filename>`: Print the lines that contain the numbers 0 through 9
 - `$ grep -C 3 [pattern] <filename>`: Print context of lines (specified number of lines above and below the pattern) for matching the pattern. Here the number of lines is specified as 3.

9. `tr`: Used to translate specified characters into other characters or to delete them.<br>
**Usage**:
`$ cat <filename> | tr [options] set1 [set2]`<br>
or<br>
`$ tr [options] set1 [set2] < inputfile > outputfile`<br>
where<br>
`set1` in the example, lists the characters in the text to be replaced or removed and `set2`, lists the characters that are to be substituted for the characters listed in the first argument. `inputfile` is from what to translate and `outputfile` is where to put translated data.<br>
**Common Usages**:
 - `$ tr a-z A-Z`: Convert lower case to upper case
 - `$ tr '{}' '()' < inputfile > outputfile`  : Translate braces into parenthesis from `inputfile` into `outputfile`
 - `$ echo "This is for testing" | tr [:space:] '\t'`: Translate white-space to tabs
 - `$ echo "This   is   for    testing" | tr -s [:space:]`: Squeeze repetition of characters using `-s`
 - `$ echo "the geek stuff" | tr -d 't'`: Delete specified characters using `-d` option
 - `$ echo "my username is 432234" | tr -cd [:digit:]`: Complement the sets using -c option
 - `$ tr -cd [:print:] < file.txt`: Remove all non-printable character from a file
 - `$ tr -s '\n' ' ' < file.txt`: Join all the lines in a file into a single line.

10 . `tee`: Takes the output from any command, and while sending it to standard output, it also saves it to a file. In other words, it "tees" the output stream from the command: one stream is displayed on the standard output and the other is saved to a file.<br>
**Usage**<br>
`$ tee <newfile>`<br>
Eg:  `$ ls -l | tee newfile`

11 . `wc`:  `wc(word count)` counts the number of lines, words, and characters in a file or list of files.<br>
**Usage**:<br>
`$ wc <filename>`<br>
Options are given in the table below.<br>
*NOTE: By default all three of these options are active.*
```
Option   Action
–l     display the number of lines.
-c     display the number of bytes.
-w     display the number of words.
```

12 . `cut`: Used for manipulating column-based files and is designed to extract specific columns. The default column separator is the `tab` character. A different delimiter can be given as a command option.
<br>
Eg:  To display the third column delimited by a blank space<br>
`$ ls -l | cut -d" " -f3` and press the Enter key.

13 . `less`: View the contents of a large file, scrolling up and down page by page without the system having to place the entire file in memory before starting.<br>
**Usage**:<br>
`$ less <filename>`<br>
or<br>
`$ cat <filename> | less`

14 . `head`: Reads the first few lines of each named file (`10 by default`) and displays it on standard output. You can give a different number of lines in an option.<br>
**Usage**<br>
`$ head <filename>`<br>
Eg: If you want to print the first 5 lines from `atmtrans.txt`, use the following command:<br>
`$ head –n 5 atmtrans.txt`

15 . `tail`: Prints the last few lines of each named file and displays it on standard output. *By default, it displays the last 10 lines*. You can give a different number of lines as an option. tail is especially useful when you are troubleshooting any issue using log files as you probably want to see the most recent lines of output.<br>
**Usage**<br>
`$ tail <filename>`<br>
Eg: To display the last 15 lines of `atmtrans.txt`, use the following command:<br>
`$ tail -n 15 atmtrans.txt` or `tail -15 atmtrans.txt`<br>
**NOTE**:<br>
To continually monitor new output in a growing log file:<br>
`$ tail -f atmtrans.txt`

16 . `strings`: Used to extract all printable character strings found in the file or files given as arguments. It is useful in locating human readable content embedded in* binary files*: for text files one can just *use grep*.<br>
**Usage**:<br>
`$ strings <filename>`<br>
Eg: To search for the string `my_string` in a spreadsheet:<br>
`$ strings book1.xls | grep my_string`

17 .` The z Command Family`:
When working with compressed files many standard commands can not be used directly. For many commonly-used file and text manipulation programs there is also a version especially designed to work directly with compressed files. These associated utilities have the letter `z` prefixed to their name. For example, we have utility programs such as `zcat`, `zless`, `zdiff`, and `zgrep`.<br>
**Usage**:<br>
```
To view a compressed file
$ zcat compressed-file.txt.gz

To page through a compressed file
$ zless <filename>.gz
or
$ zmore <filename>.gz

To search inside a compressed file
$ zgrep -i less test-file.txt.gz

To compare two compressed files
$ zdiff filename1.txt.gz filename2.txt.gz
```
**Note**: *Note that if you run `zless` on an uncompressed file, it will still work and ignore the decompression stage. There are also equivalent utility programs for other compression methods besides `gzip`; i.e, we have `bzcat` and `bzless` associated with `bzip2`, and `xzcat` and `xzless` associated with `xz`.*

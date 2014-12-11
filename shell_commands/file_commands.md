#### File and its manipulation related commands
##### File Ownership
1. `chown`
<br>Used to change user ownership of a file or directory

2. `chgrp`
<br>Used to change group ownership of file/directory

3. `chmod`
<br>*Used to change the permissions on the file which can be done separately for owner, group and the rest of the world (often named as other.)*

##### File manipulation
1. `cat`:<br>
`cat` is short for concatenate. It is often used to read and print files as well as for simply viewing file contents.
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
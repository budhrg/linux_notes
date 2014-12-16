#### Basic and Shell related commands
`shell` is a command line interpreter which provides the user interface for terminal windows.

1. cat /etc/shells : List all shell

2. `echo`: Simply displays (echoes) text.
**Usage**
`$ echo <string>`
  - `$ echo <string> > <filename>`: Place the string into a file(create it if doesn't exist or overwrite)
 - `$ echo <string> >> <filename>`: Append the string to file
**NOTE**: *The `–e` option enable using escape sequence character like `\n` or `\t` for `newline` or `tab` respectively.*
  - `$echo $PATH`: Used for viewing the value of Environment variable

3. `Features of Shell scripts`:
 - Automate tasks and reduce risk of errors
 - Combining long and repetitive commands into one single command
 - Share procedures among several users
 - Quick prototyping, no need to compile
 - Create new commands using combination of utilities
 - Provide a controlled interface to users

4.  `Shell basic syntax and structures`:<br>
`#` - Used to add a comment, except when used as `\#`, or as `#!` when starting a script<br>
`\` - Used at the end of a line to indicate continuation on to the next line<br>
`;` - Used to interpret what follows as a new command<br>
`$` - Indicates what follows is a variable<br>

 - The concatenation operator (\) is used to concatenate large commands over several lines in the shell.
 - Semicolon(;) is used to put multiple commands in single line
` $ make ; make install ; make clean`
 - To abort subsequent commands if one fails
`$ make && make install && make clean`
 - Proceed until something succeeds and then you stop executing any further steps.
`$ cat file1 || cat file2 || cat file3`

5. `Function`:  A code block that implements a set of operations. Functions are useful for executing procedures multiple times perhaps with varying input variables. Functions are also often called `subroutines`. 
Using functions in scripts requires two steps:
 - Declaring a function:
`function_name () {
       command...
}`
 - Calling a function: `function_name()` <br>
**Note**: *The first argument can be referred to as `$1`, the second as `$2` and so on.*

6. `Command Substitution`: To substitute the result of a command as a portion of another command. It can be done in two ways:
 - By enclosing the inner command with backticks ``(`)``:<br>
``$ echo `ls -l```
 - By enclosing the inner command in `$( )`:<br>
`$ echo $(ls -l)`<br>
**NOTE**: `$( )` method allows command nesting `$ cd /lib/modules/$(uname -r)/`

7. `Script Parameters`: Users often need to pass parameter values to a script, such as a `filename`, `date`, etc.  Scripts will take different paths or arrive at different values according to the parameters (command arguments) that are passed to them.  These values can be text or numbers as in:
```
$ ./script.sh /tmp
$ ./script.sh 100 200
```
Within a script, the parameter or an argument is represented with a `$ and a number`
```
Parameter	           Meaning
$0	                Script name
$1	                First parameter
$2, $3, etc.	Second, third parameter, etc.
$*	                All parameters
$#	                Number of arguments
```

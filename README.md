# Linux Command Line Udemy Bootcamp

## Section 1-3: Introduction & Using the terminal

## Section 4: Getting Help
### Material
Command: man - to lookup for description for the command

Commands can tkae multiple options and inputs, some of those may be optional

Command: type - lets you see the type of a command
  Example: type clear
            clear is hashed
           type cd
             cd is a shell builti

Command: which - tells where a command is located

Command: help - for commands that are directly bulti in to the shell (that have no man pages)
Example: help cd

### Quiz
![image](https://github.com/user-attachments/assets/cffbc7ff-9fc4-4d13-b527-3677d7e7e741)
![image](https://github.com/user-attachments/assets/32d80904-7f4d-47e0-b3e8-a2f0de540c78)
![image](https://github.com/user-attachments/assets/bfb8de21-1a71-4a44-a549-2170316a3b1f)

### Exercise
Link: https://plum-poppy-0ea.notion.site/Getting-Help-Exercise-dac5ac2d63764c6180c1eb31204ba98a

- command: whoami - prints user name. doesn't need any options or arguments
- after running it, it ptinted my user name: artem
- after using man on 'who', i figured out it's a command to show who is logged in. there are optionsl options and arguemnts it seems
- 'who -b'
- type echo: ehco is a shell builtin
- type date: date is hashed

## Section 5: Navigation
### Material
Everything is located inside root directory (/), and /home contains all the users and their folders (desktop, documents etc)
/ - root
~ - home

Command: pwd - prints the current working directory (where we currently are in the window)

Command: ls - lists files/folders in the currewnt working directory
Has different optiosn, -l: long listing format, -a: do not ignore hiden directories

Command: cd - basic navigation for changing directories
Examples: 'cd Desktop', 'cd Destop/Folder'
cd .. - go to the previous directory (one dir upwards/parent dir)
. - current dir

Paths: relative and absolute
- Relative: path from the current dir
  Ex: lily/../colt/animals/cat
- Absolute: path starting from the root
  Ex: /home/colt/animals/cat

### Quiz
![image](https://github.com/user-attachments/assets/29a5c3b6-489e-4216-a899-a2a883ee2dec)
![image](https://github.com/user-attachments/assets/262f6d83-db77-4c0d-89cf-66f34c28fb0f)
![image](https://github.com/user-attachments/assets/0812f13b-7757-4923-878b-a5ebffecc600)

### Exercise
Link: https://plum-poppy-0ea.notion.site/Navigation-Exercise-cfabfffd1fc04c22a76b6e3ebb60a4ca

- cd Desktop/Farm
- cd Coop
- ls
- cd Chickens
- ls, 6 chickens
- ls -l, 4 chickens share the oldest modification date
- cd ../Geese
- ls, 4
- ls -l, Muffin because the size is 15 (bytes?)
- cd ../../Stable/Horses
- ls, 4
- ls -a, Troy
- Bonus question: ls -m, printed all the horses in a comma separated list

## Section 6: Creating Files & Folders
### MateriaL
Command: touch - used for creating files (can create with or without extensions) (technically the command was created to update modification time, but it is moslty used for creating new files)

Command: file - helps determining the file type

When deciding a name for a file/folder, there are some chars you shouldn't include in a name (, / space etc)

\ is an escape character 

Command: mkdir - create directories

### Exercise
Link: https://plum-poppy-0ea.notion.site/Making-Files-And-Folders-Exercise-5da482693b3547058be3496d60e54144
- mkdir my-app
- touch README.md package.json
- mkdir public, touch public/index.html
- mkdir src, cd src
- touch App.css App.js index.css index.js
- Bonus question: mkdir -p components/Navbar

## Section 7: Nano
### Material
Nano is a file editor, like vim (learned at school already)
To open an existing file with nano: nano book.txt
Nano is useful for creating files
Has multiple useful shortcuts

You can use spellcheck in Nano, but it is disabled by default, we can configure it by going into /etc/nanorc

## Exercise
Link: https://plum-poppy-0ea.notion.site/Nano-Exercise-a6daa37a53bd4b749f3c8f085936fc74

Part 1
- nano recipe.txt
- added my name on the line 3 after Author
- used ctrl + w to find two instances of 'Parm'
- used ctrl + O then enter, thyen ctrl + X to exit
Part 2
- nano website.html
- Alt + R, replace Ristorante Colt with Patty Slaps, replaced all 4 instances
- saved with ctrl + O and ctrl + X to exit
Part 3
- nano country-data.json
- ctrl + \ (replace) and type in line 15399, fix the spelling of the country and save the file
Bonus
- nano recipe.txt, then ctrl + r review.txt which inserted 10 lines from that file

## Section 8: Moving & Deleting
### Material
Command: rm - removes/deletes files or directories
- Example: rm script.js
- To delete folders that are empty: rm -d, or rmdir
- To remove directories and their contents recursevly: rm -r
- Add -i to prompt for a confirmation before deleting

Command: mv <source> <destination> - used for moving files/directories OR renaming
- The folder where we move things needs to be existent already
- We can move multiple source files, but to only one destination
- We can also move directories, but the destination dir needs to be existent otherwise the command will rename the dir we're trying to move
- We can also use it to rename: mv <currentname> <newname>

Command: cp <source> <destination> - used for copying files
Can aslo be used to copy directories: cp -r

### Exercise
Link: https://plum-poppy-0ea.notion.site/Deleting-Moving-Copying-Exercise-90384060a2444b88bef15f052dd6b721
Part 1
![image](https://github.com/user-attachments/assets/b0873c88-2243-4480-80e6-8912d3df385f)
Part 2
![image](https://github.com/user-attachments/assets/be3d546d-742c-44df-be0d-a664db14d744)
![image](https://github.com/user-attachments/assets/ce8caa1d-2093-4860-bf8f-98462f1c4bee)

## Section 9: Shortcuts & History
- Shortcut: ctrl + l - to clear the termianl
- Shortcut: ctrl + a - jump to the beginning of the line
- Shortcut: ctrl + e - jump to the end of the line
- Shortcut: alt+f or alt+b - move forward/backward one word at a time
- Shortcut: ctrl+t - swap the current character under the cursor with the one preceeding it
- Shortcut: ctrl+k - kill the text from the cursor location until the end of line
- Shortcut: ctrl+u - kill the text from cursor to the beginning of the line
- Shortcut: alt+d - to kill text from current cursor location till the end of word
- Shortcut: ctrl+w or alt+delete to go in the opposite direction
- Shortcut: ctrl+y - retrieve the most recent 'kill' with other commands (this is called yanking)

History - bash keeps a record of commands we previously entered. We could already scroll through history withj up and down arrows to see the commands;
But you can also use 'history' command to view the entire history, though it's generally easier with piping the output to | less
To run a command that's far in our history, we can look at the line it's at and run that 'line'
  Example: command at line 1314
          !1314

Shortcut: ctrl+r - to search through history

## Section 10: Working With Files
### Material
Command: cat <filename> - prints the contents of a file
Can also [concatinate] multiple file (prints them together): cat <file1> <file2>

Command: less - prints contets of a file one page at a time
The interface is the same as using man page: we can scroll down or go down by one page using 'space', to search for a keyword use '/'

Command: tac (cat backwards) - does what cat does in the opposite order

Command: rev - prints contest of a file reversing the order of each line

Command: head - prints a portion of a file (first 10 lines by default)
To change the number of lines: head - n 5 file.txt (prints first 5 lines) (can also just type '-' with no 'n')

Command: tail - does the same as head except starting from the end
To change the number of lines: tail - n 5 file.txt (prints first 5 lines) (can also just type '-' with no 'n')

Command: wc - tells number of word/lines in the file
wc book.txt: 4 6 33 book.txt (lines, words, bytes)
Can use multiple options for a specific number we want

Command: sort - outputs the sorted contents of a file (alphabetically by default)
Doesn't actually change the contents
-r for reverse, -n to sort nummerically, -u for unique values
-k to specify a column/field by which we want to sort

### Exercise
Link: https://plum-poppy-0ea.notion.site/Working-With-Files-Exercise-1f1136c779da4f3286e6cfb6c934d571

Part 1
![image](https://github.com/user-attachments/assets/3ca4b774-5f0e-46cb-bd42-befdfeb36ff8)
![image](https://github.com/user-attachments/assets/b39d9b5d-0253-4bf0-bad0-4d21c3b6517a)
![image](https://github.com/user-attachments/assets/b3c9af10-4cb4-47a7-a36b-6a78b2e159d5)
Part 2
![image](https://github.com/user-attachments/assets/4b6455f3-ad1f-4675-9bbb-471a28719a2e)
![image](https://github.com/user-attachments/assets/a034de11-7d5a-46a3-9ac4-ac6fc9120e8f)

## Section 11: Redirection
### Material
Standart Streams - three communication channels
- Standart Input (STDIN)
- Standart Output (STDOUT)
- Standart Error (STDERR)

Redirection describes the ways we can alter the source of standart input and the destinations of stdout and stderr
Exmaple: date > today.txt - redirects the first command into a file

Appending: with '>', any existing content in a file is overwritten
           we can use '>>' to append instead

Redirecting input: command < filename
                   cat < chickens.txt

We can do both at the same time: cat < original.txt > output.txt

Redirecting standart error: 2>

Using all together exmaple: cat bees.txt ants.txt > insects.txt 2> error.txt 
To redirect stderr to the same location as standart output: 2>&1
  Example: ls docs > output.txt 2> output.txt
           instead do:
           ls docs > output.txt 2>&1
For newer bash versions: &>

### Exercise
Link: https://plum-poppy-0ea.notion.site/Redirection-Exercise-db6cb41044434c678f59c08e824d1828

![image](https://github.com/user-attachments/assets/02405ccd-b524-4682-b0e9-5b89edde7321)
![image](https://github.com/user-attachments/assets/a99f6d62-e89f-479b-b998-c65aa1abf156)
![image](https://github.com/user-attachments/assets/3dee4f62-6e05-4f99-8c45-d9aadf3cf1da)
![image](https://github.com/user-attachments/assets/94395a53-69a2-408b-a1c8-c3745c459b0d)

## Section 12: Piping
### Material
We use the pipe character ( | ) to separate two commands: command1 | command 2
Examples: 
- date | rev
- ls -l | less

Differences between redirecting and piping: 
> connects a command to some file
| connects a command to another command

Command: tr - it will take text from stdin and outputs based on a set of characters to match and translate
Some examples:
- cat msg | tr s S
- cat msg | tr s a
- cat msg | tr a-z A-Z
- cat msg | tr -d s
- cat data.txt | tr -d [:alpha:] | tr -d
- cat data.txt | tr -d [:alpha:] | tr -d : | tr -d [:blank:] > phones.txt

We can pipe multiple times in a row to achieve a desired output
Example: cat file | head -7 | tail -5

Command: tee <file> - reads stdin and copies it both  to stdout and to a file
This allows us to capture info in the middle of a pipeline without interrupting the flow
It goes like this: command1 | tee file.txt | command2
Example: ( cat colors.txt words.txt > colorsAndWords.txt | wc ) WON't WORK because we cannot pipe a file into wc
Instead do this: cat colors.txt words.txt | tee colorsAndWords.txt | wc

### Exercise
Link: https://plum-poppy-0ea.notion.site/Piping-Exercise-2be75864d4bb42beabb6b3d89cda2be3

![image](https://github.com/user-attachments/assets/d665fc52-918b-448d-b4ed-74460e145ba7)
![image](https://github.com/user-attachments/assets/d992a877-0e47-4c0e-9e21-0be14b13772c)
![image](https://github.com/user-attachments/assets/d76b1798-462b-4db2-b779-927a413dd714)
![image](https://github.com/user-attachments/assets/3c617986-86a7-4c07-9208-80d373cdc255)

## Section 12: Expansion
### Material
Some characters in bash cannot be echoed, as they posses a specia meaning

* - wildcard character, represents zero or more characters in a filename
Examples: ls *.html will match any files that match with .html like index.html for example

? - represents a single character 

[] - matches a range of characters
Examples: ls [A-F]*
          ls pic[123].png will match pic1.png, pic2.png, pic3.png
Negative ranges: if we include ^ inside [], we tell to match everything EXCEPT that wildcard

~ is a wildcard for home directory

Brace expansion ( {} ) is sued to generate arbitrary strings. What it does is generating multiple strings for us based on a pattern.
Example: touch page{1,2,3}.txt will generate three files: page1.txt, page2.txt, page3.txt

Ranges: 
- mkdir jan{1..31} will generate jan1, jan2...jan31
- echo {2..10..2} will print 2,4,6,8,10
- touch group-{a..e}.txt will generate files group-a/txt, group-b.txt...

Nested brace expansion: example - echo {x,y{1..5}, z} --> x y1 y2 y3 y4 y5 z

Arithmetic Expansion: the shell will perform math via expansion using $((expression)) syntax. Inside, we can write arithemtic expressions using: +, -, *, /, ** (exponents), % (modulo)

Quoting:
- " ": using the double quotes, the shell will respect the spacing and ignore special characters except for $, \ and `.

Command substitution: we can use $(command) to display the output of another command
Example: echo "today is $(date)"

### Exercise
Link: https://plum-poppy-0ea.notion.site/Expansion-Exercise-added25bbf314060a226a81c09921892

#### Part 1
![image](https://github.com/user-attachments/assets/8527d80d-3d5b-4b7e-96f6-9bdc20a241d7)
![image](https://github.com/user-attachments/assets/c34250b0-e76f-425a-85f6-23d74a02eb1d)
#### Part 2
![image](https://github.com/user-attachments/assets/c98adfa2-e31a-4ca8-a95d-51bd73fecb32)
#### Part 3
![image](https://github.com/user-attachments/assets/7d915dc4-5a2a-448e-bcd1-56c2f06964b6)
![image](https://github.com/user-attachments/assets/47cc3e8b-327f-47e7-80a9-b0d839633166)

## Section 14: Finding Things
### Material
Command: locate - quick way to perform a search of pathnames across our machine that match a given substring and then prints out any matching names

Command: find - a more powerful version of locate, by default lists every single file and directory nested in our current weorking directory.
- We can also provide a specific folder.
- Finding by type: we can tell find to only find by file type - only print files, dirs etc.
  Examples: find -type f will limit the search to files.
            find -type d for directories
- finding by name: -name "pattern"; Example: find ~/Desktop -name "*.txt".
  iname is for case insensitive search.
- find -size will helps us finding files of a specific size: find -size +1G, find -size -50M, find -size -20k

Timestamps:
- mtime: modification time
- ctime: change time
- atime: access time

Logical operators - can be used in combination with find command:
- and
- or
- not
Example: find -name "\*chick\*" -or -name "\*kitty\*"'

User Defined Actions:
We can provide find with our own action to perform using each mathcing pathname. The syntax: find -exec command {} ; .
Example: find ~ -type f -empty -exec ls -l '{}' ';' (for every match we find run ls -l command)

Command: xargs - a command to build up the input into a bundle that will be provided as an argument list to the next command.
Example: find -name "*.txt" | xargs ls

### Exercise
Link: https://plum-poppy-0ea.notion.site/Find-Exercise-1258f6c24327427888e3662cab37b4f9

![image](https://github.com/user-attachments/assets/e314e3a5-5b1e-4d9e-a1d7-af02f5823982)
![image](https://github.com/user-attachments/assets/edcc2be4-b971-4f66-9309-c4b72e503eca)
![image](https://github.com/user-attachments/assets/ebfd5b43-7dc5-427e-b364-1b2d3ca67800)
![image](https://github.com/user-attachments/assets/eac16faf-d03c-418f-804a-1e770a45f282)
![image](https://github.com/user-attachments/assets/32400e86-830f-484b-8560-3f1127d38657)
![image](https://github.com/user-attachments/assets/76be131a-d846-476c-a90d-4a5bf497d6a1)
![image](https://github.com/user-attachments/assets/19f44fa5-0872-4141-8d89-522ab46d7afc)
![image](https://github.com/user-attachments/assets/1b8fca32-5dcb-4bbc-867e-2facf35ba689)

## Section 15: Grep
### Material
Command: grep - searches for patterns within files contents
How to use: grep PATTERN FILE
Example: grep "chicken" animals.txt

There are a lot of different useful options:
- "-w" option to ensure that it matches a word not not a pattern (exmaple: cat and not cattle)
- "-r" option for recusrive search: will search the pwd and nested directories for the lines that contain the pattern
- "-i" for case insensitive
- "-c" to count how many times the match occurs
- "-A/-B" to include lines before and after the line where the match occurs. Examples: grep "wagon" file.txt -A1
- "-C" does A and B combines, so C1 for example will give 1 line before and after the line that matches
- "-n" will show the line numbers

Regex: pattern matching syntax
![image](https://github.com/user-attachments/assets/22cf0763-3280-41c2-b48c-5ee68fe77742)

Egrep/grep -E lets us use special chars when matching patterns

Command: ps - shows current processes

## Section 16 & 17: Permission Basics & Altering Permissions
### Material
Command: whoami - shows your user
We can have multiple users on the same OS

#### File Owners and Group Owners
- File Owner (User):
  Every file or directory is owned by a user. Typically, this is the user who created the file. The owner has specific permissions on the file.
- Group Owner:
  Each file or directory is also associated with a group. A group consists of one or more users. Any user in the group will have the group's permissions for that file.

#### File Type Attribute

In Bash (and Unix-like systems), permissions determine what actions can be performed on a file or directory by different users. Here's a breakdown of the basics:

1. File Owners and Group Owners
File Owner (User):
Every file or directory is owned by a user. Typically, this is the user who created the file. The owner has specific permissions on the file.

Group Owner:
Each file or directory is also associated with a group. A group consists of one or more users. Any user in the group will have the group's permissions for that file.

2. File Type Attribute
When you view file attributes (e.g., using ls -l), the first character indicates the file type:

- : Regular file
d : Directory
l : Symbolic link
b : Block device (e.g., a hard drive)
c : Character device (e.g., a terminal)
p : Named pipe
s : Socket
Example:
-rw-r--r--  1 user group 1024 Jan 15 14:00 file.txt
Here, the - at the beginning indicates a regular file.

#### Read, Write, and Execute Permissions
Permissions are divided into three categories: owner, group, and others. Each category has three types of permissions:

Read (r)
- For files: Allows the contents of the file to be read.
- For directories: Allows the listing of directory contents.
Write (w)
- For files: Allows modifying or deleting the file.
- For directories: Allows adding, deleting, or renaming files within the directory.
Execute (x)
- For files: Allows executing the file as a program or script.
- For directories: Allows accessing the directory (required to cd into it).

#### Permission Representation
ermissions are displayed as a string of 10 characters when using ls -l: 
-rwxr-xr--  1 user group 1024 Jan 15 14:00 file.txt

#### Numeric (Octal) Representation
Permissions can also be represented using numbers (octal system):

4: Read
2: Write
1: Execute
Combine these values to represent permissions:

7 (4+2+1): Read, Write, Execute (rwx)
6 (4+2): Read, Write (rw-)
5 (4+1): Read, Execute (r-x)
4: Read only (r--)

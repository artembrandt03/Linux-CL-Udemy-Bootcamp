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
Shortcut: ctrl + l - to clear the termianl
Shortcut: ctrl + a - jump to the beginning of the line
Shortcut: ctrl + e - jump to the end of the line
Shortcut: alt+f or alt+b - move forward/backward one word at a time
Shortcut: ctrl+t - swap the current character under the cursor with the one preceeding it
Shortcut: ctrl+k - kill the text from the cursor location until the end of line
Shortcut: ctrl+u - kill the text from cursor to the beginning of the line
Shortcut: alt+d - to kill text from current cursor location till the end of word
Shortcut: ctrl+w or alt+delete to go in the opposite direction
Shortcut: ctrl+y - retrieve the most recent 'kill' with other commands (this is called yanking)

History - bash keeps a record of commands we previously entered. We could already scroll through history withj up and down arrows to see the commands;
But you can also use 'history' command to view the entire history, though it's generally easier with piping the output to | less
To run a command that's far in our history, we can look at the line it's at and run that 'line'
  Example: command at line 1314
          !1314

Shortcut: ctrl+r - to search through history

Command Line Shortcuts
===

Navigation
---
Show file path:
   
    pwd # Print Working Directory

Open folder:

    open .              # Open current folder
    open ..             # Open parent folder
    open <folder/path>  # Open specified folder

Display current folders/files:

    ls      # list folders/files
    ls -a   # list all folders/files (including hidden files)

Change directory:

    cd ..           # Change to parent directory
    cd file/path    # Change to specified directory

Push/Pop directory:

    pushd <folder/path> # save current directory to stack and go to folder/path
    popd                # pop folder/path from stack and go to that folder/path

Search
---

Find a file:

    find <search_directory> -name "<file.ext>"  #print location of file

Find word in a file(s):

    grep <word> <file.ext>  # search word in file

Help Tools
---

Read a manual page:

    man <command>   # get details about command

Find what man page is appropriate:

    apropos <command detail>    # finds potentially helpful info about command

Permissions
---

Run command as Super User:

    sudo <command>  # run as admin

Change permission modifiers:

    chmod

Change ownership:

    chown

Folder/Files Manipulation
---

Create/Destroy directory:

    mkdir <folder_name>         # Create specified folder
    rmdir <folder_name>         # Directory must be empty
    rm -rf <folder_name>        # Destroy directory containing files

Create/Destroy file:

    mkfile <file_name>    # Create a new file
    rm <file_name>        # Destroy an existing file

Create empty file:

    touch <file_name.ext>   # Create empty file

Create file & add text:

    cat > <new_file.ext>    # start typing. ctrl-c when done adding text

Move file/directory

    mv <file_path> <new_path>   # Move file or directory

Print contents of a file:

    cat <file_name>     # echo file contents

print some arguments

    echo

Page through a file:

    less

Copy/Paste to clipboard:

    pbcopy < <fileName> # copy data from file into clipboard
    pbpaste > file.txt  # save clipboard to file

Copy files/file content:

    cp <from_file.ext> <to_file.ext>     # copy contents to new file
    cp <from_file.ext> <directory/path>  # copy file to another directory
    cp <directory/path> <directory/path> # copy files from one directory to another

Enviromnent Variables
---

Echo environment variables:

    env

Export/set a new environment variable:

    export

Piping and Redirection
---

Find details about pipes and redirection [here](http://cli.learncodethehardway.org/book/ex15.html).


Miscleaneous
---

Wildcard:

    ls *.txt     # list all text files
    ls <file>.*  # list all files named <file>

Print computer's network name:

    hostname

Exit shell:
    
    exit

Execute arguments:

    xargs

References
---

Command Line Crash Course by [Zed A. Shaw](http://cli.learncodethehardway.org/book/)

Bash Shell Programming [How To's](http://www.cyberciti.biz/faq/category/bash-shell/)

Unix/Linux [Command Reference](http://files.fosswire.com/2007/08/fwunixref.pdf)
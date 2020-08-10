# Linux Commands and Shell Scripting

## Frequent Commands

**Deletion (rm and rmdir)** - Used to remove something. Use option -r after command and before the folder/file to recursively remove that and everything underneath it.

**Finding execs (which)** - The which commmand can be used to find where an executable has been stored. For instance, "which go" would tell you the location of the go executable

## Syntax/Operators

**"|" vertical bar character** - The vertical bar character represents piping, or redirection occurring in a Linux command.

**"&&" AND operator** - The AND operator allows you to split commands up so that the command after only runs if the one before runs successfully.

**"-"** - If comes after bash, it means to open up the bash to allow io utility for it

**${  }** - Generate parameter expansion; takes the variable or expression and expands it to what it truly represents at its source. Good practice

**(command)** - Denotes the usage of a subshell to execute "command" or whatever comes between parentheses. Has return status of "command". Command could be any sequence of differents commands or shell lines. 

**lastcode = \$?** - "$?" Indicates thee exit code of the last executed command

## Word Operators

**BASH_SOURCE[0]** - file path for where current file is located

**dirname** - Directory path for where current file is located

**exit (followed by a code)** - in Linux, exit code 0 means exit success. Any code after that represents some kind of error. Error code 1 is usually interpreted as a general error. 

## Options and Shortcuts

Linux commands usually have various options that you can append after them. These commands have some cool features and options.

- Shortcuts; options beginning with a single hyphen are a shortcut of a longer option, like "-l" being a shortcut for "--length"

- Combination; multiple shortcuts can be combined together for faster scripting, such as the curl options -s (silences the progress bar of the curl command) and -L (follow the given redirect) being joined together  
    <code>curl -s -L google.com </code>  
    can become  
    <code>curl -sL google.com </code>

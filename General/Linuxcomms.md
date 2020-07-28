# Linux Commands and Shell Scripting

## Frequent Commands

**Deletion (rm and rmdir)** - Used to remove something. Use option -r after command and before the folder/file to recursively remove that and everything underneath it.

**Finding execs (which)** - The which commmand can be used to find where an executable has been stored. For instance, "which go" would tell you the location of the go executable

## Syntax/Operators

**"|" vertical bar character** - The vertical bar character represents piping, or redirection occurring in a Linux command.

**"&&" AND operator** - The AND operator allows you to split commands up so that the command after only runs if the one before runs successfully.

## Options and Shortcuts

Linux commands usually have various options that you can append after them. These commands have some cool features and options.

- Shortcuts; options beginning with a single hyphen are a shortcut of a longer option, like "-l" being a shortcut for "--length"

- Combination; multiple shortcuts can be combined together for faster scripting, such as the curl options -s (silences the progress bar of the curl command) and -L (follow the given redirect) being joined together  
    <code>curl -s -L google.com </code>  
    can become  
    <code>curl -sL google.com </code>

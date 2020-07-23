# Makefiles

## Components

**.PHONY** - Line that goes at the top of the Makefile to prevent caching for specific make commands that are listed within .PHONY's results

## Good Practices

**Abstracted Scripts** - It is often good, rather than having a monstrous amount of Make logic in one file, to have the makefile referring to several different scripts that you can individually identify with the business logic/command they perform for.

**Make Help** - Have a make command specifically for providing an overview of what the various commands do/general info necessary to properly use the various make commands

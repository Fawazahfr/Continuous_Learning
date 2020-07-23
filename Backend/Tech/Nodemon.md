# Nodemon

## What is it?

Package that automates deployment during development, allows developers to have their deployed binaries refresh upon code base changes very easily.

## Making it Work

**Config**: You can modify the configs for Nodemon to control which files are being assessed for changes, and this may also require you to change other settings based on the OS to adjust for polling, e.g. Nodemon may work on Linux and Mac without polling but not on windows. You can detect which file types to look for changes in, so for example just .go files but not .md files

## Useful With

**Docker**: You can load nodemon into a docker CMD command and set up a volume between the container and the files to be watched so that you can develop locally and automatically see changes as they come up in the container. 
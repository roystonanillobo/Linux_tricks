# Move all files from subfolders to parent folder

## Windows
https://superuser.com/questions/746632/windows-how-to-move-all-files-in-subfolders-to-a-parent-folder/746652

## Linux
https://askubuntu.com/questions/146634/shell-script-to-move-all-files-from-subfolders-to-parent-folder

`find . -mindepth 2 -type f -print -exec mv {} . \; `

## Mac
https://osxdaily.com/2015/02/11/flatten-nested-directory-structure-command-line/

`find [DIRECTORY] -mindepth 2 -type f -exec mv -i '{}' [DIRECTORY] ';'`





# vimr

vimr is a terminal-based file rename utility that lets you easily mass-rename files using Vim. It also supports recursive renaming in subfolders.

## Installing

1. For the current user:
   ```
   curl https://raw.githubusercontent.com/picakia/vimr/master/vimr > ~/bin/vimr && chmod +755 ~/bin/vimr
   ```
2. For the current system:
   ```
   sudo PREFIX=/usr/local make install
   ```
Or simply copy the `vimr` file to a location in your `$PATH` and make it executable.

## Usage

1. Go to a directory and enter `vimr` with optionally, a list of files to rename or -p [pattern] parameter.
2. A Vim window will be opened with names of all files in directory or with all files marching pattern even in subdirectories.
3. Use Vim's text editing features to edit the names of files. For example, search and replace a particular string, or use visual selection to delete a block.
4. Save and exit. Your files should be renamed now.

## Other features

* If you want to list only a group of files, you can pass them as an argument. eg: `vimr *.mp4`
* If you want to perform recursive rename just pass -p PATTERN parameter to vimr and it will list all files matching that pattern including these in subdirectories. (PATTERN can be "*" if you want all files in all dirs)
* If you have an `$EDITOR` environment variable set, vimr will use its value by default.
* If you are inside a Git directory, vimr will use `git mv` (instead of `mv`) to rename the files.
* You can use `/some/path/filename` format to move the file elsewhere during renaming. If the path is non-existent, it will be automatically created before moving.

## Screencast

![alt text](screencast.gif "vimr in action")

## Gotchas

Don't delete or swap the lines while in Vim or things will get ugly.

## Credits

Script was originally created by [thameera](https://github.com/thameera). Check out his profile!

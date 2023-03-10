# Copying files with error showing batch file.

This script is a batch file for the Windows command prompt that copies all files from a source directory to a destination directory. It also tracks the number of files that were successfully copied and those that failed to copy.

The script begins by setting the colors of the command prompt window to yellow using the `"color"` command. The script then displays some ASCII art using the `"echo"` command.z

Next, the script sets the values of the "source" and "destination" variables to the directories where the files are to be copied from and to, respectively. The `"setlocal enabledelayedexpansion"` command enables the use of the "!variable!" syntax, which allows the script to access and modify variables within a loop.

The script then sets the `"files_copied"` and `"files_failed"` variables to 0. It also creates a new file called `"failed_files.txt"` and clears its contents.

The script then uses a `"for" loop` to iterate through all the files in the source directory. For each file, the script uses the `"xcopy"` command to copy the file to the destination directory. If the copy operation was successful, the script increments the `"files_copied"` variable by 1. If the copy operation failed, the script increments the `"files_failed"` variable by 1 and appends the file name to the `"failed_files.txt"` file.

After the loop completes, the script displays the total number of files copied and failed, as well as the names of the files that failed to copy (if any). It then deletes the `"failed_files.txt"` file and waits for the user to press any key before exiting.

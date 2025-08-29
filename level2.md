# username / password 
leviathan2 / NsN1HwFoyN
# Concept
* more SUID binaries :D
# Method of solve
* the SUID binary in this level does a privilged file read with `/bin/cat` to read a file specfied in the command arguments
*  by defaultm it own;t read any files that belong to the `leviathan3` user, which is our traget user

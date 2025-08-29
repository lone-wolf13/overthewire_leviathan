# Username / Password
leviathan1  /  3QJ3TgzHDq
# Command used to sign inn
sshpass -p 3QJ3TgzHDq ssh leviathan1@leviathan.labs.overthewire.org -p 2223
# Concept
* inspecting the dynamic libray calls and system calls used by process using the `ltrace` command
# method of solvekali
* there is a `check ` SUID binary in the home directory owned by our target user `leviathan2`
* when we run the `check` binary, it asks us for a password, but we dont know it
* we used the ltrace command to check which dynamic library calls and  system calls are used when it is run
* we see that the binary is doing a a `stremp` runction that checks the user input against the `sex` value
* when we provide the correct password, we get an /bin/sh shell


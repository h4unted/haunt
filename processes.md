[return](bash)

:processes:

```sh

#first install screen and reptyr
sudo apt install screen
sudo apt install reptyr

#start any process and then stop them by pressing ctrl+z
#then to know the process id of that process, type
jobs -l

#then to bring that process id to the background type 
bg %1

#then you may disown that background process for you to close the terminal.
disown -h %1

#then close the terminal

#ps lists the processes only on the terminal session
#ps aux lists all processes on the global space
#open a new terminal the process will no longer be listed on the <jobs -l> command but on this command
ps aux | grep -i <process name>

#on that same terminal start a new screen session by typing
screen

#then to start that process on the new terminal type
reptyr <pid>

#sometimes restoring processes using reptyr does not work its better to run the process as a child process on screen first type this first an run the process
screen

#then ctrl+A+D to detach, and close the terminal

#then open another terminal and type this command to list all screen parented process ids
screen -ls

#restore that process 
screen -r <screen pid>

#kill that process
screen -r <screen pid>

```





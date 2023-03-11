[return](bash)

:variable:

```sh

# This is how you set a temporary environment variable in bash
export fhirfolder=/home/help/directory
echo $fhirfolder

# Take note though that when you assign a value to a variable using “export” in a shell, the changes are not persisted on reboots or to other shells. In order to set a permanent environment variable in Bash, you have to use the export command and add it either to your “.bashrc” file (if this variable is only for you) or to the /etc/environment file if you want all users to have this environment variable.

$ nano /home/user/.bashrc

# Content of the .bashrc file

export VAR="My permanent variable"



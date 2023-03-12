[return](gnuhealth)

:gnuhealthuser:

```sh

#postgres user (s) 
#create another user for the server and database
#mume
sudo useradd -m projhelp

#you may need to start the postgres server at least one time 
#as this file may be created 
#during first startup.
#mume
sudo service postgresql start

#look for the pg_hba.conf file. Become the postgresql user first. 
#with a postgresql environment variable. (suse) Usually this file 
#is located at /etc/postgresql/10/main or /var/lib/pgsql/data.
#you can not start a postgres shell if you are not running shell as root first
#rume
su - postgres -c "psql -t -P format=unaligned -c 'show hba_file'"

#using a bash file editor, make sure the pg_hba.conf file is set to 
#“trust” on these following configurations
#Make sure you edit the file as user 'postgres', not root.
#Otherwise, postgres may have trouble reading the changed file. 
#suse

local all all trust

#and so that the create button will not be greyed out with the initial use of the
#tryton client that first tries to establish a connection with the tryton server's
#gnuhealth database, make sure “trust” is also set on these following configurations
#as well
#suse
host all all 127.0.0.1/32 trust
host all all ::1/128      trust

#in order for edits within the pg_hba.conf file to take effect, make sure 
#to restart the postgresql service once again
#mume
sudo service postgresql start

```





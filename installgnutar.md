[return](gnuhealth)

:installgnutar:

```sh

#uncompress GNU Health HMIS package
#guge
tar xzf gnuhealth-latest.tar.gz

#download the latest GNU Health installer
#guge
wget -qO- https://ftp.gnu.org/gnu/health/gnuhealth-setup-latest.tar.gz | tar -xzvf -

#change to the GNU Health installation directory matching your version
#guge
cd gnuhealth-4.0.4

#run the GNU Health installer
#guge
bash ./gnuhealth-setup install

#finally, enable the BASH environment for the gnuhealth user.
#guge
source ${HOME}/.gnuhealthrc

#activate Network Devices for the JSON-RPC Protocol
#the Tryton GNU Health server listens to localhost at port 8000, 
#not allowing direct connections from other workstations.
#if necessary, enter the following:
#guge
editconf


#you can edit the parameter listen in the [web] section, 
#to activate the network device so workstations 
#in your net can connect. Will allow to connect to the server
#in the different devices of your system.
#for example, the following block
[web]
listen = *:8000



#setting up a Local Directory for Attachments
#by default, Tryton uses a system-wide directory to store
#the attachments. It is advisable, in GNUHealth to keep 
#the attachments in the gnuhealth user space.

#if necessary, edit the server configuration file trytond.conf 
#and enter the attach directory under the [database] section,
#for instance:
#guge
editconf

#guge
[database]
path = /home/gnuhealth/attach

#since debian systems connect to database over a UNIX socket,
#add an extra / under the [database] section, for instance:
[database]
uri = postgresql:///localhost:5432

#create the database
#we use "health" as an example, choose the name of your database,
#but keep it short and only alphanumeric chars

#guge
createdb health

#change to your newly installed system (use the alias cdexe):
cdexe

#and initialize the instance:
#you will be asked to provide a password for the "admin" user.
#if everything goes well, you are ready to start the GNU Health HMIS node server.
python3 ./trytond-admin --all --database=health

#start the GNU Health HMIS node
cd
bash ./start_gnuhealth.sh

#starting and Stopping the GNU Health service
#you can issue the commands:
#guge
systemctl start gnuhealth

#or:
#guge
systemctl stop gnuhealth

```

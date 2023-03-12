[return](gnuhealth)

:postgresqlinstall:

```sh

#postgresql is arelational database management system (RDBMS). 
#The RDBMS provides an interface 
#between users and applications and the database, 
#as well as administrative functions for managing 
#data storage, access, and performance.


#first update the advanced packaging tool (apt) package index
#mume
sudo apt update

#install postgresql server and contrib package which 
#which provides additional features for the postgresql database
#mume
sudo apt install postgresql postgresql-contrib

#Once the installation is complete, the PostgreSQL service will start. 
#To verify the installation, use the psql tool to print the server version
#mume
sudo -u postgres psql -c "SELECT version();"

#The output should look something like the following:

#PostgreSQL 11.5 (Debian 11.5-1+deb10u1) on x86_64-pc-linux-gnu, compiled by gcc  (Debian 8.3.0-6) 8.3.0, 64-bit

```

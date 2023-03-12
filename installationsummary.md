[return](gnuhealth)

:installationsummary:

1. First install global dependencies such as python and postgres server 
     (pip packages such as trytond and tryton are just installed on local 
     python by the gnu-health installer)
2. Create gnuhealth server (ghs) user.
3. As root user edit the HBA file of that postgres server, assign that ghs 
     user a create database role and make it create a database
4. Authenticate and download the gnuhealth installer
5. Make that installer install itself and all its python packages on local python
6. Set the bash environment variable for that gnuhealth installation, edit its configuration 
    and attach the created postgres database on to it
7. Start the server.

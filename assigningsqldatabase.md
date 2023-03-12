[return](gnuhealth)

:assigningsqldatabase:

```sh

#The following command switches to the postgres administration user
#and gives permissions to your newly created gnuhealth administrator:
#rume
su - postgres -c "createuser --createdb --no-createrole --no-superuser gnuhealth"

```



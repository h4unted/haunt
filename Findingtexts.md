[return](filesystem)

:findingtexts:

```sh

# To grep a row containing a word
awk '/#/' directory/text.txt

# to grep a row with a first field of "name" print its 4th collumn
awk '$1 == "name" { print $4 }' directory/text.txt

```





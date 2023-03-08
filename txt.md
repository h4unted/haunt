[return](filesystem)

:txt:

```sh

cat > test.txt

# type a text and press ctrl+d
# or to create a file
touch test.txt

# to edit a file
vim test.txt

# i = edits text file
# esc = exits editing
# :q = exit
# :q! = exits without saving
# :qw = save and exit

# Place the cursor on the line you want to begin cutting.
# Press V to select the entire line, or v to select from where your cursor is.
# Move the cursor to the end of what you want to copy, using h,j,k, or l
# Press y to copy it, or d to cut it.
# Place the cursor where you would like to paste your copied stuff.
# Press P to paste it before your cursor, or p to paste it after the cursor.

# in order to copy from and to outside of vim terminal
# follow this
sudo apt-get update
sudo apt-get install vim-gtk3

# v then highlight a line
# v "by
# v "bp
# v "+y
# v "+y

# to undo in vim type u
# to redo ctrl+r

```

# mkdice

Create diceware like passwords from terminal. Possible to use them with keyboard shortcut.
You may choose from arbitrary diceware wordlists, some are already provided within the repo.

### Preperation
Put the file `mkdice` to your local `~/bin` folder or wherever you have your custom scripts stored in.\
\
You then need to create the default folder `~/.diceware_wordlists` for the wordlists und put the `*.txt` there.
* You can either move the provided folder using the command `mv .diceware_wordlists ~/` within the repo folder.
* Or you just create a symbolic link using the command `ln -s .diceware_wordlists ~/.diceware_wordlists` within the repo folder.

You dont need to do that, if you provide full path to wordlist with `-F`

### Using
Command `mkdice` in terminal returns a 3 word passphrase

You can use parameters to modify the output (like `mkdice -l 5 -sxd _`)\
`-l` length of the passphrase, number of words used (default `3`)\
`-F` full path to used diceware list\
`-f` filename of used diceware list within default folder `~/.diceware_wordlists`\
`-r` source of the entropy to choose random words (default `/dev/urandom`)\
`-d` delimiter between the words (default `-`)\
`-D` delimiter between the words in the clipboard (default same as `-d`)\
\
`-x` the passphrase will also be available in the clipboard (paste it with `strg+v`)\
`-U` the first letter of each word will be Uppercase\
`-s` silent, the passphrase will not be returned to the terminal (standard output)\
`-z` the passphrase will be shown with zenity information (if available)\
\
***Its most handy to create a keyboard shortcut for your preffered command and use it with -x or -z to have the passphrase available.***

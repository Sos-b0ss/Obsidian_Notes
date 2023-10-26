";" is used to run several commands in a row completely separated from each-other
\
"&&" will also run the sequence of commands in the line however it will stop all 
commands after an error occurs with a command in the line
\
"aliases" are ways to run a custom command with flags included used this way.
aliases are only usable during that terminal session they are named and only 
usable for that user the terminal is open for
\
ex.
	[[alias]] lh="ls -lah"
the lh in this is the custom command and the -lah is the command that runs instead
\
you can also name an [[alias]] anything you need to
\
"unalias <alias name>" is a command used to [[unalias]] any alias stated in the brackets
\
"alias" can be used to show you a list of all the aliases that are currently being used in the terminal
\
you can keep aliases by:
\
editing the [[Bashrc]] to make it so that the aliases stay even after the terminal closes or system boots
\
use:
"cp .bashrc .bashrc.back" to backup the .bashrc for the user because without it the user could corrupt
\
look for "some more aliases" to show you all the aliases that will be with the user by default
\
in the config file you can also make at the bottom "#custom alias section" and write the alias that 
you want to stay just like in the terminal
\
afterwards make sure to reload the .bashrc by using:
\
"source .bashrc"
\
avoid using any special characters when making aliases or variables because it just doesnt compile properly sometimes
\
to double check perm.custom aliases you can use:
"tail -8 ~/.bashrc"
\
"rm -i" also asks you if you're sure you would like to remove a file
\
echo -e "\n test \n" will make a new line for the echoed text similar to a hard return

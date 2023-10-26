There are: user level & system level cron jobs
\
[[Cron]] is a robust task scheduler [[Daemon]] automatically included in Linux operating systems.
\
[[CronTabs]] ([[CronTablets]]) each user has their own individual private tabs (including root)
\
[[Cron]] Syntax:
Execute backup.sh script every Sunday @ 2:36AM
\
ex.
36 2 * * 7 root /usr/local/sbin/backup.sh *
\
you can use "/" to do every other hour/day/week/month
\
you can use "-" will do a range for hour/day/week/month
\
you can use the system variable {$DATE} and it lets you insert date into scripts
\
research system variables!!
\
Using [[crontab.guru]] to verify syntax for crontabs also [[crontab-generator.org]] generates [[crontabs]] for you.
\
[[Lynis]] is a tool that checks for vulnerability like a scanner.
\
crontab -l <- lists crontabs for working user
crontab -e <- edits crontab w/ nano
\
Research brace expansion! {arrays}
\
To verify the [[cron]] service is running
	[[systemctl]] status [[cron]]
\
Inspect user cron tab to verify no tampering
	[[crontab]] -l
\
Observe no commented lines in here^^
\
Make directory for reference
	sudo mkdir -p /usr/share/{directoryName}
\
edit crontab to make sure to schedule moving files
	crontab -e
	add - 0 18 * * mv ~/Download/{direcotyrName}*.docx /usr/share/{directoryName}
	add - 0 18 * * mv ~/Downloads/{directoryName}*.txt usr/share/{directoryName}
\
double check to make sure crontab was made
	sudo ls -l /var/spool/cron | grep sysadmin
\
make script for backups in dir called scripts
	-Create a tar archive for home
	-Saves to var
	-Moves from saves/var to home
	-List all var backups
	-Save the output to a log file
	-At the end show free memory

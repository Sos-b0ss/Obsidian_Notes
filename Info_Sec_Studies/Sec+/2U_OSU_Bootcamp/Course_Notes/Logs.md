[[JournalCtl]] & [[log rotate]]

[[PII]] - personally identifiable information

[[Linux]] stores all logs in:

- /var/log/auth.log
- /var/log/cron.log

[[app logs]] - software used by user

[[event logs]]/[[sec logs]] - info about security events

[[services logs]] - print jobs or [[cron jobs]]

[[system logs]] - system & [[kernel]] logs like [[boot logs]]

[[journalctl]] can be used to sift through all these [[Logs]]

[[Systemd]] - used for logging system wide event (not read friendly)
[[journald]] - actually logs readable info [[Logs]]
[[journalctl]] - read friendly access to [[Logs]]

[[Syntax]]: [[Sudo]] [[journalctl]] --list-boots

[[Sudo]] journalctl -ef
	(e) = end of file | (f) = follow
sudo journalctl _UID (tells you logs of user from systemd journald logs)

_UID={uid}

logging [[daemons]] cannot control log file size (if left unchecked log files can consume all space on disk)

[[log rotation]] 
- scheduling the creation of logs
- [[compressing]]
- Executing commands
- [[time stamping]]
- log file [[archive pruning]]
- faster logging of info because smaller files

main config is in:
	/etc/logrotate.conf
	(some apps will require their own configs that do not fit the default log configs)

[[auditd]]: a [[kernel]] level [[subsystem]] that can watch every system cell an app makes (essentially an alarm system, ie. it doesnt act!)

[[ausearch]] | [[aureport]]/[[aulast]] | [[auditctl]]

-au is any auth attempts
-m is any modifications

*whenever there is a change made to the 'journald.conf' then systemd-journald system needs to be restarted
[[journald.conf]] is found in /var/log/journel

do this in :/etc/systemd/journald.conf

uncommenting is enabling for: storage=auto
and this enables logging persistence so your logs don't go away on reboot.

other apps put 'logrotate.conf's into /etc/logrotate.d

.d is not a file extension its just a part of the file names

log rotate conf creation

-navigate to the /etc/logrotat.d/
-create a {mail} file named {mail  }

syntax of log rotate

	bash
		/var/log/mail.log {
			rotate 56
			daily
			notif empty
			endscript
		}

this will rotate every 8 weeks and it does it mostly 6PM or 11:55PM and it does not log empty.log\s

[[auditing]] is not [[retroactive]]

to change what [[auditctl]] logs use:

					  v (if you dont specify perms it will default to rwxa)
sudo [[auditctl]] -w /home/sysadmin/Music/ -p wa
sudo [[Nano]] /etc/audit/rules.d/audit.rules

-w /etc/shadow -p wa shadow
-w     /etc/shadow     -p               wa                              shadow
watch	what watches	[[permissions]]	writes or attribute changes	key name

-w [[/etc/passwd]] -p wa passwd

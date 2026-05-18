# process commands

zuhaib_khan@DESKTOP-KE4EHHC:~$ ps
    PID TTY          TIME CMD
    317 pts/0    00:00:00 bash
    573 pts/0    00:00:00 ps
zuhaib_khan@DESKTOP-KE4EHHC:~$ free
               total        used        free      shared  buff/cache   available
Mem:         7795916      527884     7272972        3604      148192     7268032
Swap:        2097152           0     2097152
zuhaib_khan@DESKTOP-KE4EHHC:~$ uptime
 07:16:28 up 10 min,  1 user,  load average: 0.00, 0.02, 0.00
zuhaib_khan@DESKTOP-KE4EHHC:~$

# service commands


zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl status ssh
Unit ssh.service could not be found.
zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl status
● DESKTOP-KE4EHHC
    State: running
    Units: 356 loaded (incl. loaded aliases)
     Jobs: 0 queued
   Failed: 0 units
    Since: Mon 2026-05-18 07:05:49 UTC; 13min ago
  systemd: 255.4-1ubuntu8.12
   CGroup: /
           ├─init.scope
           │ ├─  1 /sbin/init
           │ ├─  2 /init
           │ ├─  8 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10 --log-truncate
           │ ├─312 /init
           │ ├─313 /init
           │ ├─317 -bash
           │ ├─595 systemctl status
           │ └─596 less
           ├─system.slice
           │ ├─console-getty.service
           │ │ └─201 /sbin/agetty -o "-p -- \\u" --noclear --keep-baud - 115200,38400,9600 vt220
           │ ├─cron.service
           │ │ └─173 /usr/sbin/cron -f -P
           │ ├─dbus.service
           │ │ └─174 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
           │ ├─rsyslog.service
           │ │ └─209 /usr/sbin/rsyslogd -n -iNONE
           │ ├─system-getty.slice
           │ │ └─getty@tty1.service
           │ │   └─212 /sbin/agetty -o "-p -- \\u" --noclear - linux
           │ ├─systemd-journald.service
lines 2-30
^C
zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl start
Too few arguments.
zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl start ssh
Failed to start ssh.service: Interactive authentication required.
See system logs and 'systemctl status ssh.service' for details.
zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl start ngnix
Failed to start ngnix.service: Interactive authentication required.
See system logs and 'systemctl status ngnix.service' for details.
zuhaib_khan@DESKTOP-KE4EHHC:~$ systemctl start nginx
Failed to start nginx.service: Interactive authentication required.
See system logs and 'systemctl status nginx.service' for details.
zuhaib_khan@DESKTOP-KE4EHHC:~$ sudo systemctl start nginx
[sudo] password for zuhaib_khan:zuhaib_khan@DESKTOP-KE4EHHC:~$ tail -n 50
^C


# Logs commands

zuhaib_khan@DESKTOP-KE4EHHC:~$ tail -n 50
^C
zuhaib_khan@DESKTOP-KE4EHHC:~$ grep "error" /var/log/syslog
2026-03-14T12:05:20.890911+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-14T12:05:20.890921+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-16T06:54:51.306492+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-16T06:54:51.306506+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-17T06:40:47.150637+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-17T06:40:47.150653+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-17T16:56:40.281436+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-17T16:56:40.281454+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-19T17:44:25.328411+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-19T17:44:25.328433+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-28T13:57:20.020168+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-03-28T13:57:20.020204+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-10T18:12:39.028027+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-10T18:12:39.028050+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-11T05:43:07.964020+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-11T05:43:07.964026+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-11T05:43:49.562880+00:00 DESKTOP-KE4EHHC snapd[180]: stateengine.go:161: state ensure error: Get "https://api.snapcraft.io/api/v1/snaps/sections": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)
2026-04-11T17:28:45.687885+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-11T17:28:45.687907+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-11T17:29:27.463027+00:00 DESKTOP-KE4EHHC snapd[186]: stateengine.go:161: state ensure error: Get "https://api.snapcraft.io/api/v1/snaps/sections": context deadline exceeded
2026-04-14T07:29:35.710055+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-14T07:29:35.710071+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-14T17:54:52.114813+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-14T17:54:52.114835+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-15T05:50:38.144552+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-15T05:50:38.144575+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-18T13:50:28.769250+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-18T13:50:28.769272+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-26T14:15:05.361918+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-04-26T14:15:05.361925+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-02T18:10:59.006179+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-02T18:10:59.006193+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-03T09:54:47.340151+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-03T09:54:47.340158+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-10T13:14:46.625657+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-10T13:14:46.625671+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-18T07:05:50.554607+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.path - Process error reports when automatic reporting is enabled (file watch) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
2026-05-18T07:05:50.554620+00:00 DESKTOP-KE4EHHC systemd[1]: apport-autoreport.timer - Process error reports when automatic reporting is enabled (timer based) was skipped because of an unmet condition check (ConditionPathExists=/var/lib/apport/autoreport).
zuhaib_khan@DESKTOP-KE4EHHC:~$ journalctl -xe
May 18 07:20:50 DESKTOP-KE4EHHC systemd[1]: Starting systemd-tmpfiles-clean.service - Cleanup of Temporary Directories.>
░░ Subject: A start job for unit systemd-tmpfiles-clean.service has begun execution
░░ Defined-By: systemd
░░ Support: http://www.ubuntu.com/support
░░
░░ A start job for unit systemd-tmpfiles-clean.service has begun execution.
░░
░░ The job identifier is 785.
May 18 07:20:50 DESKTOP-KE4EHHC systemd[1]: systemd-tmpfiles-clean.service: Deactivated successfully.
░░ Subject: Unit succeeded
░░ Defined-By: systemd
░░ Support: http://www.ubuntu.com/support
░░
░░ The unit systemd-tmpfiles-clean.service has successfully entered the 'dead' state.
May 18 07:20:50 DESKTOP-KE4EHHC systemd[1]: Finished systemd-tmpfiles-clean.service - Cleanup of Temporary Directories.
░░ Subject: A start job for unit systemd-tmpfiles-clean.service has finished successfully
░░ Defined-By: systemd
░░ Support: http://www.ubuntu.com/support
░░
░░ A start job for unit systemd-tmpfiles-clean.service has finished successfully.
░░
░░ The job identifier is 785.
May 18 07:21:32 DESKTOP-KE4EHHC polkitd[604]: Registered Authentication Agent for unix-process:634:94737 (system bus na>
May 18 07:21:32 DESKTOP-KE4EHHC polkitd[604]: Unregistered Authentication Agent for unix-process:634:94737 (system bus >
May 18 07:22:52 DESKTOP-KE4EHHC sudo[716]: pam_unix(sudo:auth): conversation failed
May 18 07:22:52 DESKTOP-KE4EHHC sudo[716]: pam_unix(sudo:auth): auth could not identify password for [zuhaib_khan]
May 18 07:25:01 DESKTOP-KE4EHHC CRON[728]: pam_unix(cron:session): session opened for user root(uid=0) by root(uid=0)
May 18 07:25:01 DESKTOP-KE4EHHC CRON[729]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
May 18 07:25:01 DESKTOP-KE4EHHC CRON[728]: pam_unix(cron:session): session closed for user root
lines 1783-1811/1811 (END)














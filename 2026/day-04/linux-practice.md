#########################Process check ########################
By using 'ps' command you can check system running processes.

ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ ps
    PID TTY          TIME CMD
   1363 pts/0    00:00:00 bash
   2148 pts/0    00:00:00 ps
ubuntu@ip-172-31-21-105:~$


ubuntu@ip-172-31-21-105:~$ ps -ax
    PID TTY      STAT   TIME COMMAND
      1 ?        Ss     0:02 /sbin/init
      2 ?        S      0:00 [kthreadd]
      3 ?        S      0:00 [pool_workqueue_release]
      4 ?        I<     0:00 [kworker/R-rcu_gp]
      5 ?        I<     0:00 [kworker/R-sync_wq]
      6 ?        I<     0:00 [kworker/R-kvfree_rcu_reclaim]
      7 ?        I<     0:00 [kworker/R-slub_flushwq]
      8 ?        I<     0:00 [kworker/R-netns]
     11 ?        I<     0:00 [kworker/0:0H-events_highpri]
     13 ?        I<     0:00 [kworker/R-mm_percpu_wq]
     14 ?        I      0:00 [rcu_tasks_rude_kthread]
     15 ?        I      0:00 [rcu_tasks_trace_kthread]
     16 ?        S      0:00 [ksoftirqd/0]
     17 ?        I      0:00 [rcu_sched]
     18 ?        S      0:00 [rcu_exp_par_gp_kthread_worker/0]
     19 ?        S      0:00 [rcu_exp_gp_kthread_worker]
     20 ?        S      0:00 [migration/0]
     21 ?        S      0:00 [idle_inject/0]
     22 ?        S      0:00 [cpuhp/0]
     23 ?        S      0:00 [cpuhp/1]
     24 ?        S      0:00 [idle_inject/1]
     25 ?        S      0:00 [migration/1]
     26 ?        S      0:00 [ksoftirqd/1]
     28 ?        I<     0:00 [kworker/1:0H-events_highpri]
     29 ?        S      0:00 [kdevtmpfs]
     30 ?        I<     0:00 [kworker/R-inet_frag_wq]
     31 ?        S      0:00 [kauditd]
     32 ?        S      0:00 [khungtaskd]
     33 ?        I      0:00 [kworker/u8:1-events_unbound]
     34 ?        S      0:00 [oom_reaper]
     36 ?        I<     0:00 [kworker/R-writeback]
     37 ?        S      0:00 [kcompactd0]
     38 ?        SN     0:00 [ksmd]
     39 ?        SN     0:00 [khugepaged]
     40 ?        I<     0:00 [kworker/R-kintegrityd]
     41 ?        I<     0:00 [kworker/R-kblockd]
     42 ?        I<     0:00 [kworker/R-blkcg_punt_bio]
     43 ?        S      0:00 [irq/9-acpi]
     45 ?        I<     0:00 [kworker/R-tpm_dev_wq]
     46 ?        I<     0:00 [kworker/R-ata_sff]
     47 ?        I<     0:00 [kworker/R-md]
     48 ?        I<     0:00 [kworker/R-md_bitmap]
     49 ?        I<     0:00 [kworker/R-edac-poller]
     50 ?        I<     0:00 [kworker/R-devfreq_wq]
     51 ?        S      0:00 [watchdogd]
     52 ?        I<     0:00 [kworker/1:1H-kblockd]
     53 ?        S      0:00 [kswapd0]
     54 ?        S      0:00 [ecryptfs-kthread]
     55 ?        I<     0:00 [kworker/R-kthrotld]
     56 ?        I<     0:00 [kworker/R-acpi_thermal_pm]
     57 ?        I<     0:00 [kworker/R-nvme-wq]
     58 ?        I<     0:00 [kworker/R-nvme-reset-wq]
     59 ?        I<     0:00 [kworker/R-nvme-delete-wq]
     60 ?        I<     0:00 [kworker/R-nvme-auth-wq]
     63 ?        I<     0:00 [kworker/R-mld]
     64 ?        I<     0:00 [kworker/R-ipv6_addrconf]
     71 ?        I<     0:00 [kworker/R-kstrp]
     73 ?        I<     0:00 [kworker/u9:0]
     86 ?        I<     0:00 [kworker/R-charger_manager]
     87 ?        I<     0:00 [kworker/0:1H-kblockd]
     88 ?        S      0:00 [jbd2/nvme0n1p1-8]
     89 ?        I<     0:00 [kworker/R-ext4-rsv-conversion]
    128 ?        S<s    0:00 /usr/lib/systemd/systemd-journald
    149 ?        I      0:00 [kworker/1:2-events]
    152 ?        I<     0:00 [kworker/R-kmpathd]
    153 ?        I<     0:00 [kworker/R-kmpath_handlerd]
    189 ?        SLsl   0:00 /sbin/multipathd -d -s
    194 ?        Ss     0:00 /usr/lib/systemd/systemd-udevd
    212 ?        S      0:00 [psimon]
    256 ?        I<     0:00 [kworker/R-ena]
    257 ?        I<     0:00 [kworker/R-cryptd]
    287 ?        S      0:00 [jbd2/nvme0n1p16-8]
    288 ?        I<     0:00 [kworker/R-ext4-rsv-conversion]
    332 ?        I      0:00 [kworker/0:3-events]
    335 ?        Ss     0:00 /usr/lib/systemd/systemd-resolved
    473 ?        Ss     0:00 /usr/lib/systemd/systemd-networkd
    513 ?        Ss     0:00 /usr/sbin/acpid
    517 ?        Ss     0:00 /usr/sbin/cron -f -P
    518 ?        Ss     0:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
    523 ?        Ssl    0:00 /usr/sbin/irqbalance
    525 ?        Ss     0:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --run-startup-triggers
    527 ?        Ssl    0:00 /usr/lib/polkit-1/polkitd --no-debug
    549 ?        Ss     0:00 /usr/lib/systemd/systemd-logind
    554 ?        Ssl    0:00 /usr/libexec/udisks2/udisksd
    601 ttyS0    Ss+    0:00 /sbin/agetty -o -p -- \u --keep-baud 115200,57600,38400,9600 - vt220
    632 ?        Ssl    0:00 /usr/sbin/rsyslogd -n -iNONE
    640 ?        S      0:00 /usr/sbin/chronyd -F 1
    648 ?        S      0:00 /usr/sbin/chronyd -F 1
    668 tty1     Ss+    0:00 /sbin/agetty -o -p -- \u --noclear - linux
    690 ?        Ssl    0:00 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade-shutdown --wait-for-signal
    753 ?        Ssl    0:00 /usr/sbin/ModemManager
    909 ?        Ss     0:00 sshd: /usr/sbin/sshd -D -o AuthorizedKeysCommand /usr/share/ec2-instance-connect/eic_run_authorized_keys %u %f -o AuthorizedKeysComm
    910 ?        Ss     0:00 sshd: ubuntu [priv]
   1213 ?        Ss     0:00 /usr/lib/systemd/systemd --user
   1214 ?        S      0:00 (sd-pam)
   1326 ?        S      0:00 sshd: ubuntu@pts/0
   1361 ?        I<     0:00 [kworker/R-tls-strp]
   1363 pts/0    Ss     0:00 -bash
   1606 ?        Ssl    0:02 /snap/snapd/current/usr/lib/snapd/snapd
   1978 ?        S      0:00 [psimon]
   1980 ?        Ssl    0:01 /snap/amazon-ssm-agent/12322/amazon-ssm-agent
   2094 ?        I      0:00 [kworker/u8:0-events_unbound]
   2114 ?        I      0:00 [kworker/1:1-events]
   2125 ?        I      0:00 [kworker/u8:4-events_power_efficient]
   2126 ?        I      0:00 [kworker/0:0-cgroup_destroy]
   2164 pts/0    R+     0:00 ps -ax
ubuntu@ip-172-31-21-105:~$ 



#########################Service check ########################**
ubuntu@ip-172-31-21-105:~$ systemctl status rsyslog.service
● rsyslog.service - System Logging Service
     Loaded: loaded (/usr/lib/systemd/system/rsyslog.service; enabled; preset: enabled)
     Active: active (running) since Thu 2026-02-05 08:13:01 UTC; 1h 7min ago
TriggeredBy: ● syslog.socket
       Docs: man:rsyslogd(8)
             man:rsyslog.conf(5)
             https://www.rsyslog.com/doc/
   Main PID: 632 (rsyslogd)
      Tasks: 4 (limit: 1017)
     Memory: 3.1M (peak: 5.1M)
        CPU: 229ms
     CGroup: /system.slice/rsyslog.service
             └─632 /usr/sbin/rsyslogd -n -iNONE

Feb 05 08:13:00 ip-172-31-21-105 systemd[1]: Starting rsyslog.service - System Logging Service...
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2312.0]
Feb 05 08:13:01 ip-172-31-21-105 systemd[1]: Started rsyslog.service - System Logging Service.
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's groupid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's userid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: [origin software="rsyslogd" swVersion="8.2312.0" x-pid="632" x-info="https://www.rsyslog.com"] start
ubuntu@ip-172-31-21-105:~$ 





ubuntu@ip-172-31-21-105:~$ systemctl is-active rsyslog.service 
active
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 



ubuntu@ip-172-31-21-105:/etc/ssh$ 
ubuntu@ip-172-31-21-105:/etc/ssh$ systemctl is-enabled rsyslog.service 
enabled
ubuntu@ip-172-31-21-105:/etc/ssh$ 
ubuntu@ip-172-31-21-105:/etc/ssh$ 



#########################Log check ########################
ubuntu@ip-172-31-21-105:~$ journalctl -u rsyslog.service
Jan 29 09:23:17 ip-172-31-21-105 systemd[1]: Starting rsyslog.service - System Logging Service...
Jan 29 09:23:18 ip-172-31-21-105 rsyslogd[793]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2312.0]
Jan 29 09:23:18 ip-172-31-21-105 rsyslogd[793]: rsyslogd's groupid changed to 102
Jan 29 09:23:18 ip-172-31-21-105 rsyslogd[793]: rsyslogd's userid changed to 102
Jan 29 09:23:18 ip-172-31-21-105 rsyslogd[793]: [origin software="rsyslogd" swVersion="8.2312.0" x-pid="793" x-info="https://www.rsyslog.com"] start
Jan 29 09:23:18 ip-172-31-21-105 systemd[1]: Started rsyslog.service - System Logging Service.
Jan 29 12:15:13 ip-172-31-21-105 rsyslogd[793]: [origin software="rsyslogd" swVersion="8.2312.0" x-pid="793" x-info="https://www.rsyslog.com"] exiting on signal>
Jan 29 12:15:13 ip-172-31-21-105 systemd[1]: Stopping rsyslog.service - System Logging Service...
Jan 29 12:15:13 ip-172-31-21-105 systemd[1]: rsyslog.service: Deactivated successfully.
Jan 29 12:15:13 ip-172-31-21-105 systemd[1]: Stopped rsyslog.service - System Logging Service.
-- Boot c2d8c109214b418681242e2d988971db --
Feb 05 08:13:00 ip-172-31-21-105 systemd[1]: Starting rsyslog.service - System Logging Service...
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2312.0]
Feb 05 08:13:01 ip-172-31-21-105 systemd[1]: Started rsyslog.service - System Logging Service.
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's groupid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's userid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: [origin software="rsyslogd" swVersion="8.2312.0" x-pid="632" x-info="https://www.rsyslog.com"] start
lines 1-17/17 (END)



ubuntu@ip-172-31-21-105:~$ journalctl -u rsyslog.service | tail -n 5
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2312.0]
Feb 05 08:13:01 ip-172-31-21-105 systemd[1]: Started rsyslog.service - System Logging Service.
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's groupid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: rsyslogd's userid changed to 102
Feb 05 08:13:01 ip-172-31-21-105 rsyslogd[632]: [origin software="rsyslogd" swVersion="8.2312.0" x-pid="632" x-info="https://www.rsyslog.com"] start
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 





############################ Mini troubleshooting steps ###########################################

Issue :
sshd service not running

Troubleshooting steps :
1. Verify the status of sshd service & check the state of that service (running/failed)
2. Via service check command verify from which date it has been in failed state.
3. Verify the log file of sshd from /var/log/sshd/ssh file or check in /var/log/dmesg file if anything mentioned about sshd service.
4. Another way, to check it in the file (/usr/lib/systemd/system/ssh.service & /etc/ssh/sshd_config) whether the content is fine or if anything is changed/wrong/parameteres set incorrectly.
5. Another way, verify your ssh connectivity whether its working properly (ssh user@ip)

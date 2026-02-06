1. Capture a quick health snapshot (CPU, memory, disk, network) :

CPU/Memory :
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ free -h
               total        used        free      shared  buff/cache   available
Mem:           914Mi       360Mi       245Mi       2.7Mi       471Mi       553Mi
Swap:             0B          0B          0B
ubuntu@ip-172-31-21-105:~$ 


top - 10:42:54 up  3:57,  2 users,  load average: 0.08, 0.02, 0.01
Tasks: 112 total,   1 running, 111 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st 
MiB Mem :    914.2 total,    233.6 free,    371.0 used,    472.9 buff/cache     
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    543.2 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                   
      1 root      20   0   22564  13892   9608 S   0.0   1.5   0:01.80 systemd                                                                   
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd                                                                  
      3 root      20   0       0      0      0 S   0.0   0.0   0:00.00 pool_workqueue_release                                                    
      4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-rcu_gp                                                          
      5 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-sync_wq                                                         
      6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-kvfree_rcu_reclaim                                              
      7 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-slub_flushwq                                                    
      8 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-netns                                                           
     10 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/0:0H-events_highpri                                               
     13 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-mm_percpu_wq                                                    
     14 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_rude_kthread                                                    
     15 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_trace_kthread                                                   
     16 root      20   0       0      0      0 S   0.0   0.0   0:00.02 ksoftirqd/0                                                               
     17 root      20   0       0      0      0 I   0.0   0.0   0:00.22 rcu_sched                                                                 
     18 root      20   0       0      0      0 S   0.0   0.0   0:00.00 rcu_exp_par_gp_kthread_worker/0                                           
     19 root      20   0       0      0      0 S   0.0   0.0   0:00.00 rcu_exp_gp_kthread_worker                                                 
     20 root      rt   0       0      0      0 S   0.0   0.0   0:00.05 migration/0                                                               
     21 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/0                                                             
     22 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/0                                                                   
     23 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/1                                                                   
     24 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/1                                                             
     25 root      rt   0       0      0      0 S   0.0   0.0   0:00.10 migration/1                                                               
     26 root      20   0       0      0      0 S   0.0   0.0   0:00.04 ksoftirqd/1                                                               
     28 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/1:0H-events_highpri                                               
     29 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kdevtmpfs                                                                 
     30 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-inet_frag_wq                                                    
     31 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kauditd                                                                   
     32 root      20   0       0      0      0 S   0.0   0.0   0:00.00 khungtaskd                                                                
     34 root      20   0       0      0      0 S   0.0   0.0   0:00.00 oom_reaper                                                                
     36 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-writeback                                                       
     37 root      20   0       0      0      0 S   0.0   0.0   0:00.48 kcompactd0                                                                
     38 root      25   5       0      0      0 S   0.0   0.0   0:00.00 ksmd                                                                      
     39 root      39  19       0      0      0 S   0.0   0.0   0:00.00 khugepaged                                                                
     40 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-kintegrityd                                                     
     41 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-kblockd                                                         
     42 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-blkcg_punt_bio                                                  
     44 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 irq/9-acpi                                                                
     45 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/R-tpm_dev_wq                                                      


ubuntu@ip-172-31-21-105:~$ vmstat 
procs -----------memory---------- ---swap-- -----io---- -system-- -------cpu-------
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st gu
 0  0      0  77188  14968 618740    0    0    31    35   54    0  0  0 100  0  0  0
ubuntu@ip-172-31-21-105:~$ 


Disk/IO :
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ df -h
Filesystem       Size  Used Avail Use% Mounted on
/dev/root         29G  1.9G   27G   7% /
tmpfs            458M     0  458M   0% /dev/shm
tmpfs            183M  884K  182M   1% /run
tmpfs            5.0M     0  5.0M   0% /run/lock
efivarfs         128K  3.8K  120K   4% /sys/firmware/efi/efivars
/dev/nvme0n1p16  881M   89M  730M  11% /boot
/dev/nvme0n1p15  105M  6.2M   99M   6% /boot/efi
tmpfs             92M   12K   92M   1% /run/user/1000
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ iostat 
Linux 6.14.0-1018-aws (ip-172-31-21-105) 	02/06/26 	_x86_64_	(2 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
           0.05    0.00    0.04    0.03    0.00   99.88

Device             tps    kB_read/s    kB_wrtn/s    kB_dscd/s    kB_read    kB_wrtn    kB_dscd
loop0             0.00         0.02         0.00         0.00        345          0          0
loop1             0.01         0.30         0.00         0.00       4271          0          0
loop2             0.00         0.08         0.00         0.00       1097          0          0
loop3             0.00         0.02         0.00         0.00        346          0          0
loop4             0.04         1.57         0.00         0.00      22472          0          0
loop5             0.00         0.00         0.00         0.00         14          0          0
nvme0n1           1.28        25.45         7.01         0.00     364331     100326          0


ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ du -sh
60K	.
ubuntu@ip-172-31-21-105:~$ 



Network :

ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ ping google.com
PING google.com (216.58.211.14) 56(84) bytes of data.
64 bytes from muc03s13-in-f14.1e100.net (216.58.211.14): icmp_seq=1 ttl=119 time=3.16 ms
64 bytes from muc03s13-in-f14.1e100.net (216.58.211.14): icmp_seq=2 ttl=119 time=3.16 ms
64 bytes from muc03s13-in-f14.1e100.net (216.58.211.14): icmp_seq=3 ttl=119 time=3.17 ms
64 bytes from muc03s13-in-f14.1e100.net (216.58.211.14): icmp_seq=4 ttl=119 time=3.17 ms
^C
--- google.com ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3004ms
rtt min/avg/max/mdev = 3.155/3.166/3.174/0.007 ms
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ curl google.com
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 


ubuntu@ip-172-31-21-105:~$ netstat -tulpn
(No info could be read for "-p": geteuid()=1000 but you should be root.)
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name    
tcp        0      0 127.0.0.54:53           0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN      -                   
tcp        0      0 0.0.0.0:80              0.0.0.0:*               LISTEN      -                   
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      -                   
tcp6       0      0 :::80                   :::*                    LISTEN      -                   
tcp6       0      0 :::22                   :::*                    LISTEN      -                   
udp        0      0 127.0.0.54:53           0.0.0.0:*                           -                   
udp        0      0 127.0.0.53:53           0.0.0.0:*                           -                   
udp        0      0 172.31.21.105:68        0.0.0.0:*                           -                   
udp        0      0 127.0.0.1:323           0.0.0.0:*                           -                   
udp6       0      0 ::1:323                 :::*                                -                   
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 


2. Trace logs for that service :

-Nginx service 
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: active (running) since Fri 2026-02-06 07:31:29 UTC; 3h 16min ago
       Docs: man:nginx(8)
    Process: 1620 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 1622 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 1652 (nginx)
      Tasks: 3 (limit: 1017)
     Memory: 2.4M (peak: 5.3M)
        CPU: 20ms
     CGroup: /system.slice/nginx.service
             ├─1652 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             ├─1654 "nginx: worker process"
             └─1655 "nginx: worker process"

Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ sudo systemctl stop nginx.service 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
○ nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: inactive (dead) since Fri 2026-02-06 10:48:35 UTC; 2s ago
   Duration: 3h 17min 5.456s
       Docs: man:nginx(8)
    Process: 1620 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 1622 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 2578 ExecStop=/sbin/start-stop-daemon --quiet --stop --retry QUIT/5 --pidfile /run/nginx.pid (code=exited, status=0/SUCCESS)
   Main PID: 1652 (code=exited, status=0/SUCCESS)
        CPU: 23ms

Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: nginx.service: Deactivated successfully.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ sudo systemctl disable nginx.service 
Synchronizing state of nginx.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install disable nginx
Removed "/etc/systemd/system/multi-user.target.wants/nginx.service".
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
○ nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; disabled; preset: enabled)
     Active: inactive (dead)
       Docs: man:nginx(8)

Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: nginx.service: Deactivated successfully.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ sudo systemctl enable nginx.service 
Synchronizing state of nginx.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install enable nginx
Created symlink /etc/systemd/system/multi-user.target.wants/nginx.service → /usr/lib/systemd/system/nginx.service.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
○ nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: inactive (dead)
       Docs: man:nginx(8)

Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: nginx.service: Deactivated successfully.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ sudo systemctl start nginx.service 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: active (running) since Fri 2026-02-06 10:49:37 UTC; 3s ago
       Docs: man:nginx(8)
    Process: 3386 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 3388 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 3389 (nginx)
      Tasks: 3 (limit: 1017)
     Memory: 3.6M (peak: 3.8M)
        CPU: 11ms
     CGroup: /system.slice/nginx.service
             ├─3389 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             ├─3390 "nginx: worker process"
             └─3391 "nginx: worker process"

Feb 06 10:49:37 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:49:37 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$


Logs :
ubuntu@ip-172-31-21-105:~$ sudo journalctl -u nginx.service
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 07:31:29 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: nginx.service: Deactivated successfully.
Feb 06 10:48:35 ip-172-31-21-105 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
Feb 06 10:49:37 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 06 10:49:37 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 



3. Write a mini runbook describing what you did and what you’d do next if things were worse :

Scenario : 
- Stopped the service then disabled it.

If things get more worse then I would first check the service logs with its day/date/time to check when it has started to show the error next will check the logs line by line. If nothing is wrong then will go for configuration file checking. If anything is wrong in the configuration file then also service gets affected. Will check for network connection as well.


Environment basics :

ubuntu@ip-172-31-21-105:~$ uname -a
Linux ip-172-31-21-105 6.14.0-1018-aws #18~24.04.1-Ubuntu SMP Mon Nov 24 19:46:27 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ cat /etc/os-release 
PRETTY_NAME="Ubuntu 24.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.3 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo


Filesystem sanity :

ubuntu@ip-172-31-21-105:~$ mkdir -p devops/test/runbook-demo/
ubuntu@ip-172-31-21-105:~$ ll
total 52
drwxr-x--- 6 ubuntu ubuntu 4096 Feb  6 11:02 ./
drwxr-xr-x 4 root   root   4096 Feb  6 10:12 ../
-rw------- 1 ubuntu ubuntu 1535 Feb  6 09:43 .bash_history
-rw-r--r-- 1 ubuntu ubuntu  220 Mar 31  2024 .bash_logout
-rw-r--r-- 1 ubuntu ubuntu 3771 Mar 31  2024 .bashrc
drwx------ 2 ubuntu ubuntu 4096 Jan 29 09:23 .cache/
drwx------ 4 ubuntu ubuntu 4096 Feb  6 10:42 .config/
-rw------- 1 ubuntu ubuntu   20 Feb  6 10:52 .lesshst
-rw-r--r-- 1 ubuntu ubuntu  807 Mar 31  2024 .profile
drwx------ 2 ubuntu ubuntu 4096 Jan 29 09:23 .ssh/
-rw-r--r-- 1 ubuntu ubuntu    0 Feb  5 09:54 .sudo_as_admin_successful
-rw------- 1 ubuntu ubuntu  983 Feb  5 09:53 .viminfo
-rw-rw-r-- 1 test   test      4 Feb  6 10:13 a.txt
drwxrwxr-x 3 ubuntu ubuntu 4096 Feb  6 11:02 devops/
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ ll devops/
total 12
drwxrwxr-x 3 ubuntu ubuntu 4096 Feb  6 11:02 ./
drwxr-x--- 6 ubuntu ubuntu 4096 Feb  6 11:02 ../
drwxrwxr-x 3 ubuntu ubuntu 4096 Feb  6 11:02 test/
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ ll devops/test/
total 12
drwxrwxr-x 3 ubuntu ubuntu 4096 Feb  6 11:02 ./
drwxrwxr-x 3 ubuntu ubuntu 4096 Feb  6 11:02 ../
drwxrwxr-x 2 ubuntu ubuntu 4096 Feb  6 11:02 runbook-demo/
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ sudo cp /etc/hosts devops/test/runbook-demo/hosts-copy
ubuntu@ip-172-31-21-105:~$ ls -l devops/test/runbook-demo/
total 4
-rw-r--r-- 1 root root 221 Feb  6 11:03 hosts-copy
ubuntu@ip-172-31-21-105:~$ 




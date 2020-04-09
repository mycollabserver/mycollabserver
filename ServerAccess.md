## Server Access Details
Keep up to date info, change to ssh keygen access with 2fa ASAP.

### 139.59.90.239
Digital Ocean droplet (smallest?)
#### details
```
root@collab-server-32:~# hostname -f
collab-server-32
root@collab-server-32:~# uname -a
Linux collab-server-32 4.4.0-176-generic #206-Ubuntu SMP Fri Feb 28 05:00:50 UTC 2020 i686 i686 i686 GNU/Linux
root@collab-server-32:~# cat /proc/cpuinfo 
processor	: 0
vendor_id	: GenuineIntel
cpu family	: 6
model		: 79
model name	: Intel(R) Xeon(R) CPU E5-2650 v4 @ 2.20GHz
stepping	: 1
microcode	: 0x1
cpu MHz		: 2199.996
cache size	: 30720 KB
physical id	: 0
siblings	: 1
core id		: 0
cpu cores	: 1
apicid		: 0
initial apicid	: 0
fdiv_bug	: no
f00f_bug	: no
coma_bug	: no
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon tsc_known_freq pni pclmulqdq vmx ssse3 fma cx16 sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch ssbd ibrs ibpb tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs taa itlb_multihit
bogomips	: 4399.99
clflush size	: 64
cache_alignment	: 64
address sizes	: 40 bits physical, 48 bits virtual
power management:

root@collab-server-32:~# df -h
Filesystem      Size  Used Avail Use% Mounted on
udev            493M     0  493M   0% /dev
tmpfs           100M   15M   86M  15% /run
/dev/vda1        25G  2.8G   22G  12% /
tmpfs           500M     0  500M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           500M     0  500M   0% /sys/fs/cgroup
tmpfs           100M     0  100M   0% /run/user/1001
root@collab-server-32:~# free -h
              total        used        free      shared  buff/cache   available
Mem:           999M         81M        133M         24M        784M        712M
Swap:            0B          0B          0B
root@collab-server-32:~# 

```

#### ssh
webg@139.59.90.239 port 22 passwd collab . in

#### More

```
root@collab-server-32:~# netstat -nlpt
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 0.0.0.0:10000           0.0.0.0:*               LISTEN      1754/perl       
tcp        0      0 127.0.0.1:8080          0.0.0.0:*               LISTEN      1729/apache2    
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      1695/sshd       
tcp6       0      0 :::8080                 :::*                    LISTEN      1729/apache2    
tcp6       0      0 :::22                   :::*                    LISTEN      1695/sshd       
root@collab-server-32:~# systemctl status
● collab-server-32
    State: degraded
     Jobs: 0 queued
   Failed: 3 units
    Since: Sun 2020-04-05 07:11:22 UTC; 4 days ago
   CGroup: /
           ├─init.scope
           │ └─1 /sbin/init
           ├─system.slice
           │ ├─mdadm.service
           │ │ └─1685 /sbin/mdadm --monitor --pid-file /run/mdadm/monitor.pid --daemonise --scan --syslog
           │ ├─dbus.service
           │ │ └─1548 /usr/bin/dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation
           │ ├─cron.service
           │ │ └─1525 /usr/sbin/cron -f
           │ ├─lvm2-lvmetad.service
           │ │ └─657 /sbin/lvmetad -f
           │ ├─apache2.service
           │ │ ├─ 1729 /usr/sbin/apache2 -k start
           │ │ ├─32420 /usr/sbin/apache2 -k start
           │ │ ├─32421 /usr/sbin/apache2 -k start
           │ │ ├─32422 /usr/sbin/apache2 -k start
           │ │ ├─32423 /usr/sbin/apache2 -k start
           │ │ └─32424 /usr/sbin/apache2 -k start
           │ ├─iscsid.service
           │ │ ├─1590 /sbin/iscsid
           │ │ └─1591 /sbin/iscsid
           │ ├─unattended-upgrades.service
           │ │ └─1645 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade-shutdown --wait-for-signal
           │ ├─webmin.service
           │ │ └─1754 /usr/bin/perl /usr/share/webmin/miniserv.pl /etc/webmin/miniserv.conf
           │ ├─accounts-daemon.service
           │ │ └─1542 /usr/lib/accountsservice/accounts-daemon
           │ ├─system-serial\x2dgetty.slice
           │ │ └─serial-getty@ttyS0.service
           │ │   └─1661 /sbin/agetty --keep-baud 115200 38400 9600 ttyS0 vt220
           │ ├─atd.service
           │ │ └─1576 /usr/sbin/atd -f
           │ ├─systemd-journald.service
           │ │ └─644 /lib/systemd/systemd-journald
           │ ├─systemd-timesyncd.service
           │ │ └─799 /lib/systemd/systemd-timesyncd
           │ ├─ssh.service
           │ │ ├─1695 /usr/sbin/sshd -D
           │ │ ├─6490 sshd: [accepted]    
           │ │ ├─6491 sshd: [net]         
           │ │ └─6501 sshd: [accepted]    
           │ ├─systemd-logind.service
           │ │ └─1569 /lib/systemd/systemd-logind
           │ ├─php7.3-fpm.service
           │ │ ├─1532 php-fpm: master process (/etc/php/7.3/fpm/php-fpm.conf)                      
           │ │ ├─1714 php-fpm: pool www                                                            
           │ │ └─1715 php-fpm: pool www                                                            
           │ ├─system-getty.slice
           │ │ └─getty@tty1.service
           │ │   └─1665 /sbin/agetty --noclear tty1 linux
           │ ├─systemd-udevd.service
           │ │ └─1446 /lib/systemd/systemd-udevd
           │ ├─polkitd.service
           │ │ └─1648 /usr/lib/policykit-1/polkitd --no-debug
           │ ├─php7.0-fpm.service
           │ │ ├─1547 php-fpm: master process (/etc/php/7.0/fpm/php-fpm.conf)                      
           │ │ ├─1721 php-fpm: pool www                                                            
           │ │ ├─1722 php-fpm: pool www                                                            
           │ │ ├─1723 php-fpm: pool www                                                            
           │ │ ├─1724 php-fpm: pool www                                                            
           │ │ ├─1725 php-fpm: pool www                                                            
           │ │ ├─1726 php-fpm: pool www                                                            
           │ │ ├─1727 php-fpm: pool www                                                            
           │ │ ├─1728 php-fpm: pool www                                                            
           │ │ ├─1737 php-fpm: pool www                                                            
           │ │ └─1738 php-fpm: pool www                                                            
           │ ├─rsyslog.service
           │ │ └─1512 /usr/sbin/rsyslogd -n
           │ ├─lxcfs.service
           │ │ └─1537 /usr/bin/lxcfs /var/lib/lxcfs/
           │ └─acpid.service
           │   └─1536 /usr/sbin/acpid

```

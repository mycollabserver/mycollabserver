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

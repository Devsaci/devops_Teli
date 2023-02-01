# C:\Users\Zakaria\vagrant-vms\ubuntu18> vagrant global-status 
output : 
id       name    provider   state    directory                             
--------------------------------------------------------------------------
7ea06e1  default virtualbox running C:/Users/Zakaria/vagrant-vms/ubuntu18 
3263d84  default virtualbox running C:/Users/Zakaria/vagrant-vms/centos7  
 
The above shows information about all known Vagrant environments
on this machine. This data is cached and may not be completely
up-to-date (use "vagrant global-status --prune" to prune invalid
entries). To interact with any of the machines, you can go to that
directory and run Vagrant, or you can use the ID directly with
Vagrant commands from any directory. For example:
"vagrant destroy 1a2b3c4d"

# C:\Users\Zakaria\vagrant-vms\ubuntu18> vagrant status
output : 
Current machine states:

default                   running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.

# PS C:\Users\Zakaria\vagrant-vms\ubuntu18> vagrant reload
output :
==> default: Attempting graceful shutdown of VM...
==> default: Checking if box 'geerlingguy/ubuntu1804' version '1.1.10' is up to date...
==> default: Clearing any previously set forwarded ports...
==> default: Clearing any previously set network interfaces...
==> default: Available bridged network interfaces:
1) Intel(R) 82579V Gigabit Network Connection
2) Hyper-V Virtual Ethernet Adapter
==> default: When choosing an interface, it is usually the one that is
==> default: being used to connect to the internet.
==> default:
    default: Which interface should the network bridge to?
    default: Which interface should the network bridge to?
    default: Which interface should the network bridge to? 192.168.33.10
    default: Which interface should the network bridge to? public_network
    default: Which interface should the network bridge to? d
    default: Which interface should the network bridge to? y
    default: Which interface should the network bridge to? n
    default: Which interface should the network bridge to? 0
    default: Which interface should the network bridge to? 1
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
    default: Adapter 2: hostonly
    default: Adapter 3: bridged
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 6.1.32 r149290
    default: VirtualBox Version: 7.0
==> default: Configuring and enabling network interfaces...
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Zakaria/vagrant-vms/ubuntu18
==> default: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> default: flag to force provisioning. Provisioners marked to run always will still run.


# PS C:\Users\Zakaria\vagrant-vms\ubuntu18> vagrant ssh
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 4.15.0-156-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
New release '20.04.5 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


#  whoami
vagrant@vagrant:~$ whoami
vagrant

# free -m
vagrant@vagrant:~$  # free -m
              total        used        free      shared  buff/cache   available
Mem:           1550          66        1153           0         330        1342
Swap:           979           0         979
vagrant@vagrant:~$

# ifconfig
vagrant@vagrant:~$ ifconfig
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:fe78:8ef1  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:78:8e:f1  txqueuelen 1000  (Ethernet)
        RX packets 896  bytes 284073 (284.0 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 596  bytes 92746 (92.7 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s8: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.33.10  netmask 255.255.255.0  broadcast 192.168.33.255
        inet6 fe80::a00:27ff:fec0:2b02  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:c0:2b:02  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 14  bytes 1076 (1.0 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s9: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.62  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::a00:27ff:fe84:c198  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:84:c1:98  txqueuelen 1000  (Ethernet)
        RX packets 645  bytes 39802 (39.8 KB)
        RX errors 0  dropped 614  overruns 0  frame 0
        TX packets 25  bytes 2891 (2.8 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 6  bytes 544 (544.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 544 (544.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

# exit
vagrant@vagrant:~$ exit
logout
Connection to 127.0.0.1 closed.
PS C:\Users\Zakaria\vagrant-vms\ubuntu18>


# PS C:\Users\Zakaria\vagrant-vms\ubuntu18> vagrant ssh
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 4.15.0-156-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
New release '20.04.5 LTS' available.
Run 'do-release-upgrade' to upgrade to it.

Last login: Wed Jan 25 11:40:06 2023 from 10.0.2.2
vagrant@vagrant:~$

# vagrant@vagrant:~$ free -m
              total        used        free      shared  buff/cache   available
Mem:           1550          69        1150           0         330        1339
Swap:           979           0         979
vagrant@vagrant:~$

# vagrant@vagrant:~$ ls -al
vagrant@vagrant:~$ ls
vagrant@vagrant:~$ ls -al
total 44
drwxr-xr-x 6 vagrant vagrant 4096 Jan 24 22:07 .
drwxr-xr-x 3 root    root    4096 Feb 12  2022 ..
drwx------ 3 vagrant vagrant 4096 Feb 12  2022 .ansible
-rw------- 1 vagrant vagrant   65 Jan 24 22:07 .bash_history
-rw-r--r-- 1 vagrant vagrant  220 Feb 12  2022 .bash_logout
-rw-r--r-- 1 vagrant vagrant 3771 Feb 12  2022 .bashrc
drwx------ 2 vagrant vagrant 4096 Feb 12  2022 .cache
drwx------ 3 vagrant vagrant 4096 Feb 12  2022 .gnupg
-rw-r--r-- 1 vagrant vagrant  807 Feb 12  2022 .profile
drwx------ 2 vagrant vagrant 4096 Jan 24 20:16 .ssh
-rw-r--r-- 1 vagrant vagrant    0 Feb 12  2022 .sudo_as_admin_successful
-rw-r--r-- 1 vagrant vagrant    6 Feb 12  2022 .vbox_version

# vagrant@vagrant:~$ cat /etc/os-release
NAME="Ubuntu"
VERSION="18.04.6 LTS (Bionic Beaver)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 18.04.6 LTS"
VERSION_ID="18.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=bionic
UBUNTU_CODENAME=bionic
vagrant@vagrant:~$

# vagrant@vagrant:~$ sudo -i
root@vagrant:~#

# root@vagrant:~# whoami
root
root@vagrant:~#

# root@vagrant:~# pwd
/root
root@vagrant:~#

# root@vagrant:~# ls
# root@vagrant:~# ls -a
.  ..  .bashrc  .profile
# root@vagrant:~# ls -al
total 16
drwx------  2 root root 4096 Feb 12  2022 .
drwxr-xr-x 23 root root 4096 Jan 24 20:16 ..
-rw-r--r--  1 root root 3106 Apr  9  2018 .bashrc
-rw-r--r--  1 root root  148 Aug 17  2015 .profile
root@vagrant:~#

# vagrant@vagrant:~$ /vagrant/devopsdir/./bashfiles1.sh
welcome to bash scripting.
Get:1 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]
..
..
..
eading state information... Done
152 packages can be upgraded. Run 'apt list --upgradable' to see them.
Completed successfullyvagrant
vagrant@vagrant:~$

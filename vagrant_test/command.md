

# vagrant init ubuntu/xenial64
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant init ubuntu/xenial64
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>

#########################################################################

# vagrant init ubuntu/xenial64
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant init ubuntu/xenial64
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'ubuntu/xenial64' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'ubuntu/xenial64'
    default: URL: https://vagrantcloud.com/ubuntu/xenial64
==> default: Adding box 'ubuntu/xenial64' (v20211001.0.0) for provider: virtualbox
    default: Downloading: https://vagrantcloud.com/ubuntu/boxes/xenial64/versions/20211001.0.0/providers/virtualbox.box
Download redirected to host: cloud-images.ubuntu.com
    default:
==> default: Successfully added box 'ubuntu/xenial64' (v20211001.0.0) for 'virtualbox'!
==> default: Importing base box 'ubuntu/xenial64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/xenial64' version '20211001.0.0' is up to date...
==> default: Setting the name of the VM: vagrant_test_default_1674721263076_82566
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default: Warning: Connection aborted. Retrying...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 5.1.38
    default: VirtualBox Version: 7.0
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Zakaria/vagrant-vms/vagrant_test


# vagrant status
    PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant status
Current machine states:

default                   running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>

# vagrant global-status
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant global-status
id       name    provider   state   directory
------------------------------------------------------------------------------
7ea06e1  default virtualbox running C:/Users/Zakaria/vagrant-vms/ubuntu18
3263d84  default virtualbox running C:/Users/Zakaria/vagrant-vms/centos7
181409a  default virtualbox running C:/Users/Zakaria/vagrant-vms/vagrant_test

The above shows information about all known Vagrant environments
on this machine. This data is cached and may not be completely
up-to-date (use "vagrant global-status --prune" to prune invalid
entries). To interact with any of the machines, you can go to that
directory and run Vagrant, or you can use the ID directly with
Vagrant commands from any directory. For example:
"vagrant destroy 1a2b3c4d"
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>

# vagrant ssh
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant ssh
Welcome to Ubuntu 16.04.7 LTS (GNU/Linux 4.4.0-210-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

UA Infra: Extended Security Maintenance (ESM) is not enabled.

0 updates can be applied immediately.

45 additional security updates can be applied with UA Infra: ESM
Learn more about enabling UA Infra: ESM service for Ubuntu 16.04 at
https://ubuntu.com/16-04

New release '18.04.6 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


vagrant@ubuntu-xenial:~$

# ~$ sudo -i  / ~# whoami
vagrant@ubuntu-xenial:~$ sudo -i
root@ubuntu-xenial:~# whoami
root
root@ubuntu-xenial:~#

# ~# exit
root@ubuntu-xenial:~# exit
logout
vagrant@ubuntu-xenial:~$

# ~$ sudo apt update
vagrant@ubuntu-xenial:~$ sudo apt update


# vagrant destroy
vagrant@ubuntu-xenial:~$ vagrant destroy
The program 'vagrant' is currently not installed. To run 'vagrant' please ask your administrator to install the package 'vagrant'

# ~$ exit
vagrant@ubuntu-xenial:~$ exit
logout
Connection to 127.0.0.1 closed.

# vagrant destroy
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant destroy
    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Forcing shutdown of VM...
==> default: Destroying VM and associated drives...
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>


# vagrant up
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'ubuntu/xenial64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/xenial64' version '20211001.0.0' is up to date...
==> default: Setting the name of the VM: vagrant_test_default_1674724183611_38433
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
see
    default: shared folder errors, please make sure the guest additions within thee
    default: virtual machine match the version of VirtualBox you have installed onn
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 5.1.38
    default: VirtualBox Version: 7.0
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Zakaria/vagrant-vms/vagrant_test
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>


# vagrant reload
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant reload
==> default: Attempting graceful shutdown of VM...
==> default: Checking if box 'ubuntu/xenial64' version '20211001.0.0' is up to date...
==> default: Clearing any previously set forwarded ports...
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default: Warning: Connection aborted. Retrying...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you
see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 5.1.38
    default: VirtualBox Version: 7.0
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Zakaria/vagrant-vms/vagrant_test
==> default: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> default: flag to force provisioning. Provisioners marked to run always will still run.
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>


# vagrant reload
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant reload

# vagrant destroy
PS C:\Users\Zakaria\vagrant-vms\vagrant_test> vagrant destroy
    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Forcing shutdown of VM...
==> default: Destroying VM and associated drives...
PS C:\Users\Zakaria\vagrant-vms\vagrant_test>

# Zakaria@Gen▒ve MINGW64 ~/vagrant-vms/ubuntu18 (main)
$ vagrant free -m
Usage: vagrant [options] <command> [<args>]

    -h, --help                       Print this help.


#  $ vagrant ssh
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 4.15.0-156-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
Last login: Wed Feb  1 11:12:44 2023 from 10.0.2.2

# vagrant@vagrant:~$ free -m
              total        used        free      shared  buff/cache   available
Mem:           1550          66        1153           0         330        1342
Swap:           979           0         979
vagrant@vagrant:~$

# vagrant@vagrant:~$ ifconfig

enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:fe78:8ef1  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:78:8e:f1  txqueuelen 1000  (Ethernet)
        RX packets 619  bytes 72157 (72.1 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 444  bytes 79877 (79.8 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s8: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.44.10  netmask 255.255.255.0  broadcast 192.168.44.255
        inet6 fe80::a00:27ff:fec0:2b02  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:c0:2b:02  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 17  bytes 1326 (1.3 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s9: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.62  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::a00:27ff:fe84:c198  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:84:c1:98  txqueuelen 1000  (Ethernet)
        RX packets 548  bytes 34229 (34.2 KB)
        RX errors 0  dropped 390  overruns 0  frame 0
        TX packets 22  bytes 2734 (2.7 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

vagrant@vagrant:~$


# Zakaria@Gen▒ve MINGW64 ~/vagrant-vms/ubuntu18 (main)
# $ touch testfile123.txt

# Zakaria@Gen▒ve MINGW64 ~/vagrant-vms/ubuntu18 (main)
# $ ls
testfile123.txt  Vagrantfile
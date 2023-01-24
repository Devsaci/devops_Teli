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

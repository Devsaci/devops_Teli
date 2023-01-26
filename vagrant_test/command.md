

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
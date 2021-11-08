# DevOps education Program - Virtualization

This module covers virtualization and Cloud Basic.
Task 2.1 is for virtualization.

## Part 1. Hypervisors

Most popular hypervisors for infrastructure virtualization are 
1- VMware vSphere / ESXi
2- Microsoft Windows server Hyper-V
3- Xen /Citrix XenServer
4- Red Hat Enterprise Virtualization (RHEV)
5- KVM

## Part 2. Work with VirtualBox


- Cloning and creating group of two VMs: 

![VMs-Groups](screenshots_of_tasks/Creating-VMs-Group.PNG)

- Working with OVA files:

![import-OVF](screenshots_of_tasks/import-OVF.png)

- Shared folder configuration:

![sharedFolder](screenshots_of_tasks/sharedFolders.png)

- Basic commands of VBoxManage:

![controlvm](screenshots_of_tasks/controlvm-poweroff.png)

![startvm](screenshots_of_tasks/startvm-command.png)

![showvminfo](screenshots_of_tasks/showvminfo-command.PNG)

## Part 3. Work with Vagrant

- Working with vagrant hashicorp/precise64 box

![precise64](screenshots_of_tasks/vagrant_precise64.png)


## Creating my Vagrant box:

- This box consists of the simple website html page that I did during task1.1. ant it is running in nginx and depends on VirtualBox.
- Follow [the link](https://app.vagrantup.com/Lina-at/boxes/test) to my box in vagrant cloud
- After you run 
```
vagrant init Lina-at/test
vagrant up
```
- Uncommit port-forwarding line in vagrantfile:

config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
and execute 
```
vagrant reload
```
- Open the website using http://127.0.0.1:8080 in your web browser and you should see my website :)
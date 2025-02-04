---
title: "FOSS Virtualization Platform For Your Home and Business: Proxmox VE"
toc: true
---

***Virtualization*** in computer systems is not a new concept by any means, we have been using hardware-assisted virtualization in computer systems  [since the 60's](https://www.youtube.com/watch?v=u6mu5B-YZU8), However they were mostly used in datacenter's or Infrastructure environments. 


Since the beginning of 2000's virtualization has been adopted by small scale servers and personal computers thanks to hypervisors, the main reason behind this was the improvement of processing power in computers allowed us to run many virtual computers in a single physical machine. Now instead of running seperate machines for each task we can create a virtual machine using a desired hypervisor and use our resources much more efficently and also environment friendly. 

But there's a problem, many of the home server runners asks which hypervisor or tool I should use? There are bunch of options you have both free or paid such as HyperV, Citrix XenServer, Vmware etc. but I think Proxmox VE wins the cake here in terms of functionality and ease of use.

`Proxmox VE is a complete, open-source server management platform for enterprise virtualization. It tightly integrates the KVM hypervisor and Linux Containers (LXC), software-defined storage and networking functionality, on a single platform. With the integrated web-based user interface you can manage VMs and containers, high availability for clusters, or the integrated disaster recovery tools with ease.`
Source : proxmox.com

Yes, Proxmox VE is open source and free to use, which makes it a viable solution for home and small to big scale business environments.

<!--more-->

---


### Advantages of using Proxmox VE

- **It's a free project:**

Which means you can use many of it's features free of charge as stated in it's website;

`The Proxmox VE source code is free, released under the GNU Affero General Public License, v3 (GNU AGPL, v3). This means that you are free to use the software, inspect the source code at any time and contribute to the project yourself.`

- **Its a feature-rich project:**

It has a lot of features which you will need when you build a home virtualization server, such as backup, management, cluster, storage management, firewall management for virtual servers etc.

- **Active Community:**

It has many active communities which you can ask for help if you face a problem, such communities are :

[Proxmox Support Forum](https://forum.proxmox.com)

[Proxmox Sub-Reddit](https://www.reddit.com/r/Proxmox/) - (Which has over 50k members at the moment)

[Proxmox Mailing Lists](https://lists.proxmox.com/cgi-bin/mailman/listinfo)

- **Easy to Install:**

It's very easy to install thanks to its GUI based installation interface which you will see in this article soon.

---

### Not Perfect

However like most things Proxmox VE is not perfect:

- Premium Features

You have to buy a subscription if you want to use Proxmox VE Enterprise Repository and update your Proxmox VE inside the management console;

`A Proxmox VE Subscription is an additional service program designed to help IT professionals and businesses to keep your Proxmox VE deployments up-to-date. A subscription provides access to the stable Proxmox VE Enterprise Repository delivering reliable software updates and security enhancements, and to technical help and support.`


However this doesn't mean that you cannot update Proxmox VE unless you pay, you can update manually and use all of the features without paying a single dollar.


---

### Hardware Requirements

**Recommended Hardware**

Intel EMT64 or AMD64 with Intel VT/AMD-V CPU flag.
Memory, minimum 2 GB for OS and Proxmox VE services. Plus designated memory for guests. For Ceph or ZFS additional memory is required, approximately 1 GB memory for every TB used storage.
Fast and redundant storage, best results with SSD disks.
OS storage: Hardware RAID with batteries protected write cache (“BBU”) or non-RAID with ZFS and SSD cache.
VM storage: For local storage use a hardware RAID with battery backed write cache (BBU) or non-RAID for ZFS. Neither ZFS nor Ceph are compatible with a hardware RAID controller. Shared and distributed storage is also possible.
Redundant Gbit NICs, additional NICs depending on the preferred storage technology and cluster setup – 10 Gbit and higher is also supported.
For PCI(e) passthrough a CPU with VT-d/AMD-d CPU flag is needed.



---


### How to Install Proxmox VE to Your Server

Since Proxmox Virtual Environment is based on Debian GNU/Linux and uses a custom Linux Kernel the installation process is very much simular to a Linux distribution, You can download the latest iso here:

https://www.proxmox.com/en/downloads/category/iso-images-pve

You can burn the iso to a usb drive or install via network, it's your choice.
Just follow the installation steps in the setup after you boot the iso.

After you install the Proxmox VE and boot the command line the web UI address will appear on the screen :

![WebUI](https://i.imgur.com/nhAzeChl.jpg)

Just go to the address from a computer on a same network and login using the root password you set during the install. That's it you can now use the Proxmox VE!


### Sources

- https://proxmox.com/
- https://forum.proxmox.com/
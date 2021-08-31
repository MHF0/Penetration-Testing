## Virtual Lap Installation

A virtual Lab is a simulated lab environment typically implemented as a software program which allows the users to perform their experiments.

### Createing TryHackMe Account

We will go to [https://tryhackme.com](https://tryhackme.com). And click to Join Now to create new account.

### Kali Linux Installtion
- Go to [https://www.kali.org/get-kali](https://www.kali.org/get-kali) and click in Download 

- Then click in Recommended

![Recommended](./img/kaliLunx-2.png)

- Finaly click in the download button

![downloadButton](./img/kaliLunx-3.png)

### Now we can dowload the VirtualBox machine

Go to [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads) and click on Windows hosts

![vBoxDownload](./img/VMBox-download.png)

Then open the  `VirtualBox-6.1.26-145957-Win` setup and download it.

## Install Kali Linux in VirtualBox

### we will change some setting in VirtualBox after install the Kali-linux

1. Create new machine:

    - Click in `new`.
    - In the `Name` section write `Kali`.
    - In the `Type` section select `Linux`.
    - In the `Version` section select `Debian (64-bit)`.
    - Change the `1024` to `4024`.
    - Press next and in the `File location size` change the `8.00 GB` to `50.0 GB`.

2. now we must change some setting

    - Go to `Settings`.
    - In the left side go to `Storage` and press in `Controller: IDE   O+` and click in `Add` then chose the `kali-linux iso file`  and press ok.
    - Go to the `Network` and select `Attached to` and choose `Bridged Adapter`.

### Note: What is `Bridged Adapter` and why we used it 

Bridged Adapter This mode is used for connecting the virtual network adapter of a VM to a physical network to which a physical network adapter of the VirtualBox host machine is connected.

A VM virtual network adapter uses the host network interface for a network connection. Put simply, network packets are sent and received directly from/to the virtual network adapter without additional routing. A special net filter driver is used by VirtualBox for a bridged network mode in order to filter data from the physical network adapter of the host.

* Note: read more about the Network visit [link](https://www.nakivo.com/blog/virtualbox-network-setting-guide)

### Now we are going to install Kali-linux

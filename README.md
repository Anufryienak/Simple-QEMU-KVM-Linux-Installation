# Simple QEMU/KVM Linux Installation
A simple tutorial for installing QEMU/KVM with GUI on pretty much any Linux distribution. Commands for the installation will be posted for the following: Arch, Fedora, and Debian.

*Step 1; Base Installation:*

Run the following commands according to your distribution:

**Arch**
```sudo pacman -S qemu virt-manager virt-viewer dnsmasq vde2 bridge-utils openbsd-netcat libguestfs```

**Fedora** 
``` sudo dnf install qemu-kvm libvirt virt-install bridge-utils virt-manager libvirt-devel virt-top libguestfs-tools guestfs-tools```

**Debian**
```sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virtinst libvirt-daemon virt-manager```


*Step 2; Start & Enable libvirtd*

>Arch, Fedora, and Debian all use systemd

```sudo systemctl start libvirtd```

```sudo systemctl enable libvirtd```

```sudo systemctl status libvirtd```


*Step 3; Add User to Libvirt Group*

```sudo usermod -aG libvirt USER```

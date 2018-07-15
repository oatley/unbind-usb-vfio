# unbind-usb-vfio
allow a pcie usb hub to be passed through to a virtual machine.

Used to allow a pcie usb hub to be passed through to a virtual machine.

This is a hacky little script that is unbinding the drivers from all usb devices
on a specific set of usb hubs, then it unbinds the kernel module xhci_hcd from
the pcie usb, finally it binds the vfio-pci kernel module to the pcie usb.

# WARNING: 
this will not work on other setups and could cause problems to computers, if you use
this make sure you read through it and change all device names and id. Use lsusb and 
lspci to determine names of devices and ids.

# Usage: 
unbind-usb-vfio -y

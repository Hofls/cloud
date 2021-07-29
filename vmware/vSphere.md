### Create new VM
* Open `VMware Cloud Director` -> Data Centers -> Virtual Machines -> NEW VM
    * Not obvious choices:
        * `Type` - NEW
        * `Boot Image` - Ubuntu.iso
        * `Size` - Custom sizing options
        * `Storage Policy` - VM default
        * `Network Adapter Type` - VMXNET3
        * `IP Mode` - Static - IP Pool
    * Press `OK`
* Install OS
    * Find created VM in list, click LAUNCH WEB CONSOLE
    * Follow installation process, create root password
    * Configure network interface (DNS, Gateway, Search...)
        * Simple way - look at the existing config in another VM, e.g. for CentOS - `nmtui`
    * Install OpenSSH server
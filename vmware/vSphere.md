### Create new VM
* Open `VMware Cloud Director` -> Data Centers -> Virtual Machines -> NEW VM
    * Not obvious choices:
        * `Type` - NEW
        * `Boot Image` - Ubuntu.iso
        * `Size` - Custom sizing options
        * `Storage Policy` - VM default
        * `Network` - (copy from any VM)
        * `Network Adapter Type` - VMXNET3
        * `IP Mode` - Static - IP Pool
    * Press `OK`
* Install OS
    * Find created VM in list, click "Launch Web Console"
    * Follow installation process, create root password
    * Configure network interface (DNS, Gateway, Search...)
        * Simple way - look at the existing config in another VM, e.g. for CentOS - `nmtui`
        * Example:
            * Subnet - 24.232.21.0/24
            * Address - 24.232.21.77 (VM ip address)
            * Gateway - 24.232.21.1 (from `nmtui`)
            * Name servers - 24.232.5.2, 24.232.5.3 (from `nmtui`)
            * Search domains - sun.lan (from `nmtui`)
    * Storage configuration:
        * Pick `Use an entire disk`
        * Unpick `Set up this disk as an LVM group`
            * With default LVM group only small amount of space will be available 
    * Install OpenSSH server
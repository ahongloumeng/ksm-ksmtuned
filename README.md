# ksm-ksmtuned
After centos install qemu 2.4.1, the ksmtuned will be not avaiable to ksm 

Source come from https://git.centos.org/summary/rpms!qemu-kvm

Code change a little at the row of 74:
"pgrep -d ' ' -- '^qemu(-kvm|-system.{1,11})$"

The reason of change code is:
QEMU have contain kvm.QEMU can make use of KVM when running a target architecture that is the same as the host architecture. For instance, when running qemu-system-x86 on an x86 compatible processor, you can take advantage of the KVM acceleration - giving you benefit for your host and your guest system.


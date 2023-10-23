# 适用于amd cpu,macos ventura , opencore 配置

# 虚拟机:vmware16/17

# 物理机:技嘉 x570 aorus master
(修改自:https://github.com/luchina-gabriel/EFI-GIGABYTE-X570-AORUS-MASTER-5950X-RX-580)

已知问题:

1,不能睡眠,系统要禁用睡眠,否则可能会不能唤醒,也可能会在睡眠时就死机

2,Intel I211 网卡不能使用,原仓库中的补丁直接不能用,启用网卡就死机,
  后来换了个AppleGB的补丁,这个补丁更痛苦,看着能用,会不定时的死机,排查禁用后没再死机过

蓝牙不能用,IntelBTPatcher.kext补丁包有问题,

同时能够由该配置引导windows11

# Proxmox VE8
需要在虚拟机配置文件xxx.conf中的第一行加入

args: -device isa-applesmc,osk=”ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc” -smbios type=2 -device usb-kbd,bus=ehci.0,port=2 -global nec-usb-xhci.msi=off -global ICH9-LPC.acpi-pci-hotplug-with-bridge-support=off -cpu Haswell-noTSX,vendor=GenuineIntel,+invtsc,+hypervisor,kvm=on,vmware-cpuid-freq=on

参考自: https://techantidote.com/install-macos-ventura-on-proxmox-8-x/


不能使用的,直接不能开机
-------------------------------
ESXi
hyper-v

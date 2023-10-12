# 适用于amd cpu,macos ventura opencore 配置


确认能使用:
-------------------------------

虚拟机:vmware16/17,Proxmox VE8

物理机:技嘉 x570 aorus master (修改自:https://github.com/luchina-gabriel/EFI-GIGABYTE-X570-AORUS-MASTER-5950X-RX-580)
x570主板音频接口还是对不上,但不影响声音,麦没试出来.
蓝牙不能用,IntelBTPatcher.kext补丁包有问题,
同时能够由该配置引导windows11

不能使用的,直接不能开机
-------------------------------
ESXi
hyper-v

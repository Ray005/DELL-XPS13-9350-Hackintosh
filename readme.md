说明：OC版本0.8.6。单nvme硬盘win&mac双系统。换免驱网卡DW1560


电脑型号	戴尔 XPS 13 9350 笔记本电脑  (扫描时间：2023年03月07日)

操作系统	Windows 10 64位 ( 4.09.00.0904 )

处理器	英特尔 Core i7-6500U @ 2.50GHz 双核

主板	戴尔 020NRM ( 英特尔 PCI 标准主机 CPU 桥 - 100 Series 芯片组 Family/eSPI Controller - 9D48 )

内存	8 GB ( 1867MHz )

主硬盘	 NVMe PM951 NVMe SAMSU ( 256 GB / 固态硬盘 )

显卡	英特尔 HD Graphics 520 ( 128 MB / 戴尔 )

显示器	夏普 SHP144A ( 13.3 英寸  )

声卡	瑞昱  @ 英特尔 High Definition Audio 控制器

网卡	博通 Broadcom 802.11ac Network Adapter / 苹果(DW1560 BCM94352Z)




# 主板级的设置：

本机解锁cfg lock的地址是0x109，使用以下命令解锁：

setup_var 0x109 # 查看状态，0x01是锁定，0x00是解锁

setup_var 0x109 0x00 # 解锁

setup_var 0x109 0x01 # 重新上锁

## 进不了mac系统怎么办？

实在不行复位bios，再①解锁cfg、②调整sata模式为ahci

## 进不了win怎么办？

实在不行复位bios，启动win，按f8进安全模式，看看能不能自动修复驱动。再重启进正常模式。
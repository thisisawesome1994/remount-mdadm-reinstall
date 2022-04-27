# remount-mdadm-reinstall
Remount mdadm software raid after os reinstall...


Software RAID (mdam) in Linux
Run the following commands from the Root Terminal window. Click the system menu system_menu_button in the bottom left corner, then click Accessories and select Root Terminal.

1.Detect RAID arrays by superblocks and generate a configuration file:

mdadm --examine --scan >/etc/mdadm/mdadm.conf

 

2.Assemble arrays based on generated configuration file:

mdadm --assemble --scan

 

3.Use the command below to list the available disk partitions:

fdisk -l

 

4.Mount the RAID array:

mount /dev/md<number> /path/to/mount/point

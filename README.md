mkbootimg_tools
===============

HOW TO USE:
-----------

### Unpack boot/recovery(.img) support dtb(dt.img):
		./mkboot name.img namefolderout

	EXAMPLE
		./mkboot recoveryksuamg5.img ksuamg
		Unpack & decompress recoveryksuamg5.img to ksuamg
		  kernel         : /home/xiaolu/work/initramfs/s4/e330s/ksuamg5/zImage
		  ramdisk        : /home/xiaolu/work/initramfs/s4/e330s/ksuamg5/ramdisk.gz
		  page_size      : 2048
		  base_addr      : 0x00000000
		  kernel size    : 6911360
		  kernel_addr    : 0x00008000
		  ramdisk_size   : 2685222
		  ramdisk_addr   : 0x02000000
		  second_size    : 0
		  second_addr    : 0x00f00000
		  dtb_size       : 1427456
		  tags_addr      : 0x01e00000
		  cmdline        : console=null androidboot.hardware=qcom user_debug=31 maxcpus=2 msm_rtb.filter=0x3F
		Unpack completed.

### Repack boot/recovery(.img) support dtb(dt.img):
		./mkboot namefolderout newimgname.img

	EXAMPLE
		./mkboot ksuamg5 recovery.img
		mkbootimg from ksuamg5/img_info.
		  kernel         : /home/xiaolu/work/initramfs/s4/e330s/ksuamg5/zImage
		  ramdisk        : /home/xiaolu/work/initramfs/s4/e330s/ksuamg5/new_ramdisk.gz
		  page_size      : 
		  base_addr      : 0x00000000
		  kernel size    : 6911360
		  kernel_addr    : 0x00008000
		  ramdisk_size   : 2685222
		  ramdisk_addr   : 0x02000000
		  second_size    : 
		  second_addr    : 
		  dtb_size       : 1427456
		  dtb_img        : dt.img
		  tags_addr      : 0x01e00000
		  cmdline        : console=null androidboot.hardware=qcom user_debug=31 maxcpus=2 msm_rtb.filter=0x3F
		Kernel size: 6911360, new ramdisk size: 3416778, recovery.img: 11759616.
		recovery.img has been created.
		...


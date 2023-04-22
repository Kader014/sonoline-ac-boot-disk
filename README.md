# sonoline-ac-boot-disk
Siemens sonoline ac boot disk image

Created using dd in ubuntu

created with:
sudo dd if=/dev/sdb of=./sonoline-ac-boot-disk-image.img bs=512 iflag=fullblock conv=noerror 
(my floppy drive was /dev/sdb)

you can write the image to a new floppy disk with:

sudo dd if=./sonoline-ac-boot-disk-image.img of=/dev/sdb bs=512 iflag=fullblock conv=sync,noerror

Good luck
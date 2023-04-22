# Siemens Sonoline AC boot floppy diskette image

Copy of my original Siemens Sonoline AC floppy drive diskette using dd in ubuntu

This is an extremely rare floppy disk image to find given that Siemens discontinued the Sonoline AC back in 1991.

I created the floppy diskette image 
with:
sudo dd if=/dev/sdb of=./sonoline-ac-boot-disk-image.img bs=512 iflag=fullblock conv=noerror 

(my floppy drive was /dev/sdb) 

I used a Sandberg USB Floppy Drive to create the floppy diskette image and to create the floppy copies.

## Usage Instructions: 

You can write the image to a new floppy disk with:

sudo dd if=./sonoline-ac-boot-disk-image.img of=/dev/sdb bs=512 iflag=fullblock conv=sync,noerror

(make sure to replace /dev/sdb with whatever device your floppy drive is)

For most cases you can find your floppy drive device with using:

sudo fdisk -l |grep -v loop |grep dev

Good luck
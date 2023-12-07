				The PCI Bus and Shared Interrupts

	This is very important- please read carefully.  Before proceeding, please make
that if your BIOS setup screens have an option to set "Plug and Play OS" to yes or no,
that you set this value to 'no' (which is usually the default).  This will result in the
startup BIOS performing all the device assignments.

	The PCI bus uses shared interrupts.  This means that the a/d converter board may 
share its interrupt with another device.  This is not desireable, however.  If the a/d 
shares its interrupt it may experience too long an interrupt latency.  Also note that many 
motherboards electrically share a PCI slot's interrupt line with a motherboard device 
(such as the ethernet controller, USB controller, video, etc).

	To discover if the a/d shares its interrupt one must run the program 'pci -v' under 
6.2NC.  This will generate a lot of info about how the PCI bus devices are configured.  
Look for the line that is labelled "Interrupt line" for each device.  The a/d converter 
will be listed with Vendor ID 1093h, National Instruments.  Note what interrupt it has been 
assigned.  Then look at the other devices and note if any have the same interrupt.

	If the a/d shares its interrupt one can try a few things to remedy this.  The 
first is to boot to the setup screens for the PC.  Some setup screens have a page where PCI 
interrupts can be assigned.  One can try changing the interrupt here.  You might notice, 
however, that as you change the a/d interrupt that some other device's interrupt changes as 
well to match it.  This is because the interrupt line of the slot the a/d is in 
electrically shares its interrupt with the motherboard device.

	If you cannot assign the a/d an unshared interrupt thru the setup screens, you can 
try changing the PCI slot of the a/d.  You might find a slot that has an unshared 
interrupt.

	Finally, if none of the above work you can disable a motherboard device you are not 
using (such as USB) in the setup screens.  Then find the slot that shares its interrupt 
with the USB device and place the a/d in it.  Even though it is still sharing its interrupt 
with the USB device, it will not be a problem since the USB device is turned off.  This is 
what must be done on the Dell Optiplex 400, for example.

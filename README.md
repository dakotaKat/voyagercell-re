# voyagercell-re
Notes and discoveries on the KLAS VoyagerCell Duo and KlasOS from an outsider PoV

# "what the fuck is klasOS"
* some kind of linux
* klasOS shell is clish-powered
* libvirt, openvswitch
* main os bin runs everywhere, changes what it can do based on hardware IDs
  * vmware? "GuestOS". voyagercell? "voyagerVMm" (lol)
  * `board_<model>.py` scripts seem to have a lot of nice documentation about each piece of kit

# "what the fuck is the voyagercell"
* it's in the lab
* it's a manpack celltower in a box
  * external ports - 2x ethernet, 1x console
  * has onboard wifi, but can swap for a modem
* it's an amalgation of two products that got welded together as klas grew up
  * voyagerVMm: virtualization server. core i7-7600u, 32gb ram, 256gb samsung 850.
  * 4GAP1000: 1-5W eNodeB. Various band options. Basically a femtocell connected internally
* it runs klasOS, then klasOS in a VM with a chroot that contains a customized version of Druid Raemis
  * default license seems to be for 2x eNodeB, 50 users. nice.
  * default cli on the VM console is klas's clish, but also includes a cisco 5921 image (unlicensed)
* voyagerVMm has lots of untapped power to run local compute, PBX, etc

# ULX-X99-EFI Atermiter X99 Socket 2011-3 (2020)

EFI for this specific motherboard

#BIOS Settings : 

#Enable
	CSM 
	Above 4G decoding.
	*This must be on, if you can't find the option then add npci=0x2000 to boot-args.
	*Do not have both this option and npci on boot-args enabled at the same time.
	Hyper-Threading
	Execute Disable Bit
	EHCI/XHCI Hand-off

#Disable
	Fast Boot
	Secure Boot
	Serial/COM Port
	Parallel Port
	VT-d (can be enabled if you set DisableIoMapper to YES)
	CFG Lock (MSR 0xE2 write protection)
		*This must be off, if you can't find the option then ENABLE AppleXcpmCfgLock.
		*Your hack will not boot with CFG-Lock enabled.
		*For 10.10 and older, you'll need to ENABLE AppleCpuPmCfgLock as well.

#Compatible SMBIOS
	*iMacPro1,1
	*MacPro7,1
Use genSMBIOS
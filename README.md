# Prebuild Raspbian with Xenomai
- SD Card: at least 4GB
- Write to SD Cart with Win32DiskImager

## rPi4
### 5.15.52 64bit

#### Log in info
- **hostname**: _xeno-pi4_
- **username**: _xeno_
- **password**: _xenomai_

#### Xenomai info
- **IRQPipe**: _Cobalt v3.2.1_
- **Xenomai**: _Xenomai v3.2.1_
  
#### Modifiers
- no frequency governor
- no CPU idling
- CPU frequency fixed to 1.8Ghz -> ensure adequate cooling
- **/boot/cmdline.txt**: _wc_otg.fiq_enable=0 dwc_otg.fiq_fsm_enable=0 dwc_otg.nak_holdoff=0 isolcpus=0,1 xenomai.supported_cpus=0x3_
- /boot/config.txt: total_mem=3072, dtoverlay=pi3-disable-bt

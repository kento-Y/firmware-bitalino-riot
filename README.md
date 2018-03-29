# BITalino R-IoT firmware
firmware of the BITalino R-IoT Hardware v2.0 (USB charging, USB serial port)

v2.04
- Fixed RGB LED order (swapped green and blue)
- Cosmetics
- Fixed : access to calibration for 6s after booting, even if not wifi connected
- Fixed : LED blinking (white) during MAG calibration

v2.03
- aligned IRCAM and Bitalino R-IoT versions and code
- Sensor axis matching between LSM9DS0 and LSM9DS1 + board layout.
- Safety on calibration: active for a short time after power cycling only (JP LAMBERT).


#### quick start

* Download and install Energia version 17 from [energia.nu/download/](http://energia.nu/download/#previousreleases).
* Modify the `cc3200.ld` file and change the `HEAP_SIZE` value to `0x00008000` :
  * on Windows this file is located into `C:\Program Files(x86)\energia-0101E0017\hardware\cc3200\cores\cc3200`
  * on Mac OS, right-click on the Energia application and select "show package contents", then go to `Contents/Resources/Java/hardware/cc3200/cores/cc3200`
* Get the SLFS library from [github.com/Ircam-R-IoT/SLFS](https://github.com/Ircam-R-IoT/SLFS) and drop it into `Documents/Energia/libraries`.
* Get the BITalino Energia library from [github.com/Ircam-R-IoT/bitalino-energia-library](https://github.com/Ircam-R-IoT/bitalino-energia-library) and drop it into `Documents/Energia/libraries`.
* Open the firmware.ino file with Energia and hit the "Verify" button in the upper left corner. If it builds, you're ready to upload it to the R-IoT board.

#### going further

For more information, please visit
[bitalino.com/en/r-iot-kit](http://bitalino.com/en/r-iot-kit) or [ismm.ircam.fr/riot/](http://ismm.ircam.fr/riot/).

#### credits

This project has been developed by the ISMM team at IRCAM-Centre Pompidou within the CoSiMa project (funded by ANR), the MusicBricks project funded by the European Union's Horizon 2020 research and innovation programme, and the RAPID-MIX project (H2020-ICT-2014-1 Project ID 644862).

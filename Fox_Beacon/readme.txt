This .ZIP file contains the files needed to upgrade and configure the 
Byonics Micro-Fox FA (www.byonics.com)

MicroFoxConfig v1.6.exe - This is the config program for the v1.6 firmware.

microfox v1.64.t3f - This is the firmware file used to update the chip.  
	If the chip already contains v1.64, this file is not needed.

Firmware updates in v1.64
- Fixed firmed when tones list is empty

Firmware updates in v1.63
- Prevented empty tones list
- Fixed bug with 0 tones duration

Firmware updates in v1.62
- Fixed bug setting frequency, especially at lower voltage
- Fixed bug where LED sometimes didn't turn on
- Fixed transmission during initial LED flash

Firmware updates in v1.6
- Fixed bug with loop time > 256 seconds
- Added support for Initial Delay

Instructions for updating the Micro-Fox firmware:
 - Obtain a copy of Tera Term Pro
 - Connect the Micro-Fox the the computer serial port with a MT-AIO/MF 
	programming cable. (Female DB-9 to 3/32" stereo, 5 to shield, 
	pin 3 to ring, and pin 2 to tip)
 - Start Tera Term Pro, and under Serial Port..., select the connected 
	COM port, 19200 baud, and a transmit delay of 1 msec/char
 - In the terminal program, press and hold the 'b' key
 - Apply power to the Micro-Fox
 - The terminal should display "ø_1" or "_1". If it doesn't, reset power
	to try again, keeping the 'b' key held.
 - Release the 'b' key
 - Press (and release) the 's' key.  Nothing will be changed in the terminal.
 - Choose File, Send File..., check the binary box, and select the 
	desired .t3f file
 - During the upload, nothing should be displayed on the terminal
 - After the upload was successful, the teminal should display a '*'. If
	it does not, repeat from the press and hold 'b' step. There 
	may be a few second delay after the Send File dialog closes
	and the '*' appears.
 - Quit Tera Term Pro
 - Cycle power on the Micro-Fox
 - Run the Micro-Fox config program to set the desired options. (Do not 
	read current settings first, they may be bad)
 
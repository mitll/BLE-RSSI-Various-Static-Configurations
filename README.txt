Overview:
This dataset contains ~30 second collects in various static configurations.  Data was collected in various environments, with different phone carrying positions, and with different user rotations relative to the measurement device.  Additionally, multiple measurement devices were used.  All collects were done with 6' separation between the transmitting device and receiving device.

Environments:
- Anechoic chamber (low multipath environment)
- Screen room (high multipath environment)
- Conference room, direct line of sight between transmitting device and receiving device
- Conference room, wall separating transmitting device and receiving device
- Outdoor, asphalt paved courtyard

Transmit device locations:
- Front pants pocket (left side)
- Purse (right side)
- Back pants pocket (left side)
- Left ear

User rotations:
- 0 degrees (user front towards measurement device)
- 45 degrees
- 90 degrees (user left side towards measurement device)
- 135 degrees
- 180 degrees (user back towards measurement device)
- 225 degrees
- 270 degrees (user right side towards measurement device)
- 315 degrees

Measurement devices:
- iPhone 10 (MIT-LL Bluetooth Proximity App)
- Ubertooth One
- nRF52 eval board

For each collect, 3-4 transmitting devices were enabled at the same time.  Therefore, the data logs will contain RSSI for multiple devices.  The nRF Connect app was used on the transmitting devices to specify unique device names.  The following is the mapping of device names to device locations on body:
	Device Name		Device Location
	TestPhone1		Front pants pocket (left side)
	TestPhone2		Purse (right side)
	TestPhone3		Back pants pocket (right side)
	TestPhone4		Held to left ear
	
Note that some collects were done without TestPhone1 present.

The dataset is organized by <environment>\<measurement device>\<user rotation>.
Within each data folder are separate subfolders for each measurement device (iPhone, Ubertooth and nRF52.  Within the measurement device folders are separate data files for each user rotation.  The angle is given at the end of the filename.  For example, a file ending in "_135.txt" or "_135.pcapng" indicates that the user was at a rotation of 135 degrees.  These details should go into the data files as metadata fields.  Once metadata fields are standardized we can postprocess the files and add them.

iPhone folders contain csv log files from the Bluetooth Proximity app.  Ubertooth and nRF52 folders contain PCAP (Wireshark) files, as well as CSV files containing teh most relevant subset of the PCAP data.  These CSV files contain a header line so they are self-explanatory.

Contact:
	Mark Krangle
	The MITRE Corporation
	mkrangle@mitre.org
	781-271-7008





• Target operating system – Windows 10

• Scan our Wi-Fi network for active IoT devices

• Provide IP and MAC address about each discovered device

• Enable users to input device information and capture packets

• Save captured packets in a pcap file format

• Save pcap filename with the device info in database for 10

## IoT devices.
# Objectives

IoT Devices

• IoT Devices are everyday objects embedded with sensors, software and connectivity to exchange data over the internet.

• It has wide range.

• Each IoT device has a public IP over the internet and a respective MAC address.

Tools and Libraries Used to Scan Wi-Fi network for IoT Devices

• Python3

• PyQt5 (for GUI interface)
 

• Scapy to send ARP requests to discover IoT devices and capture packets to and from a specified device in the network.

• Requests to send API request to mavendors.com to get the vendor details of respective MAC addresses of the devices discovered.

• Sqlite3 to store filename and respective IP of device in the database.

PyQt5

   

▪ Python library to create cross-platform desktop applications with GUI.

▪ Offers wide range of widgets, layouts and tools for building sophisticated desktop apps.

# Scapy

▪ Powerful Python Library for packet manipulation and network analysis.

▪ Allow packet capturing, send and receive packets on a network.

▪ Makes network discovery easier with Python.

# Sqlite3

▪ In-built library in python to create database instances.

▪ No need to maintain a separate database server.

▪ Lightweight solution for small to medium sized applications.

# Algorithm to Scan Wi-Fi Network

• Scapy generates an ARP object having destination address as IP range of local Wi-Fi network.

• Generate Ethernet object having destination MAC address as broadcast address to send ARP request to all IP in network.

• Packet is created and send using srp function of scapy.

• Packets received are noted and device info is stored and

# displayed using PyQt5 GUI interface.

Source code for Scanning network Algorithm to Capture Packets through a Device

• Scapy uses sniff() to capture the packets through a specific device.

• First, packets are filtered based on the device IP as src or dst fields and presence of IP layer.

• Next, packets are captured based on the packet count given by the user.

• Lastly, the packets are stored in a pcap file using wrpcap() function of scapy and stored in the database using sqlite3


# Displaying Device Information

• IP Address

• MAC Address

• Vendor Details

# Displaying Stored Device

Info in Database
• IP Address
• Packet filename

# Conclusion
• In conclusion, the provided application effectively fulfills the
specified requirements for scanning a Wi-Fi network for
active IoT devices, capturing packets, and saving device
information along with the captured packets.
• the application effectively combines the functionalities of
network scanning, packet capturing, and database
management into a coordinated solution. It provides users
with a convenient way to discover and monitor IoT devices on
their Wi-Fi network while also facilitating packet capture for
further analysis

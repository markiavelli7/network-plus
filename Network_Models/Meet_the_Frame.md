# Meet the Frame

Frames are a maximum of 1500 bytes and they have a discrete beginning and end.

Frames are created and destroyed inside the Network Interface Card (NIC).

# The MAC Address

A unique 48 bit identifier for a NIC

### Finding MAC addresses on Windows

ipconfig /all

### Finding MAC addresses on a Mac:

networksetup -listallhardwareports

The first 6 digits of the 12 digit MAC address are issued to the OEM from the internet folks. The last 6 are assigned by the OEM.

Destination MAC Address -> Source MAC Address -> Data -> Cyclic Redundancy Check (CRC) aka Frame Check Sequence

# Broadcast vs Unicast

Broadcast to all of the computers on the broadcast domain - MAC address FF-FF-FF-FF-FF-FF

# Introduction to IP Addressing

Unlike MAC addresses, IP addresses are not fixed to the NIC. We can apply an IP address to a network card.

To talk to another computer that is not on the same LAN, we use a router and add IP addresses to the frame. What we end up with is an IP packet. IP packets sit within the frame. The IP packet will include the data and a destination and source IP address. When a computer is sending data, it looks at the destination IP, if it sees that the computer is not part of its network, using its Default Gateway it will send the frame to the router and use the routers MAC address as the destination MAC. The **Default Gateway** is the connection to the router itself. Once it gets to the router, the router will strip away the frame, leaving the IP packet. It will then create a new frame with the destination MAC set to the destination computer.

# Packets and Ports

Port numbers are unique to individual applications that are used all over the internet.

TCP (Transmission Control Protocol) is a connection-orientated conversation between two computers to make sure that the data gets to us whole, complete, and in order. Two big pieces of TCP are a **sequencing number** and an **acknowledgement number**. The sequencing number lets us reasssemble the 25000 pieces of data that are sent. The acknowldgement number is the thumbs up to the other computer saying, "got the data!"

UDP is connectionless.

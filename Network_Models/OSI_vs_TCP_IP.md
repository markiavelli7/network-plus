# OSI Seven Layer Model

1. Physical - What type of cables do I use?
2. Data Link - Anything that works with a MAC address works at the Data Link layer. We start talking about switches and the NICs themselves.
3. Network - Logical addresses (IP addresses). We are talking about things like routers.
4. Transport - Assembly and disassembly area for data. We are moving large chunks of data in small pieces.
5. Session - The actual connection between two systems. Is it a TCP connection between two clients? Are we sending an email? Are we sharing a folder on a network? The session layer defines what's taking place in terms of how that connectivity really works.
6. Presentation - Used to convert data into a format that our applications can read.
7. Application - The smarts in the applications that make them network aware. Microsof Office, for example is network aware.

# TCP/IP

1. Network Interface - All the physical cabling, MAC addresses, NICs, and all kinds of harware, with the exception of routers.
2. Internet - IP addresses, routers, etc
3. Transport - Dis-assembly and re-assembly of data, as well as whatever it takes to connect to the other system to make sure that the data gets there.
4. Application - Takes into account the OSI layers of Session, Presentation, and Application.

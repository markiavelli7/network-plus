# Walking Through the OSI and TCP/IP Models

## Scenario: Client Sending a Request to a Server for a Webpage, Server Responds Back

## Step 1

### OSI Layers 1,2 (Physical & Data Link)

### TCP/IP Layer 1 (Network Interface (Link))

I'm a network card just sitting here waiting for some data.. Oh wait, here comes an ethernet frame. With this ethernet frame, my job as the network card is to take a look at the incoming MAC address and verify that it is for me. In this case it is, I can take the data in the frame and look at the Frame Check Sequence and verify that the data is in good shape. Assuming that it is, I can strip off the MAC addresses from the frame. Just in case I need to send something back later to the sender, I'm going to store the MAC info that I'm stripping off to the side so that I can reference it later. With the MAC addresses removed, we now have an IP packet and my job as a Network Card is pretty much finished.

## Step 2

### OSI Layer 3 (Network)

### TCP/IP Layer 2 (Internet)

My job is really simple, I deal with IP addresses. I check to see that the destination IP address is for me. Assuming that it is, I will store the senders IP address. I will then strip off the IP address information, leaving a TCP segment.

## Step 3

### OSI Layer 4 (Transport)

### TCP/IP Layer 3 (Transport)

I am the dis-assembler and re-assembler of data. My job is to take data that is going out, and if it is big, chop it into little bite-sized chunks. Equally, if a bunch of data is coming in, my job is to re-assemble all of this data. I use sequencing numbers to disassemble and reassemble. I remove the sequencing number from the packet, leaving the data and port numbers.

## Step 4

### OSI Layers 5,6,7 (Session, Presentation, Application)

### TCP/IP Layer 4 (Application)

The session layer is designed to connect a server to a client on a remote system. Presentation layer doesn't really apply anymore, it used to deal with weird file extensions that had to be converted in order for applications to use them. The application layer does not talk about the actual applications themselves. The application layer refers to the smarts that allow the application to interface with a network. The application layer's job is to take a look at the port numbers and send the data to the correct application. We then strip off the port numbers, taking note of the senders port number for future re-use.

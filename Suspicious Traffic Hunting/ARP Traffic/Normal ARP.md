# Normal ARP

2 packets: 1 ARP Request and 1 ARP Reply
![Alt text](image-2.png)

To see the MAC Address for both the source and destination: 
```
View > Name Resolution > Resolve Physical Addresses
```
![Alt text](image-3.png)

Here we see an ARP Request packet. 
We know it's an ARP Request by the Opcode, request(1) in the highlighted line:
![Alt text](image-4.png)

The device at 10.54.15.100 needs the MAC address for 10.54.15.68 to begin to establish communication with it. 

In this packet we have the reply to the previous packet:
![Alt text](image-5.png)

This packet is the ARP Reply packet. 
We can tell by the Opcode, reply (2). 
We see that the Sender MAC address has been populated with the MAC address of the device at 10.54.15.68.
This MAC address will be added to the ARP table of 10.54.15.100. 

The following packets reflect an ARP Request within a network using a broadcast address as the destination:
![Alt text](image-6.png)
![Alt text](image-7.png)


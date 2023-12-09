# Live Network Captures

Few things to consider during a LIVE network capture: 
1. capture and test to confirm that you're indeed capturing the traffic you intend to capture. 
2. confirm that you have enough computing power to handle all the packets you'll be capturing, especially in a heavy traffic network segment.
3. make sure you have enough disk space on your device.
4. remember with switches, traffic destined for a particular host is point-to-point. To capture data, you will need to be connected to a mirrored port

### Port Mirroring
Port mirroring is the process of replicating traffic destined for one or more ports to this specific port, mirrored port, which will be used for network analysis or packet analysis. 

If the port mirroring option is not available, use the following options to sniff network traffic on the switch:
- tapping the network cable
- MAC flooding (red team tactic)
- ARP spoofing (red team tactic)

### Network Tap
Network taps entail physically tapping the wire or network cable, whether it's a copper cable or fiber. 

Hardware is availble that will allow us to tap the wire and intercept the traffic as it traverses the cable. 
- ex: vampire tap

Inline Network Tap: tap is inserted 'inline' between two physical network devices, such as a firewall and a switch. 
- replicates copies of packets on a seperate port, or ports, as it passes along the packets to its destination. 

### MAC Floods
MAC flooding is considered active sniffing and a tactic used by Red Teams
- requires authorization to use

MAC Flooding is meant to stress the switch and fill its CAM table. 
When the space in the CAM table is filled with fake MAC addresses, the switch can no longer learn new MAC addresses. 
The only way to keep the network alive is to forward the frames meant to be delivered to the unknown MAC address on all ports of the switch, thus making it fail open and act like a hub. 

### ARP Poisoning
ARP Poisoning or ARP spoofing is another active technique, but can be considered stealthy. 
It doesn't bring down the functionalities of the switch, as MAC Flooding does, but instead, it exploits the concept of traffic redirection. 
- considered a Red Team technique

By exploiting the network via ARP poisoning, we can redirect the traffic of the host(s) we want to monitor to our machine; this will allow us to monitor the traffic intended for the host(s) of interest. 

Used to perform Man in the Middle attacks. 
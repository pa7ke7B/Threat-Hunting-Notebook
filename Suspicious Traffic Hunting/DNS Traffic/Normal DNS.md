# Normal DNS

4 packets - 2 packets for DNS Queries and 2 for DNS Responses:
![Alt text](image-2.png)

There are 2 different transaction IDs for the packets: 0xde40 & 0xa620

Below is a UDP packet and it's using an expected port, 53:
![Alt text](image-3.png)

This is the DNS Response to the DNS Query in packet 16:
![Alt text](image-4.png)

Packet capture displaying various DNS queries, but you can see the pattern of the DNS Query followed by the DNS Response:
![Alt text](image-5.png)


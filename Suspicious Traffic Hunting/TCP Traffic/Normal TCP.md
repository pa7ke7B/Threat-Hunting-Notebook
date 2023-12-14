# Normal TCP

Example of a normal TCP 3-way handshake:
![Alt text](image-3.png)

![Alt text](image-4.png)
![Alt text](image-5.png)

All SEQ and ACK numbers always start at 0 for the first packet seen in conversation because that's how Wireshark and TShark does it. 

You can change this by going into Wireshark and:
```
Edit > Preferences > Protocols > TCP > Relative sequence numbers (uncheck box)
```

In order to se the original sequence and acknowledgement numbers:
![Alt text](image-6.png)


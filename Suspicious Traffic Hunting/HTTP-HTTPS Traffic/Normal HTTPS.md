# Normal HTTPS

![Alt text](image-8.png)

- SSL portion of the packet is not empty
- Content type = handshake
- handshake protocol: Client Hello
- Version: TLS 1.2
- Cipher Suites (11 suites)
- Compression Method (1 method)

Server's response, server hello packet:
![Alt text](image-9.png)

![Alt text](image-10.png)

![Alt text](image-11.png)

The last packet and the handshake between the server and client is now complete: 

![Alt text](image-12.png)

Decrypting SSL encrypted application data: 

![Alt text](image-13.png)

```
Edit > preferences > protocols > SSL > Edit (next to RSA keys list)
```

The traffic was decrypted. The decrypted traffic is highlighted in the screenshot in green:

![Alt text](image-14.png)


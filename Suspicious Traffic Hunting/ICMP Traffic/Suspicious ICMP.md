# Suspicious ICMP

The data field of an ICMP packet can be used as a covert channel or even an exfiltration channel.

Large ICMP packets should be a red flag. 

Unusual types/codes within the ICMP packets followed by a request, such as Timestamp request. 
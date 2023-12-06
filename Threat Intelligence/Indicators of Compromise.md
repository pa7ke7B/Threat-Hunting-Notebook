# Indicators of Compromise

IOCs are pieces of forensic data, such as data found in system log entries or files, that identify potentially malicious activity on a system or network. 

Aid in detecting: 
- data breaches
- malware infections
- other threat activity

When we obtain IOCs from ISACs, threat sharing platforms, etc., we need to get the IOC in the format that our tools will understand. 
For instance, OTX allows us to download IOCs in the OpenIOC format. 

Typically, IOCs are malware signatures, MD5 hashes of malware files, IP addresses, and URLs or domain names of botnet command and control servers. 

### IOC Editor
IOCs are XML documents that help security professionals capture diverse information about threats, including attributes of malicious fiels, characteristics of registry changes, and artifacts in memory. 

### Redline
Redline can perform an IOC analysis. 
Supplied with a set of IOCs, the Redline Portable Agent is automatically configured to gether the data required to perform the IOC analysis, and an IOC hit result review. 

### YARA
YARA is a tool aimed at helping malware researchers to identify and classify malware samples. 
You can create descriptions of malware families based on textual or binary patterns. 
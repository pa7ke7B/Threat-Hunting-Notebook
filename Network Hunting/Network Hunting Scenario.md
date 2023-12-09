# Network Hunting Scenario

Scenario a threat hunter would encounter that would involve network hunting:

1. The network team would alert the hunter of unusual traffic on the network or in a specific subnet. 
- Note: the org doesn't have to go into full-blown IR mode at this point. 
2. The network team or threat hunter would begin capturing packets. 
3. The hunter would analyse the packet captures to confirm if there is an active threat in the network. 

### How would the Network Team know if someting suspicious is happening? 
They will know through an alert from an appliance, such as an IDS/IPS.
Other methods of the Network Team can use to see that something odd is happening on the network is through statistical flow analysis (statistical modeling) and full packet capturing/analysis.

Statistical flow analysis: 
- provide visibility as to what is happening on the network. 
- graphs and advanced statistical analysis will aid the network team visually to see what is happening in the network historically or in real-time. 

Network baselines:
- allow the network team to see if anything is suspicious within the network, such as large unusual spikes, which can represent an exfiltration. 


# Networking Devices

### Routers
Routers are devices connected to different networks at the same time. 

They can forward IP datagrams from one network to another. 
The forwarding policy is based on routing protocols. 

Routing protocols are used to determine the best path to reach a network. 
A router inspects the destination address of every incoming packet and then forwards it through one of its interfaces. 

To choose the right forwarding interface, a router performs a lookup in the routing table. 
The routing table maps IP addresses to a specific interface. 
The table will also contain an entry with a default address (0.0.0.0); this is used when the router receives a packet whose destination is unknown. 

During path discovery, routing protocols also assign a metric to each link; this ensures that if two paths have the same number of hops, the fastest route is selected. 
The metric is chosen according to the channel's estimated bandwidth and congestion. 

### Switches
Switches work with MAC addresses. 

Switches have multiple interfaces, so they need to keep a forwarding table that binds one or more MAC addresses to an interface. 

The forwarding table is called the Content Addressable Memory (CAM) table. 
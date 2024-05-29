
# Types of Delays 

## Store and forward / transmission delay 

* Once a packet arrives at a router, the entire packet needs to be processed by the router before the packet can continue on to its next destination. 
* We measure this amount of time by taking the number of bits in the packet (L) and dividing it by the transmission rate (R). 
	* This makes sense, it is a simple calculation that says that t = d/s.

## Processing delay 

* Time it takes for a router to access a packet's header to see where it is due to go. 

## Queuing delay

* Time it takes for a queue to clear at a router. 
	* This can get especially bad if the arrival rate exceeds the rate at which arriving packets are processed. If this is the case, then the network must stop routing packets to this router until the queue is cleared. 

## Propogation delay

* Time it takes for a packet to go from one router to another. 
* Mainly based on distance since speeds are conceptually close to that of the speed of light. 

# Principles of Packet Switching 

## VCN 

* Setup process is completed where a predetermined path is outlined for the packet, passing through numerous switches along the way. 
	* Each switch has an outbound link and knows the VC ID of this packet. 
* Each packet switch indexes the VC table to find the outbound link. 
* After a packet arrives at its destination, the network needs to clean up the state information about the packet...
	* Information such as the outbound link of each switch.
	* The VC ID associated with every packet. 
	* This is a slow process and that's why VCN is not usually preffered. 

## Datagram networks

* I still don't understand this that well. 
* Packets do not have predetermined paths, outbound links are decided on the spot and dynamically. 
* Each switch only cares about the destination address of the packet, and aims to get the packet closer to that address, layer by layer. 

# ISP Tier System 

Internet Service Proviers (ISPs), function at different levels and magnitudes. Some are reserved for local connections, some regional, others national, and few international. These ISPs are typically able to communicate with one another through connection points. I won't dwell on the details since some of them are too peculiar for this stage of the reading and will be repeated in the coming chapters. 


# Communication models for Applications 

## Client - Server 

- Most common and basic sort of architecture. 
- Consists of an always-on server that can facilitate requests of a not always-on client. 
- Common use: the Web. 

## P2P 

- Features communication between two "peers" and does not include a central server. 
- Generally thought of as unreliable as the lack of centralized control makes things hard to predict. 
- Used in instances of file sharing (Wink, Wink - piracy). 

## Hybrid 

- Contains a centralized server for some tasks but can support P2P models for others. 
- Used in certain instant messaging applications. 

# Definitions 

## Process 

- Any instance of a program executing. 
- This is a very important and commonly used word in comp sci literature, I better get used to it. 

## Socket 

- A sort of "portal" or "door" between the application layer and the transport layer. 
- Once a message is sent out and it leaves the application layer, it goes through the socket before going through the transport layer protocol that facilities the sending out of that message. 
- Application layer developers don't get much of a say in how the transport layer is developed. 
	- Can sometimes choose between TCP/UDP based on the needs of the application. 
	- Can also outline some limitations regarding buffers or segment sizes. 

## IP Address 

- Uniquely identifies the interface that is connecting a host to the Internet. 
- This definition does not make sense to me, but it will be expanded upon in later chapters. 

## Port Number 

- Helps direct data to the correct application on the receiving host as often times a host may have multiple applications and processes running at the same time. 
- This is also recognized by the sender. 
- Various application layer protocols have their own port numbers. 

# Choosing Transport Layer Protocols 

- Factors such as reliability, timing, and bandwidth are considered. 
- Choice is between TCP or UDP. 
- Will be expanded upon in the next reading. 


# Transfer Layer Protocols 

## TCP 

- Connection - oriented and requires a handshake procedure to establish a connection. 
- Guarantees arrival of data in its proper order. No guarantees are given on how long the data will take to arrive. 
- Better used for secure services such as banks, emails, etc.

## UDP

- Connectionless service, unreliable. 
- Can guarantee minimum transmission rates (some applications require a minimum bandwidth). 
- Used for real - time applications such as telephony or multiplayer games. 

**TCP/IP refers to a class of transfer layer protocols among which both TCP and UDP are included.**

**Browsers are responsible for implementing the client side of the HTTP(S) protocol.**

# Types of Connections 

## Non - persistent connections 

- A single connections established for each request. 
- Connection is closed after the request is serviced. 

## Persistent connections 

- Connection is not immediately closed after a request has been serviced. 
- Can feature pipelining in order to avoid idling (multiple requests can be serviced at the same time either in series or parallel). I have no idea what this means:). 

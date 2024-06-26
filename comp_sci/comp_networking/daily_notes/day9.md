
# P2P File Sharing 

## Description 

- Accounted for over 22% of global internet traffic, despite the rise in streaming services. 

## Approaches/Architecture 

### Centralized Directory (Example: Napster)

- Uses a centralized server to keep track of all the files that a client has. 
- Maps a client to an IP address (this mapping changes each time the client enters/exits the application). 
- Each change in the user's files (insertion or deletion) must be coordinated with the central directory as it will be updated.
- To make sure that disconnected users are not taking up bandwidth, the directory will send out messages to clients. If no response is received, users are assumed to be disconnected and are removed from the database. 
- This approach is slow and too centralized. 

### Query Flooding (Example: Gnutella)

- Overlay networks are established. These networks consist of people with TCP connections between them, modeled as graphs with nodes(clients) and edges(connections between clients).
- Each query is first sent into the neighbours of the client, then to the neighbours of the neighbours of the client, etc. This is done until a match is found. 
- When a match is found, a hitback message is sent over existing TCP connections(now traversing the same path backwards) and a direct TCP connection is established between the client and the uploader. 
- This method is known to flood the network with too many inquiries, which is why a limit can be set. Each time a neighbour forwards the query to other neighbours this count is decremented until the limit is reached. This might mean that although a file is available in the overall network, it was not found within the constraints of the peer limit that was set. 

### Hybrid (Example: KaZaA)

- Composed of many hubs, each hub has a group leader and peers assigned to that group leader. 
- Group leaders are decided based on availability and quantity of files, and quality of Internet connection. 
- Group leaders have a database of the files that are owned by group members. 
- Each time a member queries for a file, it first checks with the leader to check in the local network (a small directory server like used in Napster). If the file is not found locally, the group leader queries other group leaders (like in Gnutella), until the match is found.
- Once again, when a match is found, a direct TCP connection is established between the client and the uploader. 

## Features

- It is common to prioritize uploaders with more bandwidth, so as to make the file transfer faster. 
- People with more uploads rather than downloads are prioritized, incentivizes people to upload and to increase number of files that are available.
- These protocols are just that, protocols, they can be run on any client and modified within certain constraints. 
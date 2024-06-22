
# DNS 

- Simply said, DNS maps mnemonic hostnames to IP addresses. 
- DNS is distributed among many servers, and runs in a hierarchical fashion. 
- DNS runs over UDP since the sizes of queries are usually small enough to not need a connection-based protocol such as TCP. 

## IP addresses 

- In IPv4, IP addresses are four bytes and are addresses in the Internet. 
- DNS helps with mapping these addresses to mnemonic hostnames. (Hostnames are better for people, addresses are better for routers.)
- Read from left to right, an IP address contains more specific information about the said address. 

## Hierarchy 

- Each query will start with a local DNS resolver that will first query a root DNS server. 
- The root DNS server then will query one of these ervers. 
	- TLD (Top Level Domain), includes major servers like com, edu, gov, fr, uk, etc. 
	- Authoritative servers contain public records of mappings from hostname to IP addresses. 

## Query 

- A query from a host goes to a local DNS server.
	- In recursive queries, the local DNS resolver is completely responsible for obtaining the mapping by continuously querying other services until the match is obtained. This type query is between the client and the local DNS resolver. 
	- In iterative queries, the local DNS resolver queries other DNS servers. These servers either provide the resolver with the answer or a referall down the hierarchy to other servers that might know the answer. This type of query is between the local DNS server and other DNS servers. 

## Caching 

Caching is a very important part of DNS architecture and can mean that a single query skips an entire step in the hierarchy of DNS queries or simply finds the answer outright. 

## DNS rotation 

Popular sites that amass significant traffic have more than one mapping from their hostname to an IP address. During each query, the server will provide a different address from the set of addresses in order to distribute the load equally among this set of addresses. 


**Important Note: DNS mappings are not permanent. A host can easily add or exclude an IP address from the set of mappings.** 
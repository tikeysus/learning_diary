
# Cookies 

- Used to keep track of a user's activity.
- Can be implemented over stateless protocols such as HTTP. 
- Cookie header number can be associated with a user each time a request is sent out, keeps track of activity this way. 
- Advertising companies can keep track of a user's activity across multiple websites! Each ad or banner that is shown is obtained through an HTTP request, and each request includes a cookie number header line. Crazy stuff. 

# Electronic Mail 

- The most crucial application on the Internet. 
- Uses SMTP protocol. (Not going to read up on the specifics.)
- Includes a user agent to help send, receive, read messages.

# Web Caches 

- Inexpensive server that has its own disk storage.
- Instead of requesting an object from the origin server each time, a user can obtain the object straight through the cache. 
- "Hit rate" refers to how often the cache has the requested object in its storage. 
- Every object in cache has a "Last Modified" header, objects are confirmed to be up to the date with the origin server before they are sent out to the user. 
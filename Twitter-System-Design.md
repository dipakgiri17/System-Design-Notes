# Twitter

Read/Write from users must be very fast. To achive this there are two separate services for reading and writing.


## Message Queue for write operations

To handle write, there are a Message Queue and a Database updater between the Write Service and the Database.
This deals with the conditions when the database is offline or fails, it waits for the database to come online and retries.

## Caching for read operations

To handle read, it uses a caching layer. There must be more read operations than writes (such as feeds, timeline, viewing tweets and proofiles).
when a read request comes it checks the cache, if the data is not available on cache it queries the database and updates the cache.

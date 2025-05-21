# Twitter

Read/Write from users must be very fast. To achive this there are two separate services for reading and writing.

To handle write, there are a Message Queue and a Database updater between the Write Service and the Database.
This deals with the conditions when the database is offline or fails, it waits for the database to come online and retries.


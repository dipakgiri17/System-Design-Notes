# WhatsApp System Design

## Message Queue for Write Operations

WS uses a Message Service(write service) responsible for handling all the incoming messages from user-to-user or group chats, validates it and sends to message queue.

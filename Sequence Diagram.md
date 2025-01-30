```mermaid

sequenceDiagram
    participant Client
    participant Server
    participant ServerProcess
    
    Client->>Server: DYNA_CONN_REQ
    Server->>ServerProcess: Create Process
    ServerProcess->>Client: CONN_ACK
    Client->>ServerProcess: DATA_QUERY
    ServerProcess->>Client: DATA_RESULT
    Client->>ServerProcess: DISC_REQ
    ServerProcess->>Client: DISC_ACK
```
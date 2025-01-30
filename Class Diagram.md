```mermaid
classDiagram
    class Server {
        -cModuleType* srvProcType
        -int counter
        +initialize()
        +handleMessage(cMessage*)
    }
    class ServerProcess {
        +handleMessage(cMessage*)
        +initialize()
    }
    class Client {
        +handleMessage(cMessage*)
        +initialize()
    }
    class DynaPacket {
        +getKind()
        +getServerProcId()
        +setServerProcId()
    }
    
    Server --> ServerProcess : creates
    Server --> DynaPacket : handles
    Client --> DynaPacket : sends
    ServerProcess --> DynaPacket : processes
```mermaid
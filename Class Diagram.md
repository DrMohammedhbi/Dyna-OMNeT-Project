```mermaid
classDiagram
    class Server {
        -cModuleType* srvProcType
        -int counter
        +initialize()
        +handleMessage(cMessage*)
    }
    class ServerProcess {
        +ServerProcess()
        +activity()
    }
    class Client {
        +Client()
        +activity()
    }
    class DynaPacket {
     + getSrcAddress() 
    +setSrcAddress(int srcAddress)
    + getDestAddress() 
    +setDestAddress(int destAddress)
    + getServerProcId() 
    +setServerProcId(int serverProcId)
    }
    
    Server --> ServerProcess : creates
    Server --> DynaPacket : handles
    Client --> DynaPacket : sends
    ServerProcess --> DynaPacket : processes
```mermaid

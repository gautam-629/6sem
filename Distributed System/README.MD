# communication in distributed system
Communication in a distributed system refers to the exchange of information and messages between the different components or nodes of the system. In a distributed system, components are located on multiple computers or servers, connected through a network, and work together to achieve a common goal. 

>**Here are some key aspects of communication in a distributed system**

1. **Message Passing**
The most common method of communication in distributed systems is through message passing. Nodes send messages to each other to request information, notify about events, or initiate actions. 
 
2. **Remote Procedure Calls (RPC)**
RPC is a technique that allows a distributed system to invoke procedures or functions on remote nodes as if they were local. It abstracts the details of network communication, making it easier to develop distributed applications. 

![Basic](https://res.cloudinary.com/dbvr3bxyv/image/upload/v1687757847/distributed%20system/1_qv64ja.png)

>**RPC operation**

![operation](https://res.cloudinary.com/dbvr3bxyv/image/upload/v1687757845/distributed%20system/2_zaza3w.png)

>**Working of RPC:**
1. Client
2. Client Stub
3. RPC Rutime
4. Server Stub
5. Server

![working](https://res.cloudinary.com/dbvr3bxyv/image/upload/v1687758216/distributed%20system/3_p6ko9l.png)

>**Point to know**

1.**Client**
The client component initiates the RPC by invoking a method on a remote object. It acts as the source of the RPC request.

2.**Client Stub**

The client-side stub is responsible for packaging the method invocation into a message and transmitting it to the server. It abstracts the network details and provides a local representation of the remote object.

3.**RPC Rutime**

The transport layer is responsible for transmitting the RPC request from the client to the server over the network.

4.**Server Stub**

The first task performed by server stub is that it unpacks(unmarshalled) the call request message which is received from the local RPC Runtime and makes a regular call to invoke the required procedure in the server.

5.**Server**

After receiving a call request from the client machine, the server stub passes it to the server. The execution of the required procedure is made by the server and finally, it returns the result to the server stub so that it can be passed to the client machine using the local RPC Runtime.

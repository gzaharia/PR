## Network Programming Laboratory Work Nr.6


### Prerequisites:
  - C#/Java
  - UDP - Protocol.

### Objectives:
  - Understand the UDP protocol and the basic methods.
  - Initiliazion the properties for UDP Protocol.
  - Performing the chat based on UDP protocol connection.
  - Basic concpets of UDP-protocol.
  
 ### Task:
  Performing the Client-Server application based on UDP-protocol connection.
 
 
 ### Implementation of task: 
 In this laboratory work I had to perform an Client-Server app, which will comunicate through UDP-Protocol. So, first what I have done is opening some links and read about possible connections between Client and Server with UDP-Protocol. Reading some information I have found that the **IP + Port Number = Socket**. So, let's define the term of socket that is used for performing the connections between Client and Server. The **Socket**  is the endpoint two-way communication between two machines running on the network knowing the host port, this things for TCP means that it can identify the application and the data that should be send.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Socket.PNG)
 
 Let's analyze from my task , why I use socket and for what? The socket ensure in my case the communication between Client and Server. To Client side I should specify the IP and the Port, but for Server side I should specify only the Port. The socket in other words , open a door , open a way of communication.
 
 **Why the UDP-Protocol is proposed?**

The UDP-Protocol has common things with TCP, there are both for Data Transfer, but there are the some differences between them : 
  
  - TCP will guarantee that data are delivered, but UDP not.
  - TCP is connection oriented, this means that it will keep all track about connection (open, maintain and close), UDP will not do as the TCP, just will send the request, this is useful in case of **Broadcast** and **Multicast**.
  
 In Java language for achieving the UDP-Protocol we have the **DatagramSocket** this is type of network socket which provides connection-less point for sending and receiving packets. Every packet sent from a datagram socket is individually routed and delivered.
 Next, the **InetAddress** object in Java represents an Internet Protocol(IP) address. The representation in bytes is for **ip address**.
 Sending the data : I have the **Scanner** object, which allow control on the keyboard and the next thing is the sending the ip and the port to the server with DatagramPacket, this means that the connection is build.
 
 The logic and the implementation of code are the same for the Server side.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Client.PNG)
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Server.PNG)
 
 
 ### Output:
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Send_Client.PNG)
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Receive_Server.PNG)
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab6/Screens/Receive_Client.PNG)
 
 
 ### Conclusion:
 
 In this laboratory work I obtained skills operating with Sockets and UDP-Protocol. Sockets in programming have some advantages : flexible, low internet traffic and not need some checks about delivering the data. Socket based communications allows only to send packets of raw data between applications. Both the client-side and server-side have to provide mechanisms to make the data useful in any way. 
 
 According to the documentation and the experience of working with protocols, the UDP send not the messages not the packets as the TCP. The UDP is useful in cases where the latency is critical, this means that the communication between machines should not have some delays.

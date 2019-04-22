## Network Programming Laboratory Work Nr.5


### Prerequisites:
  - C#/Java
  - Sockets API.

### Objectives:
  - Understand the Data Transfer Protocols.
  - Initiliazation the communication between Client-Server.
  - Performing the chat between clients.
  - Basic concpets of TCP-Protocol.
  
 ### Task:
  Performing the Client-Server application based on Sockets.
 
 
 ### Implementation of task:
 In this laboratory work I should perform the communication between 2 sides based on Sockets. A socket
 is a  endpoint of two-way communication between machines. There are several types of Sockets:
  - Stream Sockets - uses TCP.
  - Datagram Sockets - uses UDP.
  - Raw Sockets
  - Sequenced Packet Socket
  
  So, in this laboratory work I had perform the connection over TCP(Transmission Control Protocol), this
  protocol will guarantee that data are received by the receiver and will send the confirmation message
  baack to the sender.
  
  Let's analyze this steps acording to my task. For achieving the the tasks I have 2 main classes:
  
   - Client
   - Server
   
   In the Client Class I have implemented the Client-side in this chat and performed the connection to the 
   Server. For connection from the Client-side we need to know : ip and port.
   I had initialized some objects for working with transfer of messages or data. Next, I have the method
   **ListenThread()** which the purpose is for starting the new thread for each connected client to the 
   Server. 
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/Variables.PNG)
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/second.PNG)
   
   The **userAdd(), userRemove()** methods are for working with users and display information about
   connected users and the name of each of them. The method **sendDisconnect()** is for UI part , this is the logic for
   the Disconnect button and the **Disconnect()** will close the opened thread and one more approach is
   that the name of the user will not be changed, **isConnected(false), tf_username.setEditable(true)**.
  
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/third.PNG)
   
   **IncomingReader() implements Runnable** this method will work with all incoming messages from the clients
   and server-side and all the messages will appear on the textView on the UI part.
   
   Next in my Client class are the elements based on the UI part and the connection between UI and the 
   implementation.
   
   
   On the Server-side I had the implementation for the Server behavior, the server is performed for
   follow the communication between clients. 
   
   Let's analyze the Server implementation. I have **server class** which starts the implementation with
   the  **ClientHandler()** that implements Runnable , this means that this method will have something
   related with threads. So, this method will care of about users that will connect to the Server and will
   create for each of them the new thread separately , the ClientHandler per user.
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/Client.PNG)
   
   Next I have the method **run()** which comes automatically from the Runnable interface, the purpose of this 
   method is for show some information about data, connections to server and the status of the user.
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/run.PNG)
   
   The **ServerStart()** method is also important in this laboratory, because this will manage the connection 
   to server and deliver the threads for each client that will connect to the server. The connection is opened
   so, the Client comes to the ServerStart and this will create new thread for this client.
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/ServerStart.PNG)
   
   Next are methods for UI part.
   
   ### Output
   
   For starting the application you should first run the server_frame and then the client_frame, if you will
   start first the client the server will not start. Also, for perform some clients you should press
   again to running the client_frame class.
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/output1.PNG)
   
   ![](https://github.com/gzaharia/PR/blob/master/PR-lab5/Screens/online_users_button.PNG) 
   
   
   ### Conclusion:
   
   In this laboratory work I have obtained skills working with connection between 2 sides and some basic notions
   in Swing(UI part). Also, after implementation all of actions I can say that the server has the relation
   many-to-many with clients, because it has a lot of connections, but the client has the relation
   one-to-one with server. 
   
   The one feature that I have observed on the TCP is scalability, this allows to add some networks, without
   disrupt the existed ones.It assigns an IP address to each computer on the network, thus making each device to be identifiable over the network. 
   It assigns each site a domain name. It provides name and address resolution services.

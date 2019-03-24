## Network Programming Laboratory Work Nr.4


### Prerequisites:
  - C#/Java
  - SMTP/POP3 - Protocol.

### Objectives:
  - Understand the SMTP protocol and the basic methods.
  - Initiliazion the properties for SMTP Protocol.
  - Using the real mail account/fake server for testing the mail sending functionalities.
  - Basic concpets of SMTP/POP3 - Protocol.
  
 ### Task:
 Performing the Mail Client to sending and retrieving the messaages from mail account. The Client should use the SMTP/POP3 protocols.
 
 
 ### Implementation of task: 
 In this laboratory work I had to create Mail Client , who will send and get the messaages from the e-mail. According to the given task I should use the SMTP and POP3 protocols. So, let's inform about this protocols. 
 
 **SMTP** - mail servers and other mail transfer agents use SMTP to send and receive mail messages on TCP port 25. User-level client mail applications typically use SMTP only for sending messages to a mail server for relaying. For this, mail clients typically submit their outgoing emails to a mail server on port 587 or 465. 
 
 **POP3** - for retrieving messages the IMAP and POP3 are standards, but frequently servers use their own system on retrieving.Although most POP3 clients have an option to leave mail on server after download, they generally connect, retrieve all messages, store them on the client system, and delete them from the server. By contrast, the Internet Message Access Protocol (IMAP) normally leaves all messages on the server. 
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/SMTP.PNG)
 
 So, for perfoming the sending of the messages we have to open an session and get instance of the proprieties(configurations) for sending.
 Next, I created the variable **transport** of type SMTPTransport for connection to the gmail post and sending the credentials and message with all parts (header, message body, attachments) to the receiver. 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/main.PNG)
 
 In the function **MessageInitiliaze**  I performed the message of MIME(Multi-Purpose Internet Mail Extensions) type and initiliazed the the message parts, where I have added the one .txt file **PR-File.txt** and an image **utm.png**. 
 The one question can appeaer : **Where the all of parts are stored and are send?** . So, the answer is clear , we have the **Multipart** initialiazed in the beginning , which is an container that holds multiple body parts.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/initialize.PNG)
 
 The next function in process of sending the mail is : **Attachments()** , where this function initiliaze a abstract part which contatins the content.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/attachments.PNG)
 
 The **BodyParts()** is created for adding the content to the message.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/body.PNG)
 
 The last function is for properties, which are for configuration : **host**  , **auth**...
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/properties.PNG)
 
 For retrieving the messages I have another package, which has the RetrieveEmails Class, which retrieve the messages from Inbox Folder from the post. Here, I have the **Store** provider, which connect to the store through POP3. Next, I got the Inbox folder and read the inbox mails. The **Message** array is created for storing the inbox mails and parse them in the correspoding structure. Below, I have 2 functions which are for parsing the information from the mail. 
 
 1. **getTextFromMessage** - getContent() from the Message part. 
 
 2. **getTextFromMimeMultipart** - parsing the Html and getting the text from the body.
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/retrieve.PNG) 
 
 
 ### Output:
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/send.PNG) 
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/file.PNG)
 
 ![](https://github.com/gzaharia/PR/blob/master/PR-lab4/Screens/retrieve_result.PNG) 
 
### Conclusion:
In this laboratory work I have obtained skills of performing the Mail Client using the mail sending protocols : SMTP and POP3. So, after this tasks I understood the process of sending the mails. 

During the tasks I have obeserved some facts about SMTP, this protocol is insecure, can be easily hacked, but from another part you can using SMTP : system allows you to synchronize a Smarthost server. For example, if you have 200 computers in the office that use a CRM and you want to synchronize with the SMTP server; you don’t have to configure the SMTP on each machine. You only would have to synchronize a Smarthost server that would manage all email accounts.

The POP3 is great to use for : since all mails resides on your PC, you can read your mail without being logged onto the Internet.
You may create new messages to send to others without being logged onto the Internet. But , there are and disadvantades : all messages are stored on your hard drive eating up what is sometimes very valuable space. All messages are stored on your system, and privacy disappears when someone sits down at your machine. Even if your email reader is password protected, it is often possible for someone who knows what they are doing to read your email by using another application to open your mail folders.

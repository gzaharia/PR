## Network Programming Laboratory Work Nr.3


### Prerequisites:
  - C#/Java
  - HTTP - Protocol

### Objectives:
  - Understand the HTTP protocol and the basic methods.
  - GET, POST, DELETE, PUT.
  - Semnification of status codes.
  - Types of HTTP conections.
  - Basic concepts of HTTP method : headers, servers , clients, methods.
  
 ### Tasks: 
 Implement an HTTP client that should use the HTTP methods for performing the requests. 
 
 ### Implementation of task: 
 
 Before starting performing the laboratory work I have read about HTTP Client and what this means.
 !()[]
 
 So, according to the language that I have chose at the beginning I have found information about performing the HTTP request in the Java language.
 In Java there are several ways to perform the HTTP requests,so I have chose to use the **HttpUrlConnection**   which open or in other words
 do the conenction between Browser and Server. The UrlConnection class has a lot of methods and functions for performing the functioality of the
 connections and the requests. So, the first methods that I have performed was **GET** , I stipulated this in the **con.setRequestMethod("GET")**.
 Also, I set the property for the User-Agent, which I had mentioned all of possible Browsers that cand work with and the type of encoding **gzip**. 
 
 !()[]  
 
 Next , I catched the status code, this help to see if the request have passed or not , according to the code. 
 
 - 200 : success.
 - 405 : the method does not exist.
 - 404 : server error.  
 
 So, if the response code is 200 then I have used the Reader , the Input/OutputStream for reading and writing the **response body**. Here,
 I want mention about difference between Reader and InputStream , the main difference is that the Reader is character based , but the InputStream 
 is byte based. For reading and displaying the response I have used an **while(true)** , which seams to be an infinite loop, but in this case
 checked if here exist characters , and if exist display them in the same form(i.e parsing the response). 
 
 !()[] 
 
 The next method that I have implemented is **POST** which used the approx. the same code, but something slightly different. Here appears
 the notion about **setDoOutput()** , which should be **true** for the POST method, this means that it should send the response body to the server
 for performing some changes. If this has the **false** option this will do the GET method. 
 I have some commented code , this is for adding some fields in the body.
 
 !()[] 
 
 
 In the **DELETE** method actions is the same as in the POST method. 
 
 The last method I have performed for getting an image from the server. Here I have used another tool from Java , which is **Image** and 
 **JFrame**.
 
 
 
 
 
 

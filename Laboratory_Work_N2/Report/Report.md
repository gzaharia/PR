## Network Programming Laboratory Work Nr.2


### Prerequisites:
  - C#/Java
  - Multi-threading

### Objectives:
  - Understand the notion about threads.
  - Concurency and taks running in parallel.
  - Multi-threading methods of processing the tasks : signals, semaphore, thread-pools.
  - Create the process of running the threads according to one oriented graph.
  
 ### Tasks:
 1. According to the graph perform the communication and execution between threads.
 
 ![](https://github.com/gzaharia/PR/blob/master/Laboratory_Work_N2/Screens/Variant.PNG)
 
 
 
 
  ### Implementation of task:
  In this laboratory work I have started with reading about threads what is the purpose of this notion in programming. So, I find out that this is the smallest sequence of programmed instructions that can be managed independently by a scheduler.
  I have read about how initiliaze a thred in Java language , this looks like : **public class Threads exteds Thread** and the second way is to implement Runnable. I have performed with extend Thread.
  So, I performed ArrayList of threads , boolean variable and a variable for thread name. The next I have created the get and set methods for threadWaiting(list of threads). 
  Next, each thread has the **monitor lock** property or can implement the synchronization method, which means that each thread has a key which allow it to execute the task. The function runThreads() exactly to this thing, stop the execution of
  the thread if this should wait the previous thread execution. For example, then the 3 thread will end the execution it will notifyAll() about this and the next thread which depend on this thread , will start the execution. 
  
  In the Main class, I have created according to my graph the threads. The second step, I called the setThreadWaiting() method which will set the dependency. Next, I used start() predefined method to start the threads and join() to notify about
  his execution the threads.
  
  ![](https://github.com/gzaharia/PR/blob/master/Laboratory_Work_N2/Screens/thread.PNG)
  
  ![](https://github.com/gzaharia/PR/blob/master/Laboratory_Work_N2/Screens/main.PNG)
  
  ### Output
  The result can changes every time , because theare are more than one possible way to execute all tasks from threads.
  
  ![](https://github.com/gzaharia/PR/blob/master/Laboratory_Work_N2/Screens/output.PNG)
  
  
  ### Conclusion
  In this laboratory work I have learned how work with threads and how to execute their tasks. Also, I hadn't use many libraries , but I have implemented the whole procees of working the threads. Moreover, I learned about concurency and the parallelism can make the work process of CPU easier, this means that we only 6 Cores but the CPU can execute 1000 of tasks. Managing the threads execution with Monitor lock, synchronized method.
  

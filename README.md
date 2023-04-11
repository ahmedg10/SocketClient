## What was Returned when pinging various servers: 

1. server djxmmx.net / port 17
    1.  Apr 10, 2023 3:51:33 PM TCPClient main
        INFO: Connected to server djxmmx.net on port 17
        Apr 10, 2023 3:51:33 PM TCPClient main
        INFO: Connected to server djxmmx.net on port 17
        "Imagine all the people, sharing all the world.
        You may say I'm a dreamer, but I'm not the only one.
        I hope some day you'll join us, and world will live as one..."
        this was a greate quote!
2. server time.nist.gov / port 13 (Date-and-Time service)
    1. 60044 23-04-10 22:48:21 50 0 0 216.6 UTC(NIST) * 

3. server tcpbin.com / port 4242 (Echo Service)
    1. With thread: Apr 10, 2023 4:11:46 PM TCPClient main
                    INFO: Connected to server tcpbin.com on port 4242
                    Apr 10, 2023 4:11:46 PM TCPClient main
                    INFO: Connected to server tcpbin.com on port 4242
                    hey
                    hey
                    yo
                    yo

Other Insights: I found that the two first servers would not echo back, or return anything when I put something in it. In fact, when I put two things back to back into network pipeline it would break the pipe. 
## Important Insights:

### What is a Socket?
This is fundemental concept in Network Programming allows programs to send and recieve data to and from programs over network connection. 

### What can this be transalte to 
This basic skill can help you learn the basics in building more complex network apps, such as chat applicatons, and data driven services. Additionally, this task helps to familiarize you with the process of connecting to various types of network services and working with their APIs.

### How can you provide diagnostic logging that describes that console what is happening: 
You have to incorperate some sort of leveling. Think of this, as a way to flag if you want all the information or just in the important information. You have to provide some sort of conditional to allow the logger to understand when to do this. 

### What is the Purpose of a Thread:
Allow different parts of a program to run concurrently or at the same time. It is best practice to have a handler that implements a Runnable. This Runnable object allows you to exectute the thread you are looking to run. By using this handler, we can alos manage errors that occur on that specifc thread as well.

### Gaps in my Knowledge: 
1. Synthax of Java and using socket, input and output stream classes.  I had to do a lot of googling and looking up. 
2. Usuage of out.flush -> This is part of the outputstream class so when you write to the server it doesn't send until the buffer (temp holding area for info) is full. However, the flush will pretty much force send things in the buffer to the server after the line is ended. 
3. Logger synthax: What I found is that the logger gives us information about the network connection. However, there is a thing called levels in which depending on a input value you put in it identifies if you want more information or not. For instance, if you but -v in console that it tells to send the logger.info rather than the logger.warning (which is just the important stuff). Later, in the code we put in manual informatio of what happens in the info and it was returned to us. 
4. I sadly was not able to figure out how to get a response back after the command line input is send to the server. I don't get the echo back from the server. I only get it from the echo server. 
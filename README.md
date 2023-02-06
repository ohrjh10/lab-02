# Lab 2
[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo and clone it to your machine to get started!

## Team Members
- individual work: Richard Oh

## Lab Question Answers
Question 1: How did the reliability of UDP change when you added 50% loss to your local environment? Why did this occur?
Answer for Question 1: After 50% loss was added, I typed numbers 1 to 10 to see if all packages were correctly delivered.
From observation, I was able to notice that some numbers were not delivered properly, especially when the numbers were sent in faster speed.
As a result, the reliability of the UDP has decreased because the packets that were sent are more likely to be lost.
This trend happened because UDP protocol does not have any requirements or checking whether the data was delivered without generating an error.

Question 2: How did the reliability of TCP change? Why did this occur?
Answer for Question 2: In the beginning, the TCP works fine just like before the 50% loss was added. However, the TCP starts to become 
slower and later does not respond. Because the TCP tries to check all the data and make sure they 
don't get lost, the waiting time gets longer when 50% loss is added.

Question 3: How did the speed of the TCP response change? Why might this happen?
Answer for Question 3: For the TCP, the speed of receiving data became much slower compared to before. 
TCP protocol are safer in a sense that data is much less likely to be lost during the delivery process. 
However, since data are checked so that they are not lost during the process, it takes up more time for the process to finish.

QUESTIONS FROM tcp_server.c
1. What is argc and *argv[]?
Answer: argc is the number of arguments on the command line pointed by argv, and *argv[] is the arrays of the argument vector.

2. What is a UNIX file descriptor and file descriptor table?
Answer: The file descriptor is an identifier for a file or other input/output between the user and the kernel space.
The file descriptor table is the collection of unsigned integers used in the process to identify an open file.

3. What is a struct? What's the structure of sockaddr_in?
Answer: Struct is used to group variable that are related(depending on the type). 
The structure of specifies a transport address and port for the AF_INET address group.

4. What are the input parameters and return value of socket()
Answer: The socket() argument takes inputs such as domain, type of socket, protocol, and the address information to designate the address type.
The return value is the file descriptor which is typically a non-negative integer.

5. What are the input parameters of bind() and listen()?
Answer:

6. Why use while(1)? Based on the code below, what problems might occur if there are multiple simultaneous connections to handle?
Answer:

7. Research how the command fork() works. How can it be applied here to better handle multiple connections?
Answer:

...

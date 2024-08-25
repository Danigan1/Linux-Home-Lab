# Networking


## What is data networking?

Data networking refers to the practice of connecting various devices and systems so that they can share and exchange data

This includes everything from computers and servers to smartphones and IoT devices. 

The primary goals of data networking are to facilitate communication between devices, ensure the efficient transfer of data, and maintain the security and integrity of the information being exchanged.

<br>


![image](https://github.com/user-attachments/assets/6aab0000-8865-4600-bcfd-038d9d762900)



<br>


# The OSI MODEL

a way of showcasing what happens at the granular level when computers/ devices are communicating with each other

it consists of 7 layers.

There are many protocols at work in networking and each one is categorized at a certain layer.

![image](https://github.com/user-attachments/assets/c3f2d11d-bf8f-4d1e-919d-2b91439bee60)




### application Layer

- The Application Layer is what the user sees and interacts with such as a webpage

- The Application layer contains data that users can understand like text, images, or files. 

- There are certain protcols that are at work in this layer such as  HTTP (Hypertext Transfer Protcol)

- This is a protocol that is used by the web browser (chrome) to access a web page which is really just a document that is written in a programming language called HTML (Hyper Text Mark Up Language)

- your browser uses HTTP to make requests to the web server to accesss that webpage.

This is one of the many protcols that the application layer uses.

HTTP: For browsing the web.
<br>
SMTP: For sending emails.
<br>
FTP: For transferring files.

### presentation Layer

-  Deals with changing data from one format to another. Application level data gets converted to computer understandable language. Binary. It stays like this as it goes further down the OSI model
-  This is known as encoding

- Human-Readable Data: This refers to data that is easily understood by people, such as text, numbers, or images. For example, "Hello, World!" is human-readable text.

- Binary Data: Computers operate using binary code (combinations of 0s and 1s). To work with human-readable data, it needs to be converted into this binary format.

### Encoding Process:

Text Encoding: For text data, encoding schemes like ASCII or UTF-8 convert characters into binary representations. 

For instance, the letter "A" might be represented as the binary number 01000001 in ASCII.


File Formats: Different types of files (images, videos, documents) use specific encoding schemes to represent data in a way that can be stored and interpreted by different software. For example, JPEG files use a particular encoding format for image data, while MP4 files use another for video and audio.



### session Layer

- not used as much in today

### Transport Layer

- In order for us to have a conversation between our computer and another. There needs to be a way to build a session in between the two devices before communication can start.
- Similar to how when you call someone on the phone. the phone on the receipt's end rings and they pick up and say hello which establishes the session.
- The TCP protocol (transmission control protocol) sets up a session between two devices so that data can be sent
-  The transport layer also facilitates service to service delivery. Which means that a computer is able to reach out to a service that lies on another computer
- Source and destination port numbers are added to data as a header
-  UDP is TCP's counterpart is also a transmission protcol which does not establish a session before communication



### Routing Layer

- facilities end to end delivery

- from one ip address to another ip address at a differernt location

- source and destination ip address are added to data as a header


### Data Link Layer

- faciliates hop to hop delivery

- from one Network interface Card to another Network interface Card on the path to the final destination

- Source and Destination Mac address are added to data as a header

- switches are devices that work with MAC addresses

### Physical Layer

- bits being transported across the wire 1s and 0s

- computers at the most basic level communicate in these 1s and 0s. They dont speak in english

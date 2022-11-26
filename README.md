# Video_Stream_App_SystemDesign

## Introduction
These High Level Architecture is being used to render the videos or to upload the videos in the online streaming applicaitons like netflix or youtube .

## Basic Terminology 

### Client: 
The client is the person who would like to upload a video in the streaming application.

### Upload Services :
The main agenda of the upload services is to send the uploaded video into the distributed storage and the metadata to the database so that it can be extracted easily .Moreover, After completion of this process it will send the video to the distributed queue .

### DataBase :
The database is used to store the meta data of the video like author name, video_id in distributed storage,description etc which can be Relational or NoSQL databases.

### Distributed Storage :
The purpose of distributed storage is to store the video which is uploaded . Some of the examples are Amazon S3 or Microsoft Azure Blob Storage .

### Distributed Queue :

The purpose of this is to keep the data in a sequential order for further procedures down the line .

### Video Splitter :

The video splitter is used to break the data into multiple chunks so that it can be send for further validation and also to load the data chunk by chunk when user wants to view after the upload .

### Encoder Service :
This process is done along with content verification parallelly. The purpose of the encoder service is to render the video into different file formats and different qualities as per the modification of the encoder .

### Content Verification :

The need of content verification is to check the video that it does not contain any abusive languages or public provoking bad habits etc which again based on the modification of the service.

### Video Explorer Service :
The usage of it is to segregate the videos based on the tags mentioned bu the client and send them to the Elastic search so that when the user tries to search for any video then it takes the key words and displays the content based on it .

### Video Distributor Service :

It has an important role to play which helps to reduce of traffic and time consumption of the data load . As the distributed storage is only one and located in a prime location which makes in delay of data access so we use the video distributor service which acts as a  alternate distributed storage and is located in multiple different locations for easy access of the data as it already stores some of it based on the demand of requests present around the location.

### Internet Service Protocol(ISP) :

The ISP takes the requests from the users and maps the data to the required application based on the url and retrieves the data back after getting the information as per the request from the database . 

### cache:
The cache is same like the video distributor service which helps in storing the data based on the high requests of the users in that particular location.

### Load Balancer :
A load balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. The load balancers are used to increase capacity and reliability of applications.


## Steps :
1. Downlaod the file in the required formats and extract it in the desktop.
2. Use draw.io for opening the file or for any further modifications which are to be added based on your knowledge.



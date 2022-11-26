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

It has an important role to play which helps to reduce of traffic and time consumption of the data load 

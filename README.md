# Encryption Decryption of messages based on facial recognition
Venkat Sai Akshith V,Anshasi said 

# Overview
Our aim is to encrypt/ decrypt some type of data such as an image/written message using AES encryption/decryption algorithm, the decryption and encryption is triggered by the facial recognition algorithm.

# Background

Data existing on the cloud are massive and certain data are sensitive by nature and could present serious implication on an individual if it gets accessed by the wrong person. We wanted to implement this project because it adds to the data access security and allows authentication to the person who is trying to access sensitive data.   
Implementation strategy


# Implementation

It creates I/O Driver objects using OpenCV2 Library to interface a webcam and uses the PYNQ library . After instantiating each driver, the program will import the facial recognition library and all the images and names for each identified individual. Once completed, PYNQ will input every other frame, process the image, and detect any faces in the frame. In shunt, the program will look to see if the detected face matches any of the facial encodings from the identified individuals. If the face matches, the system will print their name under their face or print "UNKNOWN" if the face is not recognized.

AES encryption process consists of several rounds a typical round of AES encryption. Each round comprises of four sub-processes. 
Byte Substitution (SubBytes)
The 16 input bytes are substituted by looking up a fixed table (S-box) given in design. The result is in a matrix of four rows and four columns.
Shiftrows

Each of the four rows of the matrix is shifted to the left. Any entries that ‘fall off’ are re-inserted on the right side of row. Shift is carried out as follows −

•	First row is not shifted.

•	Second row is shifted one (byte) position to the left.

•	Third row is shifted two positions to the left.

•	Fourth row is shifted three positions to the left.

•	The result is a new matrix consisting of the same 16 bytes but shifted with respect to each other.

MixColumns

Each column of four bytes is now transformed using a special mathematical function. This function takes as input the four bytes of one column and outputs four completely new bytes, which replace the original column. The result is another new matrix consisting of 16 new bytes. it should be noted that this step is not performed in the last round.
Addroundkey

The 16 bytes of the matrix are now considered as 128 bits and are XORed to the 128 bits of the round key. If this is the last round then the output is the ciphertext. Otherwise, the resulting 128 bits are interpreted as 16 bytes and we begin another similar round.
Decryption Process

The process of decryption of an AES ciphertext is similar to the encryption process in the reverse order. Each round consists of the four processes conducted in the reverse order −
•	Add round key

•	Mix columns

•	Shift rows

•	Byte substitution



# Tasks
1.The first is a webcam that can be interfaced by OpenCV and imports facial recognition libraries.- Akshith (2 hrs)

2.In this we make sure that pynq will take input of every other frame and process the image and detects the faces in the frame.- Akshith/said (2hrs)

3.now we have to see detected faces match any of the facial encoding and see that if it is matched it shows detected if not it tells unknown. - Akshith/said (2 hr)

4.Creating Jupiter notebook for implementing a CPU AES encryption algorithm
(optional)-Said 3 hours

5.Creating Jupiter notebook for testing FPGA AES encryption overlay by
encrypting/decrypting a plaintext - Said 3 hours.

6.Creating Jupiter notebook for executing timing analysis between CPU and FPGA
encryption overlay (optional) -Said 3 hours.

7.Creating HLS code for encryption and decryption using Vitis security libraries - Said 3
hours.

8.Creating Vivado project to create block design for the encryption/decryption overlay -
Said 3 hours.

9.Integration between Face recognition/AES encryption/decryption overlay in Vivado
block design - Akshith/Said 3 hours.

10.Testing the integrated design in Jupiter Akshith/Said -3 hours.


# Stretch goals:
1. Encryption/decryption of the recognized face and storing it in a database
 
2. Implementing recognition algorithms for iris/ finger print
 
3. Implementing other types of recognition patterns such as a wave or special move to
decrypt a message.

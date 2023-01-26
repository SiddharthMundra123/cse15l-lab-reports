# Lap Report 1

In this file, you will learn how to install VScode, get your CSE 15L account details as well as connect to a local computer. 

## Step #1: Install VScode
The first step is to install Visual Studio Code on your PC. Go to this [link](https://code.visualstudio.com/download) and just select your OS and its version and the application automatically starts downloading.

![VScode tutorial](https://user-images.githubusercontent.com/116845419/212206740-73c63b0f-d69c-4df8-9b42-0369de90765c.png)

 

## Step #2: Download GIT
GIT is a a free-to-use open source version control system. It is very beneficial for source code management. To install it, click on this [link](https://gitforwindows.org/) and follow the installation procedures. 

![GIT tutorial](https://user-images.githubusercontent.com/116845419/212206847-723c7e73-e3d5-436c-99f0-0c32acfe4cdc.png)

## Step #3: Logging into your CSE 15L account
Once VScode and GIT is set up, you need your CSE 15L account credentials in order to login to the remote server. For that, click this [link](https://sdacs.ucsd.edu/~icc/index.php) and enter your UCSD account details. 

![password reset tutorial](https://user-images.githubusercontent.com/116845419/212208184-52535399-9d3f-480e-85c4-3048248901bd.png)

Upon recieving the details, reset your password using the specifications they have listed. AFter you have reset your password, wait for a few minutes for it to start working. ALso, note down the custom ID which is displayed in a grey box after you enter your UCSD credentials.


## Step #4: Using the terminal in VScode
Open the newly installed Visual Studio code application on your computer. Upon opening the application, you should be able to see a window similar to this one.

![vsciode tutorial](https://user-images.githubusercontent.com/116845419/212236950-ac57405e-fab2-4409-be42-dfdbf0b7e4b4.jpg)


## Step #5: Remotely connecting to the remote server

To connect to the server, you have to first open the terminal in VScode. After doing that, type in the following commmand : $ ssh cs15lwi23zz@ieng6.ucsd.edu
However, replace the zz with the specific charecters on your custom ID which you had noted down before. After entering the command, you will be prompted to enter a (yes/no) answer. Enter yes, and then it will ask you to enter a password as shown in the picture below:


![image](https://user-images.githubusercontent.com/116845419/212237985-2eecf5fb-4486-4e12-877c-36847574688d.png)



Enter the UCSD password you had just created in step #2, and then you will be connected to the UCSD Basement computer! Any commands you run now will also run on that computer! 

## Step #6: Trying out some commands
We will now try out some commands in order to test the computer's terminal. Below are some commands you can try!
* _cd_ : This command is used to change the current working directory
* _ls -lat_ : This commmand is used to display all the files in the user's profile

![ls -lat](https://user-images.githubusercontent.com/116845419/214956303-f9e4874f-c0f2-4ce3-9416-d90695c62ad3.png)

* _ls -a_ : This command is used to list all files including hidden files as well.

![ls -a](https://user-images.githubusercontent.com/116845419/214956270-b5e64ede-9b93-4382-bfb9-9937e573dadb.png)

* _mkdir_ : This stands for make directory. This command is used for creating new directories.
* _cat /home/linux/ieng6/cs15lwi23/public/hello.txt_ : cat is short for concatenate. This command displays the contents of a file

 ![cat](https://user-images.githubusercontent.com/116845419/214956321-847ab68d-170e-4f7e-8c34-b7431ff0696d.png)
 
* _cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/_ : cp stands for copy. It is used to copy the contents of a file

---
To log out of the remote server, you can either run the command "exit" or just press CTRL + D. You can also open multiple terminals in VScode! This is the end of the turotial, thank you so much for your time!


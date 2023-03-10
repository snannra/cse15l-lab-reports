# Week 1 Lab Report
## Signing into your CSE15L Account

Head to this [link](https://sdacs.ucsd.edu/~icc/index.php). You should login using your username for your triton link account, and your student ID number on this page.

<img width="667" alt="Screen Shot 2023-01-11 at 12 18 32 PM" src="https://user-images.githubusercontent.com/49798755/211909206-ca5c1dbd-14ff-4e30-9f60-245cf6f8ed16.png">

Once you've signed in, you'll land on a page that looks like this.

<img width="779" alt="Screen Shot 2023-01-11 at 12 24 15 PM" src="https://user-images.githubusercontent.com/49798755/211911454-c1813565-0045-4b8b-88f9-6b8a31e07b33.png">

Go ahead and click on the button where the arrow is pointing to. Then proceed to change your password, and make sure to uncheck the two boxes at the bottom of the page so the rest of your passwords do not get changed. Your account is now ready to be used.

## Downloading Visual Studio Code

Go to this [link](https://code.visualstudio.com/) and follow the instruction to download it onto your computer. 

![Screen Shot 2023-01-14 at 6 32 20 PM](https://user-images.githubusercontent.com/49798755/212519955-e880dc56-c497-4801-9278-4b135ed33b7c.png)

Once the download has completed, open the download on the computer and allocate the proper information in the correct folders of your choosing.

## Remotely Connecting

Once you've downloaded visual studio code, go ahead and open up a project with any name of your choosing. You'll then want to go ahead and create a new terminal. In terminal go ahead and type the comand ssh cs15lwi23xx@ieng6.ucsd.edu with the xx being replaced with the letters specfic to your username, which can be found in this [link](https://sdacs.ucsd.edu/~icc/index.php) to your account. You'll then be propmted for your new password. 

![Screen Shot 2023-01-14 at 6 40 33 PM](https://user-images.githubusercontent.com/49798755/212520139-5afab548-a2d1-4b3a-8a77-bb0ec8973c25.png)

Once you've logged in successfully, your terminal should look like this. (This may take some time the first time that you login.)

![image](https://user-images.githubusercontent.com/49798755/212520162-b5aa0a2a-b2c4-430e-b1a5-c2b4667cf8fc.png)

## Trying Some Commands

Now we'll try running some commands. Here are a list of a few commands that you can run.

![Screen Shot 2023-01-14 at 6 44 12 PM](https://user-images.githubusercontent.com/49798755/212520233-0bfe0d50-2807-4ee1-993a-8796bd202f8f.png)

When I run some of these commands, these are the outputs that I get.

![image](https://user-images.githubusercontent.com/49798755/215360382-32959b91-81ba-41e4-b62b-2c7ccdb9445b.png)

As we can see, some of these produce an output while some do not. Certain basic commands such as **ls -lat** work because they do not require a certain file structure. This function only lists the files on the computer. However, commands that are more specifc do not work. The command **ls /home/linux/ieng6/cs15lwi23/cs15lwi23abc** did not work because this file directory does not yet exist on my remote computer. This activity has taught me the importance of file structure and organization when writing intense programs.

You can try this sequence of commands that would create a directory, create a new file, write to that file, and finally print the contents of that file. 

1. mkdir test
2. cd test
3. touch file1
4. echo hello >> file1
5. cat file1

Congratulations, you've properly set up and tested your remote computer for CSE 15L.

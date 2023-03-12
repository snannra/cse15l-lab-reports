# Lab Report 4
## Steps starting at step 4
4.For this step I typed in ```ssh cs15lwi23xxx@ieng6.ucsd.edu``` (xxx is the letters specific to my account). I did not need to type in a password due to the setup that I did during lab.

![image](https://user-images.githubusercontent.com/49798755/221383543-af9b27d6-7372-48cf-9003-4e969b3d856e.png) 

5.I then went to https://github.com/username/lab7 which is where the cloned repository was. After clicking the <> Code button in the top right, I copied the SSH link. I then typed ```git clone git@github.com:snannra/lab7.git``` into the terminal.
  
![image](https://user-images.githubusercontent.com/49798755/221383632-61bf810c-01a2-40d4-ba05-7657d57414cf.png)

6.To run the tests I went to [this](https://ucsd-cse15l-w23.github.io/week/week3/) link to find the correct commands to run to test the files. I scrolled to the image that said MAC USERS and copied the first line of text, ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```, and pasted it into the terminal and hit enter. I then copied the second line and replaced ```ArrayTests``` with ```ListExamplesTests``` and typed it into the terminal and hit enter.

![image](https://user-images.githubusercontent.com/49798755/221447916-859fb7e2-4423-4b21-8283-92dfef6dc44f.png)

7.I typed ```nano ListExamples.java``` which opened up the nano environment. From there I hit ```<down>``` approximately 42 times and ```<right>``` 12 times. I then deleted the 1 and replaced it with a 2. I pressed Ctrl-O and enter to save the file and Ctrl-X to exit.
  
![image](https://user-images.githubusercontent.com/49798755/221384845-9c74df32-3f31-477f-b488-a37b104d26ee.png)
  
8.To run the tests again I pressed 
```<up><up><up><enter>, <up><up><up><enter>```

![image](https://user-images.githubusercontent.com/49798755/221384987-e489f0db-0ef3-4947-8029-3330e0c6022d.png)
  
9.To commit and push the changes to my github account I typed ```github add ListExamples.java``` and hit enter then typed ```git commit -m "updated"``` to commit the changes to the repository.

![image](https://user-images.githubusercontent.com/49798755/221385064-5713faa6-eedb-4492-99c0-84d66bd9dc1e.png)

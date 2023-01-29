# Lab Report 2
## Part 1: String Server
Here is the code that I wrote for the String Server project.

![image](https://user-images.githubusercontent.com/49798755/215362122-4a1ff5f5-7958-4cb2-9dd6-71ae32bda930.png)

In my code, I created an ArrayList of all the words that would be added and needed to be printed on the screen. To print them out, I ran a for loop to go through the ArrayList and added all the words plus the new line character to a string which was eventually printed out.

Here is an example of the code working:

![image](https://user-images.githubusercontent.com/49798755/215362275-8dd77a05-8124-456d-8f78-6cc022abbd38.png)

In my code, the first thing that is called is the handleRequest method, which also calls .getPath(), .equals(), .getQuery(), .split() and .size(). The arguments that the handleRequest method takes in is the url. There are relevant values for these methods, .getPath(), .equals() and .size(). The .getPath() method is important because it uses .equals() to make sure that they are typing in "/add-message" and if they're not, then a 404 error is returned. Addtionally the .size() method is important for the for loop so that it knows how many times to repeat based on the values that are added to the ArrayList. These values change based on the entries and the number of entries.

Here is another example of the code working again to demostrate that all words are printed:

![image](https://user-images.githubusercontent.com/49798755/215362304-896c0f25-de18-42aa-bc9c-a6be845e999b.png)


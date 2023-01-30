# Lab Report 2
## Part 1: String Server
Here is the code that I wrote for the String Server project.

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {

    ArrayList<String> allWords = new ArrayList<>();

    public String handleRequest(URI url) {

        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            allWords.add(parameters[1]);
            String output = "";
            for (int i = 0; i < allWords.size(); i++) {

                output += allWords.get(i) + "\n";

            }
            return output;
        }

        return "404 Not Found!";

    }

}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

In my code, I created an ArrayList of all the words that would be added and needed to be printed on the screen. To print them out, I ran a for loop to go through the ArrayList and added all the words plus the new line character to a string which was eventually printed out.

Here is an example of the code working:

![image](https://user-images.githubusercontent.com/49798755/215362275-8dd77a05-8124-456d-8f78-6cc022abbd38.png)

In my code, the first thing that is called is the handleRequest method, which also calls .getPath(), .equals(), .getQuery(), .split() and .size(). The arguments that the handleRequest method takes in is the url. There are relevant values for these methods, .getPath(), .equals() and .size(). The .getPath() method is important because it uses .equals() to make sure that they are typing in "/add-message" and if they're not, then a 404 error is returned. Addtionally the .size() method is important for the for loop so that it knows how many times to repeat based on the values that are added to the ArrayList. These values change based on the entries and the number of entries.

Here is another example of the code working again to demostrate that all words are printed:

![image](https://user-images.githubusercontent.com/49798755/215362304-896c0f25-de18-42aa-bc9c-a6be845e999b.png)

In this section, the handleRequest method is still called, which still calls .getPath(), .equals(), .getQuery(), .split() and .size(), however the way the code executes is slightly different. The relevant values for this method are still .getPath(), .equals() and .size(). The .getPath() and .equals() methods run the same however size is now 2 instead of 1, so the for loop runs twice and two items are now added to the output variable. Thus the output variable has changed compared to the previous example, however the .getPath() and .equals() methods didn't change.

## Part 2: Bug Analysis

The bug that I decided to work on from lab 3 is fixing the reversed method.

```
// Failure Inducing Input
@Test
  public void testReverseNewArray() {
    int[] input = {1, 2, 3, 4};
    int[] expected = {4, 3, 2, 1};
    ArrayExamples newObj = new ArrayExamples();
    int[] realOutput = newObj.reversed(input);
    assertArrayEquals(expected, realOutput);
  }
  
  @Test
  public void testReverseNewArray() {
    int[] input = {1, 3, 5};
    int[] expected = {5, 3, 1};
    ArrayExamples newObj = new ArrayExamples();
    int[] realOutput = newObj.reversed(input);
    assertArrayEquals(expected, realOutput);
  }
```
**Symptom**
When the arrays are compared, the first value of expected is 4, while the real output first value is 0.
![image](https://user-images.githubusercontent.com/49798755/215366233-0e9bcc34-6a16-40b8-b28a-ee1f7a21f838.png)
When the arrays are compared, the first value of expected is 5, while the real output first value is 0.
![image](https://user-images.githubusercontent.com/49798755/215366305-3c6832f5-12e3-437a-a8f6-970e8d4d4709.png)

```
// Input that doesn't include a failure
@Test
  public void testReverseNewArray() {
    int[] input = {0, 0};
    int[] expected = {0, 0};
    ArrayExamples newObj = new ArrayExamples();
    int[] realOutput = newObj.reversed(input);
    assertArrayEquals(expected, realOutput);
  }
  
  @Test
  public void testReverseNewArray() {
    int[] input = {0, 0, 0};
    int[] expected = {0, 0, 0};
    ArrayExamples newObj = new ArrayExamples();
    int[] realOutput = newObj.reversed(input);
    assertArrayEquals(expected, realOutput);
  }
```
**Symptom**
When the arrays are compared, all the values are the same because they are all 0 for both test cases, so there is no output code since the tests pass.

```
// Before Code
// Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

```
// After Code
// Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
The original program was setting the values that newArray contained to the indexes of arr, and was returning array at the end. Since newArray is a newly created array with only a size, all of the indexes were set to 0, so all the values in arr were being set to 0. So by changing the code so that the indexes of newArray were set to the values of arr, newArray ended up with the correct values, and the correct array was returned.

## Part 3: Reflection

One extremely important thing that I learned in week 2 and 3 is the importance of being able to test our own code properly. In our first CSE 12 assignment our test cases were given to us, but after week 2 and 3 in CSE 15L I see the value in being able to create our own tests and how that helps us understand the limitations and capabilites of our own code better. In addition, I believe that becoming more fluent with creating Junit tests can help me with my own projects and my career in the future.

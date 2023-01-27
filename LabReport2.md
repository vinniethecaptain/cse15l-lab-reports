# Part 1 #

### StringServer.java ###
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String myString = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "Type a message by adding /add-message?s=text in the link!";
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                myString = myString.concat(parameters[1] + "\n");
                return myString;
            }
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
#### Image 1 ####
![](https://media.discordapp.net/attachments/766148831594545153/1068370221536133141/image.png)

In this image, handleRequest() is called, but since there is no query, the query is returned as null and no text is returned and displayed on the page. This method takes in a URI and processes it to figure out what should be displayed on the webpage. I instantiated an empty String object called myString and it concatenates any valid query to form text for the webpage to display. The query is processed at "s" and everything after the "=" to be stored in a String array. The text the user inputs is then concatenated to the myString.

#### Image 2 ####
![](https://media.discordapp.net/attachments/766148831594545153/1068368166817890356/image.png)

In this image, handleRequest() is called, there is a query and the processed query is returned as text to be displayed on the page. Initially, the first sentence is concatenated to myString with a new line marker. I then changed the query to the second sentence which is then concatenated myString on a new line. 

# Part 2 #

##### Failure-inducing input in JUnit test #####
```
@Test 
public void testReverseInPlace() {
    int[] input = {1, 2, 3};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{3, 2, 1} , input);
}
```

##### Non-failure-inducing input in JUnit test #####
```
@Test 
public void testReverseInPlace() {
    int[] input = {0};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{0}, input1);
}
```

##### Test failure #####
![](https://media.discordapp.net/attachments/766148831594545153/1068375808768479232/image.png?width=1440&height=390)

##### The bug with before and after fixes #####
###### Before ######
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```
###### After ######
```
static void reverseInPlace(int[] arr) {
    int[] reversedArr = new int[arr.length];
    for (int i = 0, j = arr.length - 1; j >= 0; i++, j--) {
        reversedArr[i] = arr[j];
    }

    for (int i = 0; i < arr.length; i++) {
        arr[i] = reversedArr[i];
    }
}
```
The issue with the initial code is that it just reassigns indexes from left to right with indexes from right to left. Eventually, the method would reassign the second half of the array with the first half of the array, which already has changes made. For example, {1, 2, 3} becomes {3, 2, 3}.

The solution I provided makes a new array that copies elements in the reverse order. After that, the old array will simply iterate through the new array and copy the elements directly.

# Part 3 #

I have never worked with web servers before, so I thought that lab was pretty cool. I knew a little bit about URL pathing because it was very intuitive to pick up when I had first learned about it. I also knew a little bit about ports because I tried to port forward some servers for my games. Query was something new that I learned as I had never understood what the ? represents in a link. Writing the code to process the query was pretty fun.

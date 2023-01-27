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

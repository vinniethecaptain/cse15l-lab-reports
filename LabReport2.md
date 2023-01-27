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
            return "default";
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

![](https://media.discordapp.net/attachments/766148831594545153/1068367935824986172/image.png)
![](https://media.discordapp.net/attachments/766148831594545153/1068368166817890356/image.png)

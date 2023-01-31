# Lab Report 3

## Part 1: Creating the StringServer
The web server `StringServer` is implemented below. It adds to a string, named `message`, as it receives requests.
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    //String to be added to
    String message = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return message;
        }
        else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            message += "\n"+parameters[1];
            return message;
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

Here are two examples of messages being added.

![Image]()

The method being called is `handleRequest(URI url)`, which parses the request into a message string. The string "add-message" is present in the request, so the server's message will be added to. Here, the relevant argument being passed is "Here is a message". The `message` variable in the `Handler` class is concatenated with a new line and the message to be added.

![Image]()

Another "add-message" request is passed to the server. The process is repeated, except this time the relevant argument passed to the `handleRequest(URI url)` method is "Here's another one". The string `message` in the `Handler` class maintains the first message, and the new one is added on and displayed for the client.

## Part 2: JUnit


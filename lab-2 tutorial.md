# Lab Report 2
## Part 1
In this part, I will be creating my on server StringServer as given in the lab task document. Below is the code for handling the URL in StringServer:
```
class Handler implements URLHandler {
    String message = ""; 
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {  
            return message;
        } else if (url.getPath().equals("/add-message")) { 
            String[] path = url.getQuery().split("="); 
            if (path[0].equals("s")) { 
                message = message.concat(path[1]+"\n");
            }
            else {
                return "404 not found"; 
            }
        } else {
            return "404 Not Found!"; 
        }
        return message; 
    }
}
```

Below is the main method of the application:
```
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




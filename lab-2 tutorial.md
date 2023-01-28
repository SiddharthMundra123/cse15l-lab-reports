# Lab Report 2
## Part 1
In this part, I will be creating my on server StringServer as given in the lab task document. 
* Below is the code for handling the URL in StringServer:
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
* Screenshots of Adding Messages:

![message 1](https://user-images.githubusercontent.com/116845419/215248867-5098a027-1246-4d5b-bc54-0548f3cca087.png)

![message 2](https://user-images.githubusercontent.com/116845419/215248872-41565ec8-35e4-44b1-89b8-ce4d6a1fcd3f.png)

In both of the screenshots, first, the handleRequest and main method is called. The argument to call the main method is 4001 and the argument to call handleRequest is the URL. The value of the variable "message" changes everytime there is a new message added or when the survey is run. The new message is added to the original empty String in line 14 above where path[1] is the new message we add and every time a new message is added, it moves to the next line as we have also added a "\n".

* Screenshot of the error (incorrect URL):

![404 pt2](https://user-images.githubusercontent.com/116845419/215248883-564de987-d92d-4d11-94fe-5fe6e83d84b5.png)


## Part 2
* Failure inducing input for the buggy program: 
``	@Test 
	public void testReverseInPlace() {
    int[] input1 = {1,3,5,9};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{9,3,5,1}, input1);``

* Input that does not induce failure:
``	@Test 
	public void testReverseInPlace() {
    int[] input1 = {1,5,5,1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1,5,5,1}, input1);
	}'''
* Symptom:

![image](https://user-images.githubusercontent.com/116845419/215252092-b048cf2c-909e-49c7-a118-31c09ff5da47.png)



* The bug:

Code with the bug:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  ```

Code without the bug:

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      int x = arr[i];
      arr[i] = newArray[arr.length - i - 1];
      arr[arr.length-i-1] = x;
    }
    return arr;
  }
  ```
  
Describe HERE
  
## Part 3
I learned how to make my own web server and how to make a java application on it as well as JUnit testing. I also learned about GitHub desktop and did not know of this previously.

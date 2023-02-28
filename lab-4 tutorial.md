# Lab report 4
In this lab report, we are required to reproduce the task we did in the lab.

## Step 1:

I logged on into ieng6. To do that, I had to type ```ssh cs15lwi23USERNAME@ieng6.ucsd.edu``` and then I pressed ```<enter>```. After typing my password, I pressed ```<enter>``` again.




## Step 2:

I cloned the given folder using ```git clone ```. while using the copy command for the given ssh link, then I pressed ```<enter>``` to complete the cloning process.


## Step 3: 

I typed l```cd lab7``` to change the directory to the lab7 file's directory. Then, I typed ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` and pressed ```<enter>``` to compile JUnit testing file. Then, I ran the tests using ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore``` and pressed ```<enter>```. As seen below, the testers failed.
![tests failing](https://user-images.githubusercontent.com/116845419/221762737-ed1ddf0b-8fda-42e5-a3b3-a78af6fac915.png)


## Step 4:
To fix the testers, I typed ```nano ListExamples.java```, which opens up the code editor as seen below. I fixed the mistake in the code by going down using the ```<down>``` key and changing ```index1``` to ```index2```.


## Step 5:
Then, when i ran the program again to check if the applciation works correctly, I typed ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` and pressed ```<enter>``` to compile JUnit testing file. Then, I ran the tests using ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore``` and pressed ```<enter>```. As seen below, the tests ran succesfuly.

![Worked after editing](https://user-images.githubusercontent.com/116845419/221762911-1651d276-faa4-4038-87b4-579339927124.png)


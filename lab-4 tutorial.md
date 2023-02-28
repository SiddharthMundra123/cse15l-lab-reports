# Lab report 4
In this lab report, we are required to reproduce the task we did in the lab.

## Step 1:

I logged on into ieng6. To do that, I had to type ```ssh cs15lwi23USERNAME@ieng6.ucsd.edu``` and then I pressed ```<enter>```. After typing my password, I pressed ```<enter>``` again.

![image](https://user-images.githubusercontent.com/116845419/221768148-85b165c3-e28e-412e-adf0-bc81a14248e3.png)



## Step 2:

I cloned the given folder using ```git clone ```. while using the copy command for the given ssh link, then I pressed ```<enter>``` to complete the cloning process.

![image](https://user-images.githubusercontent.com/116845419/221768448-bf04989e-8ba7-4936-9a89-1db7e3815eaa.png)


## Step 3: 

I typed l```cd lab7``` to change the directory to the lab7 file's directory. Then, I typed ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` and pressed ```<enter>``` to compile JUnit testing file. Then, I ran the tests using ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore``` and pressed ```<enter>```. As seen below, the testers failed.

![tests failing](https://user-images.githubusercontent.com/116845419/221763139-f4548fc8-34e8-4ed3-bfec-753d5786a11c.png)



## Step 4:
To fix the testers, I typed ```nano ListExamples.java```, which opens up the code editor as seen below. I fixed the mistake in the code by going down using the ```<down>``` key and changing ```index1``` to ```index2```.


![image](https://user-images.githubusercontent.com/116845419/221768560-9df4e42d-e998-438f-bf97-e26d86f24d56.png)



## Step 5:
Then, when i ran the program again to check if the applciation works correctly, I typed ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` and pressed ```<enter>``` to compile JUnit testing file. Then, I ran the tests using ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore``` and pressed ```<enter>```. As seen below, the tests ran succesfuly.

![Worked after editing](https://user-images.githubusercontent.com/116845419/221762911-1651d276-faa4-4038-87b4-579339927124.png)

## Step 6:

To commit the file on github, I first typed ```git add ListExamples.java``` and then pressed ```<enter>```. After that, I typed ```git commit -m "fixed code"``` whihc commits the file with a message of "fixed code". 

![image](https://user-images.githubusercontent.com/116845419/221768838-a401b6e2-899c-4776-bb3f-3108b91f06b4.png)


## Step 7:

Lastly, to push the commit to GitHub, we have to type ```git push origin main``` and press ```<enter>``` which pushes the commit to the main branch of github.

![Screenshot 2023-02-27 220117](https://user-images.githubusercontent.com/116845419/221767828-24d1c967-cb51-43b6-ada5-d040fc1b9727.png)


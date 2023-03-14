# Lab report 5
For this lab report, I decided to return to lab report number 3 and explore a command similar to grep. I decided to research about find, which has a similar purpose to the grep command. The “find” command is used to find, filter, or search files and folders in your system according to user-specified conditions and perform several operations on them. The following are 4 interesting command-line options about the find command - 
* -name : this command is used to find files with a specific name
* -exec rm -i {} \; : this command is used to delete a file with confirmation
* -iname : this command is used to find files using their name while ignoring case
* -size : this command allows you to print files based on their size

I found all of these on https://www.tecmint.com/35-practical-examples-of-linux-find-command/. Below are the examples of using these commands

## Command 1: -name
**Example 1**
```[cs15lwi23ace@ieng6-202]:~:510$ cd skill-demo1-data
[cs15lwi23ace@ieng6-202]:skill-demo1-data:511$ find ./written_2 -name WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
```
This command finds the file in the directory we are in and returns the path of the file if found.

**Example 2**
```
[cs15lwi23ace@ieng6-202]:skill-demo1-data:512$ find ./written_2 -name WhereToIndia.txt 
./written_2/travel_guides/berlitz1/WhereToIndia.txt
```
As we can see above, it returns the path of the file WhereToIndia .

## Command 2: -exec rm -i {} \;
**Example 1**
```
[cs15lwi23ace@ieng6-202]:skill-demo1-data:530$ find ./written_2 -name WhereToFrance.txt -exec rm -i {} \;
rm: remove regular file './written_2/travel_guides/berlitz1/WhereToFrance.txt'? Y
```
This command is used to delete a file with confirmation. As seen above, once we type the command to delete a file, it asks for confirmation and it only deletes the file if we type "Y" to confirm.

**Example 2**

```
[cs15lwi23ace@ieng6-202]:skill-demo1-data:531$ find ./written_2 -name WhereToIndia.txt -exec rm -i {} \;
rm: remove regular file './written_2/travel_guides/berlitz1/WhereToIndia.txt'? y
```
As seen above, it asks for confirmation before deleting the file. Only if we confimr, then it delets the file.

## Command 3: -iname
**Example 1**
```
[cs15lwi23ace@ieng6-202]:written_2:550$ find ./travel_guides -iname California-WHATTODo.txt
./travel_guides/berlitz2/California-WhatToDo.txt
```
This find command still returns the file path despite the search query having different cases than the actual file name.

**Example 2**
```
[cs15lwi23ace@ieng6-202]:written_2:551$ find ./travel_guides -iname ATHENS-INTRO.TXT       
./travel_guides/berlitz2/Athens-Intro.txt
```
This find command still gives the output even though none of these files are named "ATHENS_INTRO.txt" (the command ignores capitalizaitions while searching). It is to note that if we just use "-name" istead of "-iname", it does not return anything since "-name" does not ingore cases while searching. 
```
[cs15lwi23ace@ieng6-202]:written_2:552$ find ./travel_guides -name ATHENS-INTRO.TXT
[cs15lwi23ace@ieng6-202]:written_2:553$ 
```
As seen above, just using "-name" does not return anything since it is case sensitive.

## Command 4: -size 
**Example 1**
```
[cs15lwi23ace@ieng6-202]:written_2:504$ find . -size -5k
./travel_guides/berlitz1/HandRHongKong.txt    
./travel_guides/berlitz1/HandRIbiza.txt       
./travel_guides/berlitz1/HandRIstanbul.txt    
./travel_guides/berlitz1/HandRJerusalem.txt   
./travel_guides/berlitz1/HandRLakeDistrict.txt
./travel_guides/berlitz1/HandRLasVegas.txt    
./travel_guides/berlitz1/HandRLisbon.txt      
./travel_guides/berlitz1/HandRLosAngeles.txt  
./travel_guides/berlitz1/HandRMadeira.txt     
./travel_guides/berlitz1/HandRMallorca.txt    
./travel_guides/berlitz1/WhatToFrance.txt     
./travel_guides/berlitz1/WhatToHawaii.txt     
./travel_guides/berlitz1/WhereToHawaii.txt    
```
The find -size command allows you to search for files based on their size. The - in the above example means "smaller than". The size is then followed by a size unit, such as k for kilobytes, M for megabytes, c for bytes. The example above prints files less than 5 kilobytes.

**Example 2**

```
[cs15lwi23ace@ieng6-202]:written_2:505$ find . -size +200k
./travel_guides/berlitz1/WhereToItaly.txt    
./travel_guides/berlitz2/Canada-WhereToGo.txt
```

The find -size command allows you to search for files based on their size. The + in the above example means "greater than". The size is then followed by a size unit, such as k for kilobytes, M for megabytes, c for bytes. The example above prints files greater than 200 kilobytes.



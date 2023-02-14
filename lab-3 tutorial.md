# Lab report 3
In this lab report, we are required to research about a specific command. I chose to research about the grep command. The following are 4 interesting command-line options about the grep command - 
* -i : this command is used to ignore capitalizaitions while searching for a match.
* -c : this command prints a count of matching lines for each input file.
* -H : this command is an indicaor to print the file name as well for each match.
* -x : this command selects only those matches that exactly match the whole line. It is to note that if this is used along with -x, -x has precedence.

I found all of these on https://man7.org/linux/man-pages/man1/grep.1.html. Below are the examples of using these commands.
## Command 1: -i
**Example 1**
```
[cs15lwi23ace@ieng6-203]:written_2:318$ grep -ilr "lucayans"
travel_guides/berlitz2/Bahamas-History.txt
```
This grep command still the Bahamas-History.txt file even though Bahamas-History.txt contains the capitalized word "Lucayans".


**Example 2**
```
[cs15lwi23ace@ieng6-203]:written_2:319$ grep -ilr "poRtUgAl"
non-fiction/OUP/Castro/chL.txt
travel_guides/berlitz1/HandRMadeira.txt
travel_guides/berlitz1/HistoryMadeira.txt
travel_guides/berlitz1/HistoryMalaysia.txt
travel_guides/berlitz1/IntroMadeira.txt
travel_guides/berlitz1/WhatToMadeira.txt
travel_guides/berlitz1/WhereToHongKong.txt
travel_guides/berlitz1/WhereToIndia.txt
travel_guides/berlitz1/WhereToMadeira.txt
travel_guides/berlitz2/Algarve-History.txt
travel_guides/berlitz2/Algarve-Intro.txt
travel_guides/berlitz2/Algarve-WhereToGo.txt
travel_guides/berlitz2/Amsterdam-History.txt
travel_guides/berlitz2/CanaryIslands-History.txt
travel_guides/berlitz2/Costa-WhereToGo.txt
travel_guides/berlitz2/Portugal-History.txt
travel_guides/berlitz2/Portugal-WhatToDo.txt
travel_guides/berlitz2/Portugal-WhereToGo.txt
```
This grep command still gives the output even though none of these files contain the word "poRtUgAl" (the commands ignores capitalizaitions while searching)

## Command 2: -c (the actual result is very long and would take up too much space, hence I am only displaying some of the results.)
**Example 1**
```
[cs15lwi23ace@ieng6-203]:travel_guides:331$ grep -rc "university"
berlitz2/Nepal-History.txt:0
berlitz2/Nepal-WhatToDo.txt:0
berlitz2/Nepal-WhereToGo.txt:0
berlitz2/NewOrleans-History.txt:0
berlitz2/Paris-WhatToDo.txt:1
berlitz2/Paris-WhereToGo.txt:3
berlitz2/Poland-History.txt:1
berlitz2/Poland-WhatToDo.txt:0
berlitz2/Portugal-History.txt:0
berlitz2/Portugal-WhatToDo.txt:1
berlitz2/Portugal-WhereToGo.txt:5
berlitz2/PuertoRico-History.txt:0
berlitz2/PuertoRico-WhatToDo.txt:0
berlitz2/PuertoRico-WhereToGo.txt:1
berlitz2/Vallarta-History.txt:0
berlitz2/Vallarta-WhatToDo.txt:0
berlitz2/Vallarta-WhereToGo.txt:0
```



**Example 2**
```
[cs15lwi23ace@ieng6-203]:travel_guides:332$ grep -rc "however"   
berlitz2/Berlin-History.txt:2
berlitz2/Berlin-WhatToDo.txt:0
berlitz2/Berlin-WhereToGo.txt:1
berlitz2/Bermuda-WhatToDo.txt:0
berlitz2/Bermuda-WhereToGo.txt:2
berlitz2/Bermuda-history.txt:1
berlitz2/Boston-WhereToGo.txt:3
berlitz2/Budapest-History.txt:3
berlitz2/Budapest-WhatToDo.txt:3
berlitz2/Budapest-WhereoGo.txt:8
berlitz2/California-History.txt:3
berlitz2/California-WhatToDo.txt:2
berlitz2/California-WhereToGo.txt:3
berlitz2/Canada-History.txt:1
berlitz2/Canada-WhereToGo.txt:0
berlitz2/CanaryIslands-History.txt:3
```

## Command 3: -H
**Example 1**
```
[cs15lwi23ace@ieng6-203]:berlitz1:370$ grep -Ho "place to" *       
HandRJamaica.txt:place to
HandRJamaica.txt:place to
HandRJamaica.txt:place to
HandRMadrid.txt:place to
HistoryLasVegas.txt:place to
HistoryLasVegas.txt:place to
HistoryMalaysia.txt:place to
IntroHongKong.txt:place to
IntroIbiza.txt:place to
IntroLosAngeles.txt:place to
IntroMallorca.txt:place to
IntroMallorca.txt:place to
JungleMalaysia.txt:place to
WhatToHongKong.txt:place to
WhatToHongKong.txt:place to
WhatToIbiza.txt:place to
```

**Example 2**
```
[cs15lwi23ace@ieng6-203]:berlitz1:372$ grep -Ho "travel here" *
WhereToGreek.txt:travel here
WhereToIndia.txt:travel here
```

## Command 4: -x
**Example 1**
```
[cs15lwi23ace@ieng6-203]:non-fiction:400$ grep -lrx "The Nation as the Crucible 
> of Equality" .
./OUP/Fletcher/ch5.txt
```

**Example 2**
```
[cs15lwi23ace@ieng6-203]:non-fiction:402$ grep -lrx "From this point of view, the wonderful Arrow-Debreu theory is fundamentally flawed."
OUP/Kauffman/ch9.txt
```




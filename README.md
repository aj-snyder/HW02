# HW02
tfcb HW02 10_19_22

Homework 2: Unix shell
This homework will assess your ability to run commands in the shell and make a simple script.
Replace the lines specified in italics with your answers and save as a text file.

## Problem 0
60 points

Complete the interactive tutorial.
Did you hit any points of frustration, and if so, how could we improve the material to avoid that frustration?

I did not hit any major points of frustration. I know others were having issues with the man-man function while working in VS code however I was working directly in the terminal and had no issues. It was helpful for me to be taken step-by-step through the tutorial with your added comments and suggestions "mash the keys and see what happens" As I found myself being nervous I was going to mess something up. Refreshing to see if something doesn’t work you can simply "return" and try again.




## Problem 1
20 points

Write a script that outputs some user and location data and moves that output to a newly created directory
Make a single script that prints out a file called question01.txt.
This file should contain the following text:
  My name is (your username, but the script needs to work for anyone, not just you)
  My home directory is (your home directory, but the script needs to work for anyone, not just you)
  The contents of the tfcb_2022/lectures/lecture04/ directory are
  (prints the contents of that directory)
  This script should also create a directory called homework02, and move question01.txt into the homework02 directory.

Example: My name is melody My home directory is /Users/melody The contents of the tfcb_2022/lectures/lecture04/ directory are 01-first-steps.md 02-directories 03-redirection 04-vim 05-history 06-scripting 07-more-interactive-shell README.md quickref.md sequence.gb slides vader.txt


### AS script: 
a.j.@AJs-MacBook-Air ~ % mkdir homework02 
a.j.@AJs-MacBook-Air ~ % echo "My name is " $USER > question01.txt
a.j.@AJs-MacBook-Air ~ % echo "My home directory is " $HOME >> question01.txt
a.j.@AJs-MacBook-Air ~ % echo "The contents of tfcb_2022/lectures/lecture04/ directory are: " >> question01.txt
a.j.@AJs-MacBook-Air ~ % for filename in $(ls tfcb_2022/lectures/lecture04/); do echo $filename >> question01.txt; done
a.j.@AJs-MacBook-Air ~ % mv question01.txt homework02

### AS validation 
a.j.@AJs-MacBook-Air ~ % cd homework02
a.j.@AJs-MacBook-Air homework02 % ls
question01.txt
a.j.@AJs-MacBook-Air homework02 % cat question01.txt
My name is  a.j.
My home directory is  /Users/a.j.
The contents of tfcb_2022/lectures/lecture04/ directory are: 
01-first-steps.md
02-directories
03-redirection
04-vim
05-history
06-scripting
07-more-interactive-shell
README.md
quickref.md
sequence.gb
slides
tfcb_2022
vader.txt
a.j.@AJs-MacBook-Air homework02 % 


## Problem 2
20 points

Write a script that uses a loop to output files with specific names
Make a single script that does the following:
Makes a new directory in homework02 called question02
In that directory, your script should make 25 new files called file###.txt
the ### should be the numbers from a list you can find here: tfcb_2022/homeworks/homework02/list.txt
You can make the contents of those files whatever you want (hint: slide 10... what was the contents of the fake "jpg" file?)



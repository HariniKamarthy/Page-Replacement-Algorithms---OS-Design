Page Replacement Algorithms Implementation README
==================================================

This is the README file for our Page Replacement algorithms Implementation code file.

Here we have 2 Structs to store the Pages Info and Page Faults info.

initializePage Method Implementation
---------------------------------------------------

Parameter page_number is passed inside the function.
Initializes all the related data of a Page.

findPageIndex Method Implementation
-------------------------------------------

Function to find the index of a page in a frame array.
Frames array, page number and number of frames are passed as parameters.
Runs a for loop for number of frames times and returns the index of a page in a frame.

displayFrames Method Implementation
-------------------------------------------
Function to display the current state of frames after each request.
Frames array and number of frames are passed as parameters.
Runs a for loop for number of frames times and returns the page number of all frames after each request.

fifoPageReplacement Method Implementation
-------------------------------------------
Function to perform the FIFO Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the FIFO page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

optimalPageReplacement Method Implementation
----------------------------------------------
Function to perform the Optimal Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the Optimal page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

lruAdditionalReferenceBits PageReplacement Method Implementation
------------------------------------------------------------------
Function to perform the LRU (Additional Reference Bits) Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the LRU (Additional Reference Bits) page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

lruSecondChance PageReplacement Method Implementation
-------------------------------------------------------
Function to perform the LRU (Second Chance) Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the LRU (Second Chance) page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

lruEnhancedSecondChance PageReplacement Method Implementation
---------------------------------------------------------------
Function to perform the LRU (Enhanced Second Chance) Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the LRU (Enhanced Second Chance) page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

lfuPageReplacement Method Implementation
-------------------------------------------
Function to perform the LFU Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the LFU page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

mfuPageReplacement Method Implementation
-------------------------------------------
Function to perform the MFU Page Replacement 
Reference String, number of references, number of frames are passed as parameters.
Implements the MFU page replacement logic on the reference string passed using initializePage(), findPageIndex(), displayFrames() functions and also finds & displays the number of Page faults.

comparePageFaults Method Implementation
-------------------------------------------
Function to compare the page faults counts for all the above Page Replacement Algorithms.
PageFaultData is the data type of the function as it returns that data.
Reference String, number of references, number of frames are passed as parameters.
It calls all the page replacement algorithm functions and stores the returned number of page faults values for each algorithm.
Compares & Displays all the page faults in ascending order using bubble sort logic.
And then displays the least page faults algorithm name. But, if, multiple algorithms have least page faults, then it displays all the list of algorithm names with least page faults. Else, if all algorithms have the equal number of page faults, then it displays the same.
It returns the data of Page faults information.

compareIntegers Method Implementation
---------------------------------------
Function just returns an integer by comparing the 2 integers.

calculateStatistics Method Implementation
------------------------------------------
Function to calculate the statistics for the Page faults i.e., average, median, standard deviation using some math library functions say pow(), sqrt().

sumOfArray Method Implementation
---------------------------------
Function to calculate the sum of an array.
Page faults data and number of tests information are passed as parameters.


Main Function
--------------
Main function is passed with 2 arguments, to get the info of number of Pages to generate in a reference string, from the user.
Here we took the frame sizes as 5, 10, 15, 20, 25 in an array, and considered it as 5 different categories. And then for each category, we run the for loop for 5 times to execute all the algorithms and find the page faults for all, in each test case.
Open a file named "reference_strings.txt" and stores the data of generated 5 difference reference strings randomly using rand() function.
Opened the same text file and reads the data of reference strings from the file.
We then used these 5 reference strings for the 1st category i.e., for frame size 5.
And then used these same 5 reference strings for the rest of the test categories i.e., 10, 15, 20, 25.
For each category we then calculated average, median and standard deviation by calling our implemented function "calculateStatistics()", and then displays the data.
Here we have calculated the statistics considering 2 metrics i.e., Total number of Page Faults, Least number of Page Faults, and displayed the both in 2 tabular forms.


Execution
=========

After implementing all these methods in the code file, we have to move all this file to the one of the UNT Servers and execute them in PUTTY, by running the following commands.

To compile, run
$ gcc -o PageReplacementAlgos PageReplacementAlgos.c -lm

To test your implementation providing the value of Number of Process to consider, run
$ ./PageReplacementAlgos 30

You can store the output in a file so that you can look at it carefully:
./PageReplacementAlgos 30 > Output30Pages.txt
./PageReplacementAlgos 40 > Output40Pages.txt
./PageReplacementAlgos 50 > Output50Pages.txt



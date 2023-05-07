Download Link: https://assignmentchef.com/product/solved-parallelcomputing-assignment-4-coarse-grain-synchronization-using-parallel-hashtable
<br>
Activity: Coarse Grain Synchronization using Parallel Hashtable

The purpose of this assignment is for you to learn more about:

<ul>

 <li>creating threads and passing parameters to them,</li>

 <li>the overhead associated with thread management and synchronization,</li>

 <li>designing parallel data structures.</li>

</ul>

As usual all time measurements are to be performed on the cluster.

<h1>1           Preliminary</h1>

Before anything, we will need to get timing for sequential execution.

<strong>Question: </strong>On mamba, navigate to the sequential/ directory. Compile the sequential code with make, and get sequential time by running make bench.

<h1>2           Coarse Grain Synchronization</h1>

<strong>Question: </strong>Write a program that uses a hashtable to track the frequency of words in a given text using multi-threading. You can use the sequential code as a reference.

Note: for this assignment you should not need to make changes to MyHashtable.hpp or Dictionary.hpp (leave them alone). Also note, that the parsing is already done for you.

The easiest way to do this is, after the files have been read and parsed, to create one thread per file, and have each thread read count the words directly to the Hashtable. Main takes 3 parameters:

<ul>

 <li>source: names a file that lists the texts to count from</li>

 <li>testword: (for testing correctness) a string that is looked up at the end of execution</li>

 <li>threshold: (for debugging purposes) a int that specifies to print words that have a frequencies greater than this number</li>

</ul>

Once you have written the program, you can verify that it works with make test once you pass all the tests you can move on.

<strong>Question: </strong>Report time and speedup across a range of executions using various numbers of cores. You can use make bench on mamba to start this process, as it will create 16 jobs. Once they are complete, plot the charts with make plot. Note: you must run these commands from within the coarse grain/ directory. <strong>Question: </strong>Why is the speedup (or slowdown) for coarse grain the way it is?
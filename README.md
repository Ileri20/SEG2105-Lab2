# Lloseng

This repository contains a copy of [the cody required to complete the first assignment](https://github.com/TimLethbridge/Lloseng)
using the book [Object-Oriented Software Engineering: Practical Software
Development using UML and Java](http://www.site.uottawa.ca/school/research/lloseng/), 2nd Edition, 2004 McGraw Hill.
by [Timothy C. Lethbridge](http://www.eecs.uottawa.ca/~tcl) and
[Robert Laganière](http://www.eecs.uottawa.ca/~laganier).

# Lab 2 (to introduce Assignment 1)

Assignment Submission before October 2nd, 11h59pm using [BrightSpace](https://uottawa.brightspace.com/)

During the lab 2, you will start working on your assignment 1. The TA will explain how to setup your environment, how to measure the execution time of a Java program and HOW TO DEBUG!

**INSTRUCTIONS**

* Use the following invitation to join or create a repository for assignment 1. As we did for the lab 1 and project, one member of the team creates the repository, the other joins it. 

```
https://classroom.github.com/g/0VttTNA0
```
* You also need to create a Group in Brightspace (Groups_Assignment1).

**Group work and partners**: In this lab, and all other labs that involve programming, you
will work in **groups of two**. If you have not previously arranged to work with someone
in your lab section, then you will have to find someone immediately. You can also work individually. 
No groups of 3 will be permitted.

## Format

Your **private** repository should be named \[prefix\]-\[student-number-1\]_\[student-number-2\], for example


```
assignment1-1484511_90210901210
```

When finished, submit the following text via the Brightspace submission link: 

* Your names and students numbers
* A link to your GitHub repository.

Your GitHub repository should contain all solutions to the Assignment 1,
no solution submissions via BrightSpace will be evaluated. 
Only the information above should be submitted to BrightSpace.


## Logistics

#### Using Eclipse

Eclipse will be presented in this lab. However, feel free to use your preferred IDE.
Instruction on how to setup your environment will be presented during the beginning of lab 2. Material is available on BS (under lab 2).


#### Exercises

Work on the following exercises from the textbook. You must hand in
only one copy of answers per group. Make sure the names and student numbers
of both partners are clearly indicated. You must work on these questions
during the lab and then finish off the work on your own time before the deadline.

## Analysis of various design alternatives

1. Before coming to the lab, you are asked to read and understand Section 2.9 of
the textbook, starting on page 57. If you have not done this, take five
minutes now to do it.

2. This Lab/Assignment will focus on [PointCP](/pointcp) from this repository,
so all instructions will be relative to that directory.

```
cd pointcp
```

Before making any changes, compile the code and make sure it runs.

```
javac PointCP.java PointCPTest.java
```

To run the program

```
java PointCPTest
```
You can, of course, run the programs using the Eclipse IDE (or your preferred IDE).

## PointCP

All modifications should be done within the `/pointcp` directory.
By modifying the original version (Design 1), implement the following designs.

* design 2 (edit code in `/design2` directory). Add your code in  `PointCP2.java`. 
* design 3 (edit code in `/design3` directory). Add your code in  `PointCP3.java` . 
* design 4 (edit code in `/design4` directory). Add your code in  `PointCP4.java`. 
* design 5 (edit code in `/design5` directory). Add your code in  `PointCP5.java` and modify your existing  `PointCP2.java` and  `PointCP3.java` (to adapt them to the new design requirements.

4. Modify the `PointCPTest` class to allow you to test the designs you
have developed. Do a thorough series of tests to ensure your classes
and interface work properly. You can implement other classes to facilitate the task or add any extar functions to the `PointCPTest` class. 

5. Overwrite the [OUTPUT.md](/pointcp/OUTPUT.md) to clearly provide a printout
of the output generated by your tests for each design.  Clearly
indiciate which design the output is from.

Answer the following exercises in the provided `EXX.md` files
using [GitHub Markdown](https://guides.github.com/features/mastering-markdown/).

* Overwrite [E26](/pointcp/E26.md) (table of what you think will be the advantages and disadvantages of designs 2, 3, 4 and 5)
* Overwrite [E28](/pointcp/E28.md) (performance analysis, comparing all four designs you have implemented instead of Design 1 with Design 5 as the book says)
* Overwrite [E29](/pointcp/E29.md) (similar as E28)
* Overwrite [E30](/pointcp/E30.md) (similar as E28)

To do this evaluation (of E26, E28-E30), for each design create random instances and
then call each method many thousands of times, and then find the elapsed time in milliseconds
for the fixed number of iterations. Make sure that your program runs each time for about
10 seconds, so you get a good measure of performance. Test each method separately.
Run each version several times to ensure that your results are consistent and use
the median result as your definitive result, plus give the maximum and minimum.

| Design | How cartesian coordinates are computed | How polar coordinates are computed |
| --- | --- | --- |
| Design 2: Store polar coordinates only | Computed on demand, but not stored| Simply returned |
| Design 3: Store cartesian coordinates only | Simply returned | Computed on demand, but not stored |
| Design 4: Store both types of coordinates, using four instance variables| Simply returned | Simply returned |
| Design 5: Abstract class with designs 2 and 3 as subclasses| Depends on the concrete class used | Depends on the concrete class used |

6. Overwrite the [TESTING.md](/pointcp/TESTING.md) file and clearly describe

* how you did the tests,
* sample outputs from running the tests
* the table and
* a discussion of the results.

## ARRAYS

7. Compare the performance of LinkedList, Vector and ordinary arrays.
You should do a series of experiments where you do each of the
following tests with the three types of collection,
timing the execution of each run.

You should run each case several times on the same computer to
obtain stable average timings.

a. Construct very large collections by putting random characters (char type) into each collection one at a time. The random characters should range in value from 'a' to 'z'. You should make each collection large enough so that the run takes at least 10 seconds to add the characters in the case of an ArrayList. You will have to do some initial experiments to find out what is a good size. You would use the same size of collection for Vector, LinkedList and the array. The Vector and LinkedList can be created by successively adding items and allowing them to grow, while the array has to be created at its full size and then populated with its contents. You could also try to experiment with the case where you do create the Vector and LinkedList initially with their full size.

b. Construct very large collections as in (a). Then use iterators to sum the elements. Subtract the construction time to get a measure of how much time the iteration takes. Use a for loop for the array, and an Iterator for the LinkedList and Vector.

Overwrite the [ARRAY.md](/pointcp/ARRAY.md) to present your data in
suitable tables and draw conclusions from an analysis of the data.
From your conclusions, develop recommendations to designers. Make you discuss about the performance, data growth and most common application of the three options.

If you have questions related to the assignments, please use the Piazza forums (tag assignment1)! 

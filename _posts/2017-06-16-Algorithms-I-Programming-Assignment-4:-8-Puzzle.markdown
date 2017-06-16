---
layout: post
title:  "Algorithms I Programming Assignment 4: 8 Puzzle"
date:   2017-06-16 23:00:00 +0800
categories: Algorithms Assignment
---
The purpose of writing this post is to collect **issues** I encountered during doing programming assignments and **solutions** to them, and any useful **notes** that I would like to write down. 

Here is the [assignment specifications][spec], and the [checklists][faq].

[spec]: http://coursera.cs.princeton.edu/algs4/assignments/8puzzle.html
[faq]: http://coursera.cs.princeton.edu/algs4/checklists/8puzzle.html
<br><br>
## Issues
* **Inner class private fields accessibility**

  **Issue description:** 

  Can a top level class access private members of a nested class inside the top level class? (can also see [the same question on stackoeverflow here.][stackoeverflow question 1]

  For example: why the private member, k of Line class, can be accessed in "print" method of outter class?
 ```java
 public class myClass {
     public static class Line{
         private double k;
         private double b;
         private boolean isVertical;
 
         public Line(double k, double b, boolean isVertical){
             this.k = k;
             this.b = b;
             this.isVertical = isVertical;
         }
 
     }

     public static boolean print(Line line){
         System.out.println(line.k);
     }
 }
 ```

  **Answer:** 

  [The rules are in the JLS chapter on accessibility][jls rule]:
  > Otherwise, if the member or constructor is declared `private`, then access is permitted if and only if it occurs **within the body of the top level class (§7.6) that encloses the declaration of the member or constructor.**

  [stackoeverflow question 1]: https://stackoverflow.com/questions/19747812/why-can-the-private-member-of-an-nested-class-be-accessed-by-the-methods-of-the?lq=1
  [jls rule]: http://docs.oracle.com/javase/specs/jls/se7/html/jls-6.html#jls-6.6.1

<br><br>
* **Memory Test Failed**
  
  **Issue description:** 

  I failed the memory test several times. Here is the details in [discussion forums.][forum]
  
  **Answer:** 

  A mentor of the forum replied to this question:

  >I have kept all the priority queue and search node linked list structures on the function stack versus as a class member . This way after the algorithm runs the Solver object doesn't keep unnecessary memory objects and it keeps only what it needs to. I mean neither the Search Node linked instances nor the Priority Queue should be a **class member** and that they should be **function scope variables** during the execution of the A* algo within the **constructor**.

  Original codes:

  ```java
  public calss Solver
  {
	private MinPQ<SearchNode> solverPQ = new MinPQ<SearchNode>(new ManhattanComparator());
	private MinPQ<SearchNode> solverPQTwin = new MinPQ<SearchNode>(new ManhattanComparator());
	private SearchNode finalNode;

	public Solver(Board initial)           // find a solution to the initial board (using the A* algorithm)
	{
		...
	}
  }
  ```

  Modified codes:

  ```java
  public calss Solver
  {
	private SearchNode finalNode;

	public Solver(Board initial)           // find a solution to the initial board (using the A* algorithm)
	{
		MinPQ<SearchNode> solverPQ = new MinPQ<SearchNode>(new ManhattanComparator());
        MinPQ<SearchNode> solverPQTwin = new MinPQ<SearchNode>(new ManhattanComparator());
        ...
	}
  }
  ```

  In this way, `garbage collector` will free unnecessary memory objects(mostly, two priority queue objecs) after the excution of the Solver constructor. The solution(from the final search node containing goal board all the way back to the initial search node) will be kept becasue the `finalNode` is a class member which will remain after excution of the Solver constructor, and each node records its previous node, so the solution can be reconstructed.

  [forum]: https://www.coursera.org/learn/algorithms-part1/discussions/weeks/4/threads/d3rrTQV7Eee36g5uvZCkbA

<br><br>
* **Return iterable objects**
  
  **Issue description:** 

  How do I return an Iterable<Board>? 

  **Answer:** 

  Add the items you want to a **Stack\<Board\>** or **Queue\<Board\>** and return that. Of course, your client code should not depend on whether the iterable returned is a stack or queue (because it could be some any iterable).

<br><br>
## Notes
* **How to format strings?**
  
  Use String.format() to format strings—it works like StdOut.printf(), but returns the string instead of printing it to standard output. Two useful links:

  [Oracle The Java™ Tutorials: The StringBuilder Class][stringbuilder toturial]

  [When to use StringBuilder in Java?][when to use]

  [stringbuilder toturial]: https://docs.oracle.com/javase/tutorial/java/data/buffers.html
  [when to use]: https://stackoverflow.com/questions/4645020/when-to-use-stringbuilder-in-java

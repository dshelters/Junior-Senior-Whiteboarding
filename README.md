# Junior-Senior-Whiteboarding

## The Focus
The focus of this exercise is communication. As interviewers we will be very very vague when asking these questions in order to force the Juniors to understand that they will need to continually ask us questions to totally understand the problem.

This is also an exercise in visualizing the problem on the whiteboard. At no point should they not be trying to show you what they mean by sketching it out on the board.

## Problem Prompts

#### _Soda Machine_
> You have an old soda vending machine used in blind taste tests. The machine has three buttons labeled, "Coke," "Pepsi," and "Surprise." Whichever button is pressed, a nondescript can of soda pops out containing either Pepsi or Coke - the surprise button is supposed to randomly give a can of one or the other. Trouble is, some rascal has gone and messed with the labels. Luckily, you are an expert at telling the difference between Pepsi and Coke, so if you sample one of the cans, you will be able to determine which soda it is (even though the can is no help). How many sodas must you drink to guarantee you will be able to put the labels back where they belong?

##### Notes for the Interviewer
This is a good warm up problem. The real point here is for the interviewee to actually find out the constraints. Mainly that ALL of the labels are incorrect. If they ask tell them this. If they don't, and assume that the labels may or may not be correct let them continue to ruminate about it and go off course.

###### Hints
1. What if you discovered that the surprise button gave you a Coke?
2. (Only if they ask!) All of the labels are incorrect.
---
#### _25 Horses_
> Let’s say that you have 25 horses, and you want to pick the fastest 3 horses out of those 25. In each race, only 5 horses can run at the same time because there are only 5 tracks. What is the minimum number of races required to find the 3 fastest horses.

##### Notes for the Interviewer
Once again this exercise is about communication. The goal is to intentionally vague to force the interviewee to ask you questions about the contrainst and nuances of the problem.

Do not tell them anything at first about how you know the top 3 finishers in each race. They need to gather as much information from you as possible.

If they come to a conclusion like "It takes 13 races" be sure to ask them why and push them to try again and get it lower to something like 10, then 7.

###### Hints
1. There is no stopwatch.
2. You know the finishing positions of the horses.
3. Draw it out!
4. The horses always run at the same speed no matter the number of races.

###### Answer
7 Races

---
#### _Cyclical Linked List_
> Write a function to detect if a linked list has a "cycle" (a loop), without extra storage.

> E.g., A->B->C->B is a linked list with a loop in it. 
How can you programmatically determine that it has a cycle, without using any other data structures?

##### Notes for the Interviewer
This problem is meant to focus on diagramming and getting to a working solution with pseudocode on the whiteboard. Syntax is not important at all.

This is very much something the junior will either get or they won't. It's good to use to get the interviewee to continually talk about their thought process. There are multiple solutions to this problem. If they get to answer that isn't the one below hint that there is a more efficient solution.

###### Hints
1. None

###### Answer
The standard way to do this is to have a "fast" and "slow" pointer.
(Sometimes called "hare" and "tortoise" pointers. )
The slow pointer moves ahead 1 node at a time. The fast pointer moves ahead 2 nodes at a time.

Start the two pointers at the head and "run" them along at their different speeds.
If they meet, the linked list has a cycle in it.

The fast pointer should always start first, or the slow pointer will always catch up.

I.e., otherwise, given A->B->C->D->etc... here's what the beginning of the run looks like:

fast pointer is A, slow pointer is A
slow pointer goes to B <--- this is the problem, slow pointer should not go first!
fast pointer goes to C
slow pointer goes to C
slow and fast are on the same node, so we falsely detect a cycle. <--- the symptom

# Design notebook entry

## Last week's critique

I definitely needed the help this week. Charlie helped on monday and Prof Ben helped on Wednesday. I think we are all dealing with that classic project situation of biting off more then we could chew. Im happy with the progress im making and the changes I can make, but im defintely far from the original goal. 

## Description

This week I focused on getting the basic version of the parser and functionality for the language done. And by done, I mean 
the most basic version. So currently a program of the shape: 
```
roll name { 
1d6
}
```
would compile. You could of course change either of the numbers and it would react accordingly. Currently `2dX` evaluates to `1dX + 1dX`. And the name can be any reasonable string. And it works! After some help from prof Ben, I was able to get the system to actually parse this basic code. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Now that I have the basic structure complete, I can make progress on implementing *stat* which will be a lot harder, since it needs to start outputing a graph of some capacity. Also checks are something I would like to add but aren't strictly necessary. because right now, equations dont even work, so figuring how to add elements and implement basically math again is key. 

The biggest design decision I have to make is about how rolls are stored, since they should be evaluated on call, we need to watch out for over functional implecations. Basically I need to keep things simple, without limited the end user functionality. 

**What questions do you have for your critique partners? How can they best help
you?**
. I think some big questions are how much I should tone down the project. What are key features of interacting with "dice" that I need to figure out. 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

I think about 5-7 hours, not including class time. 

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Badly, definitely behind "schedule" but also im not too worried. Ive been enjoyuing the project at this pace. 

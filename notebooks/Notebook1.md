# Design notebook entry

## Last week's critique

It was very nice being able to talk with my tablemate on monday. I feel like we both have similar goals in the project. Although the actually feedback on my project was minimal, there we key insights I learned from our interaction. 

First off, I definitely realized how badly defined my project was. Although I knew what I *wanted* I didn't really have any logistics figured out. Sure, a gui that a user can interact with is easy to say but not easily done. I also realized we both probably over commited to a project ie made it more complicated then can be done in the time required. So going into this designing section I want to clearly define these issues. 

In tandem with that I need some clear examples of the DSL. The feedback showed me that how the dsl will work also needs some defining. Is it something that rolls singular events? Or something that creates graphs? That is a question I need to answer. Ideally both but again we need to keep it realistic.

## Description

So the first step of this week was working to create a step by step guide of 1 what I was making and 2 how I was going to do it. In advance I apologize for the format of these and specifically how the typing ends up looking. I have dyslexia and it can make some of my sentences really impossible to understand (I swap word order alot). Feel free to comment on those in reviews so I can fix them. 

### Research: 
Firstly Here are some documents that  I might return to in my implemntation of the project
 - [Create an Exectuable Command Prompt Script](https://stackoverflow.com/questions/13975733/how-to-create-an-executable-command-prompt-script)
 - [Executing Shell Commands in Python](https://stackabuse.com/executing-shell-commands-with-python/)
 - [Convert Python To Executable](https://towardsdatascience.com/how-to-easily-convert-a-python-script-to-an-executable-file-exe-4966e253c7e9)
 - [Scalapy -- Running Python packages in Scala](https://github.com/scalapy/scalapy)
 - [Turning and Exporting a Scala Project as One single .jar file](https://github.com/sbt/sbt-onejar)
 - [GUI programming in Scala](https://otfried.org/scala/gui.html)


### Thoughts: 

From my research the actual structure of my program, I chose to do the following: The DSL will be a External Domain language, and implemented in scala. While I did a internal one for the previous project, I will have some guidence from others that did external while I set that up. Then, the external DSL will be set into a simple GUI following the tutorial above. Im not going to focus on prettyness or anything like that, I imagine this will be simple and I will focus mostly on the implementation of the language. The gui will either allow directly editing a text document and a run button, or to select a already written text file. 

The language will have two overarcing setups. 1 build a roll roll {description} and then enacting stats on that roll. Rolls can be reused by a name and can be nested if possible. See design for more. The creation of stats would use the Scalapy package to grab some python graphing packages. There might be some scala graphing packages tho, so Ill keep an eye out for that. 

Lastly, I will convert the scala to a single jar file as above. So the final checklist is 
- Make the simplest working version of the DSL 
- Make a Simple *working* GUI
- Set up Jar adaptation 
- Add Stats to DSL
- Improve DSL 
- Improve GUI 

### Design :

This is a preliminary design but this is what I want people to be able to create and explore with the system. 
Making a roll: (basically a function that outputs a number) 
```
roll alpha {

1d6 + 7

}
```
note: 1d6 evaluates to a roll object. 

Making a check: (basically a fucntion that outputs a succes or failure -- maybe add allowance for multiple successes reported?) 
```
check beta {

5d6 if >10 

}
```
note: 5d6 evaluates to a list of 1d6's that are then each rolled by if and compared to 10 

Making a stat: (output stats with various parameters) 
```
roll gamma {
 alpha + 1d6
}

stat beta (parameters)
stat gamma (parameters)
```
This still needs some refinement. I want to break away from coding conventions, but we know thats very difficult. 



## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I feel much better about starting now. The most pressing issue is I have is I dont have experience with external implementations. Something my DSL relies on. Hopefully I can get guidence from the rest of the class on how that works. 
I need to make the **big jump** from the *layout* and *construction* of a DSL to its actual design. I want to break away from the expectations of a traditional coding language and allow it to be relatively simple to write, especially since most applications will be simple. But the modularity and the recursiveness is defined well. 

**What questions do you have for your critique partners? How can they best help
you?**

Does the structure make sense? Both the actual construction of the DSL (gui, scala etc) and the actual DSL design. Plus any name suggestions would be great! 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

Ahhhh I have no idea. Everything has been done in github but Ive been so busy and working on this during the cracks of freetime I have 

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

It went ok. I feel like I made more progress then I expected and the research was very very helpful. Lets see how implementation goes. 

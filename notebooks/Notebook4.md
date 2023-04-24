# Design notebook entry

## Last week's critique

Last week I got alot of discussion about dealing with generating stats. We talked about package options and how to connect it with the overall setup. We talked about looking into our old PL's Work in order to work about Expressions. 

## Description

This week I worked on getting *stat* setup. I started with seting up the code interpreter to grab the roll called *main* and print out stats for it. So currently the actual command *stat* is not implemented but run automatically on main. (very programmer of me).  

The original goal was to use plotly and output bar graphs of the results. However that library did not work. So I looked for more library options in scala In fact I tried many of the ones listed in [this](https://analyticsindiamag.com/top-7-scala-libraries-for-data-visualisation/) article. The ones I didnt try had other reasons they didnt work. Such as not having bar graph options, or being overly complicated for the implementation I wanted. 

As a result (and after asking for help from prof Ben) I went to an ascii implementation. Its very simple. It rolls main 1000 times, and takes that data and converts it to a little ascii bar graph (sideways since its easier to implement) 

Goals going forward: The next thing I want to do is add custom dice sides and update the statistics to allow that successfully. 
Specifically the following implementation: 

```
roll CustomDie1 {
  1d[1,1,2,3]
}
```

Which would simulate a 4 sided die with each list item representing a side. That is each list item has an equal chance of appearing when rolled. This will possibly include non int implementations, that is `1d["hello","howdy"]`. I think the system will treat anything thats not an number as a string, therefore you couldnt have custom objects or booleans. This is because the elements must have an `+` defined. (That is you can added them together) which does work for strings. So `2d[a,b,c,d]` could be `"ab"`, `"bb"`, `"da"` etc. 

This would require some changes to how the graphs are calculated, but the main change is that the data it loops through is now a dictionary rather then a list of dice results. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think the most pressing issue is what key features do I try to implement in this last week. If theirs anything that seems most important I would love to prioritized it. 



**What questions do you have for your critique partners? How can they best help
you?**

Does my implemtation above make sense? Intuitively I mean. I think custom dice just being a list is intuitive, and it replaces the definition of the number of sides. Also see above. Should I prioritize something else? 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

About 4-5 hours 

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Im definitely making compremises on the overall goal. But im not unhappy with my progresss. Its actually really cool so far!

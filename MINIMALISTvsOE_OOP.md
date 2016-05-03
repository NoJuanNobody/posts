#MINIMALIST vs Object everything 
##what is the best way to approach object oriented programming in any language?

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">In terms of OOP, should you take a MINIMALIST approach or an object-everything point of view? <a href="https://twitter.com/hashtag/java?src=hash">#java</a> <a href="https://twitter.com/zipcodewilm">@zipcodewilm</a></p>&mdash; alejandro londono (@GOHANDROGO) <a href="https://twitter.com/GOHANDROGO/status/727073247204892673">May 2, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


In my first week here at ZipCodeWilmington, I have learned a so much that I could not possibly begin to keep it all in my head, however one thing seemed to stick out to me about programming as a software Engineer/Developer

for the majority of my career as a front end dev, I did sometimes delve into some of the stronger languages like Ruby, and PHP, I even looked into bash scripting, but for a majority of my basic work on the front end only ever had to be programmed in a procedural manner. I often had to solve complex problems that had very specific scenarios but all in all, I could always get away with just writing a more complex procedure. Now, **let me tell you why I was completely wrong**

if you were to write some sort of program that would add your groceries to a list it might look something like this:
```javascript
var groceries = [];
groceries.push("eggs")
groceries.push("milk")
groceries.push("bread")
groceries.push("nutella") //IMPORTANT!!

function getGroceries( arr){
//some code here
}

function.getGroceries(groceries)
...
```
this is a procedural approach, where you do one thing after another. for senarios where one thing happens, this works well, it is easy to break apart because it is how we live out lives. 

> first i am going to get eggs, then i am going to get bread and nutella then i am going to pay and leave the supermarket.

there is a problem with procedural development. **it only does one thing, and we can do better.**

if you write one procedure, what happens when you want to buy an extra item, or you want to but two milk cartons. suddenly you need to go into the code and change the behaviour of the entire program. That is the opposite of **encapsulation**. 

with OOP, you want to write objects with three things. Identity, State and behavior. I could get into the syntax about that now but that is not why i am writing this post. most languages have syntax that comes form the grandaddy C++.

if i can quote one of my mentors Tariq: 
> C++ is like the grandpop that is kind of old but he is ripped and he can still bench like 220

Why I am writing this post is because I got into a pretty heated discussion amongst my peers that involved a micdrop at the end. How should one approach your design choices when writing within the OOP approach. should you write from a lean or **Minimalist perspective**, or an **object oriented perspective?** Let me explain

##Minimalist
how can you write the least objects with the most functionality? how can you take a **Calculator** split it into all of its parts slowly merge objects after deconstruction?

this method attempts to create the objects you need, but then "clean up house" in alot of ways this method can be useful in that you can write the problem as it is now and get something going pretty quickly. there is very little forethought needed into how you might architect your software because for the most part...sometimes you only need on object. **some people laughed at me for that, i am going to be honest.**

##Object Everything 
I have a peer that I work with that was tasked with creating a program with many features but seemingly a small amount of objects. His approach was to deconstruct...and keep it that way. at first I could not comprehend why you would want do something like this! but as he explained his logic it really was sound. by separating his concerns he could actually code for the future. and that was something that i had never thought about.



there is a blog post on the [scotch](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design) blog that discusses a concept that [unclebob](https://en.wikipedia.org/wiki/Robert_Cecil_Martin) (Robert C. Martin) has popularized in his career of teaching us all how to code better, together. I want to mention this because I think it gets closer to the real issue at hand. 

the first letter of **SOLID** states that 

> A class should have one and only one reason to change, meaning that a class should have only one job.

it is pretty clear here that my 1 object approach may not have been the best idea for a scientific calculator...

> S – Single-responsiblity principle
O – Open-closed principle
L – Liskov substitution principle
I – Interface segregation principle
D – Dependency Inversion Principle


I have to stress that you read that scotch post for a deeper dive into the subject, but reading through the acronym, it is clear that alot of the idea behind SOLID is that we are a community of coders, and if 300 engineers are all writing to the same project and one thing breaks, if we do not carefully practice [separation of concerns](http://stackoverflow.com/questions/98734/what-is-separation-of-concerns), it is very easy to break something, **AND IF YOU UNIT TESTS PASS BUT YOUR CODE DOES NOT RUN, YOU ARE GOING TO HAVE A BAD TIME MKAY?**

I went to talk to [David Ginzberg](https://twitter.com/DGinzberg) about this and he explained to me that I was really thinking about optimization all wrong. It may feel as though I am writing less by having less objects, but you should optimize **AFTER** not before. just look at the cycle of test driven development:

> FAIL TEST
> pass test by any means necessary
> refactor and repeat

I took the initiative to follow up [Samuel Oloruntoba](https://pub.scotch.io/@kayandrae) who wrote the article on Uncle Bob's OOP principles, and I got a great response. it pretty much says in 3 tweets what it has taken me 15 paragraphs to lead up to 

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/GOHANDROGO">@GOHANDROGO</a> Personally, when working on a project — I tend to do the &quot;minimalist oop&quot; stuff.</p>&mdash; Samuel Oloruntoba (@kayandrae07) <a href="https://twitter.com/kayandrae07/status/727348534966628352">May 3, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/GOHANDROGO">@GOHANDROGO</a> from there, I refactor with plans for the future</p>&mdash; Samuel Oloruntoba (@kayandrae07) <a href="https://twitter.com/kayandrae07/status/727348654760189952">May 3, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>



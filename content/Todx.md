Title: TodX
Date: 2016-05-25 04:16
Category: software
Tags: cpp, productivity

# Todx, A journey

I recently(not today, a couple of weeks till today) created a productivity app named TodX. Well It was and is a adventurous journey. I am taking a little time off and writing this blog highlighting the sweat I have shred in the exhosting and tiring programming, designing and documenting the app.

>First of all, those of you who are intrested about the app can find it here : [TodX](http://arcxon.github.io/todx/)
and the source code on [github](https://github.com/arcxon/todx).

## Pre programming era

This was a huge span of time, where at first thought only one thing : **What To Make**. Yep, It was pretty hard. Actually the app had to be my school's Project for c++ programming. And like most of my classmates I really wanted to make a wonderfully amazing app. But since the knowledge we gained about programming in c++ was mostly commandline thus we were (Or I was) unable to create a full fledged(<-whatever be the spelling) GUI app.

Also I knew I could never make a Bank Management or Train Management app. Not that It was hard (Our teacher already provided us with a sample project for bank management), But It was **very very very ...** (n times) boring. And totally Unusable. (How many of us use a bank management app in our daily life?)

Thus, After a lot of thought I decided to write a simple Note taking app. But It became hard since I had to deal with lots of strings and it was simply too cumbersome writing notes through the commandline rather than just opening a text editor and jotting it down. Hence this Idea was descarded. (Those of you with bold heart can and may be would choose the above Idea, But beware of the dangers you'll face).

My second thought was of a ToDo app. It wasn't very difficult since I already had a mind makeup for something textual. Also the two apps, Note Taking and todo don't have much of a difference. The better part of this decsion was that I didn't had to worry about long pieces of text, thus user entry was smooth and file management was simple and easy.

## Programming

Suprisingly for many of you, this _was_ and _is_ the easiest part of the whole journey. Once I knew what I wanted to program It came out naturally from my fingers to the keyboard to the screen to the compiler and finally to the binary. With a few days of furious logic creation, testing a few inovative algorithms, I had created a usable version of the app. Frankly, This part of journey never complained. Easy Peasy.

## Website and Icon

This was a little confusing time taking and inovative part. Here I borrowed from my previos project [esencia]() and did a little changes to `scss` to get Beautiful website shown below :

![website screenshot](http://i.imgur.com/2MZxbAM.png)

> You can visit it here [website](http://arcxon.github.io/todx/)

And yes **Remember to scroll down**.

The website is a bit flatter and less shadowy than the initial `esencia` theme. The colour scheme is fantastic and is composed of the following two colours `#FFD05D` and `#F06C6C`. The Icon follows similar styling and is shown below :

![icon of todx](http://i.imgur.com/FcYYo2t.png)

At first I designed an awfully ugly and complicated icon which included almost everything I thought of, pencil, paper, tick on checkbox, notebook, the name TodX and a lot more. It was really disastrous. Later I simplified the Icon to a single color background and a checkbox. After trying `linear-gradient`(one of the new things I learned) in css, I applied a gradient in the background of icon. And Viola the beauty defines itself.

## Documentation

> You can find documentation of TodX on : [Read the Docs](http://todx.rtfd.io)

Although I have spent only two days documenting till today it has already been the most complicated and extremly painfull part. I could have used the github's wikis to write documentation and It would have been just fine. But with the efforts I put in there with making the app, _fine just doesn't cut it_. I then dived deaper with [Read the Docs](https://readthedocs.org). It was a lot new, since I had never documented a project, let alone the online documentation part.

I learned about [sphinx]() a document generator which can generate html, pdf, epub etc from reStructured text (I  was first scared about the formatting). I quickly switched to MkDocs for writing the documentation in Md(markdown, also used in writing on this blog) rather than reSt. I then saw my fav markup language fail me for the first time. Md was simply not designed for documenting things, it was ment to be a simple format to write prose. Infact a lot of features we see in markdown are extended versions of the orignal version.

After the blow of Md, I switched again to sphinx and reSt. After that It was a pleasent journey.

I have skipped above the part that involoves Read the Docs. Well it is a service (online) that allows you to store html(and pdf and epub) builds of you documentation online and thus serve it to the users. It is a very amazing service that I appreciated at first sight. You can read its [docs](http://docs.readthedocs.io/en/latest/) to find out more.

## The end and beyond

I have described a lot of my journey here, but it isn't complete and is ongoing. Expect a few more blogs on the same journey.

What I plan for next is :

- adding search feature to the app
- expanding documentation
- writing a python version
- completing holiday homework(completly unrelated but unfortunatly necessary)

See ya.

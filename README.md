# Markdown2Help


`Markdown2Help` is a member of the APLTree library. The library is a collection of classes etc. that aim to support the Dyalog APL programmer. Search GitHub for "apltree" and you will find solutions to many every-day problems Dyalog APL programmers might have to solve.


## Overview 

This application allows you to create a CHM-like help file (including an "Index" and a "Search" tab) by simply creating variables that hold [Markdown](https://daringfireball.net/projects/markdown/) text defining a help page. This makes you completely independent from any 3rd-party tools for creating and maintaining help files. 

It has the benefit of allowing you to edit your help pages while developing or tracing your application.

Note that the now outdated project `APLTreeHelp` offered exactly the same functionality. The difference is that in `APLTreeHelp` help pages were represented by dynamic functions returning a vector of vectors with tags and text. Markdown has significant advantages when it comes to editing a help page. That's why `APLTreeHelp` was replaced by `Markdown2Help`.

This is what `Markdown2Help`'s own help page looks like:

![](Markdown2Help_01.png)

To give it a try just download `Markdown2Help`, unzip it, load it into a Dyalog session and call this function:

```
      #.Markdown2Help.Selfie 1
```

If you want to investigate `Markdown2Help`'s own help pages look into `#.Markdown2Help.HelpHelp` with the Workspace Explorer:

![](Markdown2Help_02.png)

Note how the namespaces reflect nodes and the variables reflect help topics.

This is what a typical help variable looks like:

![](Markdown2Help_03.png)

## How to start 

Since version version 2.2.0 there is a method `CreateStub` available that makes it easy to start a new help system. 

Just call it and provide a proper name as the right argument. If it's not supposed to live in `#` you can specify the name of the namespace it shall be created in as the left argument.

It will then create a couple of pages and a node and finally display it.

## Requirements 

`Markdown2Help` needs at least version 14.0.
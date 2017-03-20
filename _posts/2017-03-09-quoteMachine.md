---
layout: post
title: Build A Random Quote Machine
category: FreeCodeCamp
tags: fcc, js, zipline, quotes
date: 2017-03-09
---

>Do you ever feel like pushing a button to find hope, gain inspiration, or direction in life. Today is your lucky day we're discussing building a quote machine.

## Current Mission
The random quote machine project is from fcc, Free Code Camp, intermediate front end development projects. There are two user stories. First, user can click a button to show a new random quote. Second, user can press a button to tweet out a quote. Additional details about the project can be found on [fcc](https://www.freecodecamp.com/challenges/build-a-random-quote-machine) website.
----
  
### Where should I get quotes?
There are two options for quotes, create and find your own quotes or use an api. Two beginner friendly quote apis I found were [quotesondesign](https://quotesondesign.com/ and [forismatic](http://forismatic.com/en/)
You can search google or ask in the fcc chatroom for more quote api choices. I chose the [forismatic](http://forismatic.com/en/api/) api because the documentation was easy to understand.

### How do I make calls to an API?
This is the most asked question in fcc chatrooms about this particular project. You can use ajax to make http request to retrieve data from a server. I suggest using jquery to make [ajax](http://api.jquery.com/jquery.ajax/) calls to the API. If you prefer vanilla javascript I suggest MDN, Mozilla Developer Network, article ["Getting Started"](https://developer.mozilla.org/en-US/docs/AJAX/Getting_Started). Also, [The Net Ninja](https://www.youtube.com/watch?v=h0ZUpPiV1ac&index=2&list=PL4cUxeGkcC9jAhrjtZ9U93UMIhnCc44MH) youtube video is an easy to understand video on how to use AJAX and vanilla javascript.
    
### Issues
- My biggest issue with this application was making my container div expand the length of the screen. The content height was 350px. So my application on a large screen size had extra white space. To correct this I needed to set the html and body height property to 100% in my css.
  <code>
      html, body {
          height: 100%;
      }
 </code>
Now I had a background that would span the height of the viewport. 
- The next minor issue was dealing with smaller screen sizes. Your layout will break on smaller screen sizes. i.e If your content is scrollable on a smaller device height: 100% only covers the viewport. So anything below the initial viewport the layout is broken. Therefore add a min-height to correct this issue.
 For more information read: 
     [Height: 100%](http://webdesign.about.com/od/csstutorials/f/set-css-height-100-percent.htm)
 
 Implementation:
 
 
#### Optional Reading Material 
##### Writing Ajax using Promises

Another article explaining [height](http://www.mattboldt.com/css-100-percent-height/) property in css.
 
Have A Good Day!!

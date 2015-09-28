---
title: Build A Random Quote Machine
category: FreeCodeCamp
tags: fcc, js, zipline, quotes
---

Build A Random Quote Machine
==========

Zipline: Show the Local Weather 
 
Problem Explanation: 
    There is one user story, click a button to show a new random quote. Also, one bonus story, press a button to tweet out a quote. 
  
Question: Which weather API should I use?
Hint: Forismatic.com
    You can search google or ask in the zipline chatroom for quote api choices. I chose the foriismatic api given as an example in the zipline explanation.
      http://forismatic.com/en/api/ 

Question: How do I make calls to an API?
Hint: This is absolutely the most asked question in chatrooms about this particular project. I suggest using ajax to make a call to the API.
    
Issues:
  My biggest issue with this application was making my container div expand the length of the screen. The content was only roughly 350px. So my application on a large screen size was white space. To correct this I needed to set the html and body height property to 100% in my css.
  <code>
      html, body {
          height: 100%;
      }
 </code>
 Now I had a background that would span the height of the viewport. The next minor issue was dealing with smaller screen sizes. Your layout will break on smaller screen sizes. i.e If your content is scrollable on a smaller device height: 100% only covers the viewport. So anything below the initial viewport the layout is broken. Therefore add a min-height to correct this issue.
 For more information read: 
     [Height: 100%](http://webdesign.about.com/od/csstutorials/f/set-css-height-100-percent.htm)
 
 Implementation:
 
 
 Optional Reading Material For Writing Ajax using Promises
   Another article explaining [height](http://www.mattboldt.com/css-100-percent-height/) property in css.
 
 Have A Good Day!!

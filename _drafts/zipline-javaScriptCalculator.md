---
title: Build a JavaScript Calculator
category: FreeCodeCamp
tags: fcc, js, zipline, calculator
---

Build a JavaScript Calculator
==========

Zipline: Build a JavaScript Calculator
 
Problem Explanation: 
Another zipline from the Basic Front End Development Projects. There are three user stories:
1. User Story: As a user, I can add, subtract, multiply and divide two numbers.
2. Bonus User Story: I can clear the input field with a clear button.
3. Bonus User Story: I can keep chaining mathematical operations together until I hit the clear button, and the calculator will tell me the correct output.
  


Question: How do i use event delegation?
Answer: In chat on FreeCodeCamp(FCC) a user posted a question in chat about buttons for a javascript calculator. Another camper @SaintPeter suggested that the camper user event delegation to attach event listener to their buttons. After reading this I did a little research and found the following articles on event delegation: (Event Delegation)[http://learn.jquery.com/events/event-delegation/], (How Java]Script Event Delegation Works)[How JavaScript Event Delegation Works] The implementation was straight forward in Jquery. I targeted my calculator wrapper to use .on() method from jquery. 
<code>
    $('.calc-wrapper').on("click", "button", fancyCallBack);
<code>

Question: How do I approach the problem?
Answer: I don't really know a good solution to answer this question. I was vaguely aware of parsing and lexers before I started the problem. I quickly looked at graphs/images of each. Then I tried just brute-forcing my way to a solution for hours. Next, due to the complexity of the problem I started writing test for my functions. I was still having issues with some of my logic. Then I decided to take a longer look at (lexical analysis)[https://en.wikipedia.org/wiki/Lexical_analysis] and (parsing)[https://en.wikipedia.org/wiki/Lexical_analysis]. 

Issues:
 
 
 
 
Implementation:

Mandatory Reading Material
How to build a (calculator)[http://ruslanspivak.com/lsbasi-part1/].

Optional Reading Material:
More resources about compilers (Kaleidoscope)[http://llvm.org/docs/tutorial/LangImpl1.html] tutorial. I read some of the material just to get a basic idea of how to think about the topic.
 
 Have A Good Day!!

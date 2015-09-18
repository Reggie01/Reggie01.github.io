---
title: Build A Pomodoro Clock
category: FreeCodeCamp
tags: fcc, js, zipline, pomodoro clock
---

Build A Pomodoro Clock
==========

Zipline: Build a Pomodoro Clock
 
Problem Explanation: 
    
  
Question: 
Hint: 
    
 Question: 
 Hint: 
      
Question: 
Hint: 
      
Question: 
Hint: 
    
Question: Where can I get free sound effects to play with my pomodoro clock?
Hint: [Freesfx](http://www.freesfx.co.uk/soundeffects/all_bells/) offers free sounds that you can use with your project. You will need to sign up with their website to download sounds. Also, attribution is required so make sure to read their license terms.
    
Question: How do I get audio to work with this project?
Hint: You can read about HTML5 audio and video at [MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML5_audio_and_video); Read the sub-heading <em>Controlling media playback</em> for example.

Place this code in your html file.
<code>
    <audio src="name_of_your_file.mp3" preload="auto" ></audio>
</code>

Place code in your javascript where you change from session to break and vice versa.
<code>
    var audio =  document.getElementByTagName("audio")[0];
    audio.play();    
</code>

This is one way to get audio to play.

Question: How do i stop highlighting of a div element when double-clicking on it?
Answer: I had this issue when clicking on span tags. I read this stack overflow [article](http://stackoverflow.com/questions/7018324/how-do-i-stop-highlighting-of-a-div-element-when-double-clicking-on) to fix the issue. 


Question: Why does my canvas image look so fuzzy/blurry? How can I make it look crisp? Help me?
Answer: This problem showed up when I started testing my clock on mobile. The circle was not fully drawn to the canvas. There appeared to be no issues on my desktop. I was using Chrome and toggled device mode to mobile. The device I chose was Google Nexus 7. The cirlce drawn on the canvas was not sharp. My cell phone showed a fuzzier  canvas image.
So I put my Google fingers to use and found an article on [stack overflow](http://stackoverflow.com/questions/15661339/how-do-i-fix-blurry-text-in-my-html5-canvas). Next, 

Question: My font is not displaying properly on my canvas. How I can fix the font?
Answer: The issue is that your custom fonts are not loaded before you draw to the canvas. The browser then falls back on default font which is 10px sans-serif. I chose a standard font to fix this issue. This stack overflow article discusses possible workarounds for this [issue](http://stackoverflow.com/questions/2756575/drawing-text-to-canvas-with-font-face-does-not-work-at-the-first-time).  

Question: My pomodoro clock does not look that great on moblie devices. Can you fix it?
Answer: There is no quick solution for this issue. You can use Chrome developer tools to debug a lot of issues. Open your chrome browser, go to your project site, click F12, look for an icon of a mobile phone and click to toggle device mode. There are a list of devices in the upper left hand corner that the browser will emulate. After that just play around with the styles for your elements. Also, media queries are your friends. You can read about them in [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries). Have fun : p

Question: I set my canvas to a fixed width and height. Now that I view the image on mobile it is way to big. Help me maybe?
Answer: http://htmlcheats.com/html/resize-the-html5-canvas-dyamically/

Question: How to calculate animation amount to fill circle?
Answer: Implement a velocity formula. This is an article discussing [velocity](http://www.physicsclassroom.com/class/1DKin/Lesson-1/Speed-and-Velocity) formula if you need to brush up on the algorithm. Not hard to implement.
Issues:
 
 
 
 
Implementation:
 
Optional Reading Material:

 
 Have A Good Day!!

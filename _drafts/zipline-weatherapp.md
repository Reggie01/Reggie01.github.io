---
title: Build A Weather App
category: FreeCodeCamp
tags: fcc, js, zipline, pomodoro clock
---

Build A Weather App
==========

Zipline: Show the Local Weather 
 
Problem Explanation: 
    There is one user story, show the weather in user current location. Also, three bonus stories which are show icon depending on temp, change background image based on temp and button to toggle Fahrenheit and Celsius. 
  
Question: Which weather API should I use?
Hint: Choose a Weather API
    You can search google or ask in the zipline chatroom for weather api choices. I did both. The choices offered in chat were in no particular order
      - http://simpleweatherjs.com/ - Tons of demos
      - https://developer.yahoo.com/weather/
      - http://forecast.io/
      - http://openweathermap.org/ 
    
 Question: How do I find the user location?    
 Hint: Chose a API for GEO location
      - http://www.geonames.org/
      - https://ipinfo.io/developers
      
 Question: How do I use the location from the user location API with the weather API?
 Hint: You can use jquery. Some people suggest nesting callbacks. I used the jquery promises methods. The method you will need to use is deferred.then().
    Two resources I used: 
      - http://api.jquery.com/deferred.then/  Pay close attenion to the last example.
      - https://medium.com/coding-design/writing-better-ajax-8ee4a7fb95f read the whole article. The section under the sub-heading Dependence of AJAX requests is important.
      
  Question: Where did you find stock images?
  Hint: google. There are a few sites offering free stock images. I would post a question in chat to see what responses you get. I used [stocksnap.io](https://stocksnap.io/) for images. 
    
  Question: Where can I store my images if I use free version of codepen?
  Hint: The two suggestions I see given the most are github and [imgur](http://imgur.com/).
  
  Question: How do I find the algorithims for unit conversions?
  Hint: [Unit](https://www.unitjuggler.com/index.html) conversion algorithims for temperature and speed. Look for the speed converter and temperature converter links near the bottom of the site. 
    
  Question: Where can I get weather icons?
  Hint: Probably best answered by google or chat room. I used [weather icons](http://erikflowers.github.io/weather-icons/) from a google search. Remeber to include the wind-icon css to include wind icons in your project. There are mappings to popular weather [APIs](https://erikflowers.github.io/weather-icons/api-list.html) .
    
  Question: I'm refactoring my event listeners. Is there a way to pass a callback with parameters to my event listeners?
  Hint: Yes, I had a very similiar issue while refactoring my code. I wanted to use a single callback that would update the dom according to the parameters I chose. Initially, I was writing code like
  <code>
      /* 
      function(e) {
          e.currentTarget.className.indexOf( "something" );
          // do some update to dom if correct event listener
      }
  </code>
  which seemed tedious because I knew exactly what I wanted the code to do. So I used my google-fu and found this article [Javascript event handler with parameters](http://stackoverflow.com/questions/10000083/javascript-event-handler-with-parameters). TL;DR You have to pass a function that uses closure to the event listener. For example, 
  <code>
      function add(number) {
          return function ( e ) {
              updateDomElement(number);  // Will retain 
          }
      }
      $( ".milesToRun" ).click( add(3) );
  </code>
 Issues:
 I tried to over-engineer this problem without first completing the project first. Therefore I found myself removing time display. I started reading about implementation ideas for dealing with locale time. This is not in the user stories or the bonus user stories. So I am placing the locale time feature on the back burner. Another issue I ran into was using weather icons. The wind icons for degrees and cardinal direction were not present in the css file. Hopefully it will get fixed soon. Another issue I had was latitude and longitude not finding the correct location on my phone. I will need to google and explore this issue further. 
 
 Implementation:
 The biggest implementation diffrences I seen between my project and others is that I choose to use hash maps in some situations instead of large if/switch statements.
 i.e. If statement route
 
 <code>
   if (data["id"] === 300) {
       // do something
   }
   if (data["id"] === "200") {
     // do something
     var weatherCondition = "thunderstorm";
   }
 </code>
 
 Hashmap
 
 <code>
    var weatherCondition = {
        200: {
            "meaning": "thunderstorm with light rain",
            icon: "wi-owm-200",
            "condition": "thunderstorm"
        }
    }
   
    var weatherID = data["list"][0]["weather"][0]["id"]; // assume id = 200;
    var weatherCondition = weatherCondition["id"]["condition"];  
 </code>
 
 I think mine is a little easier to read. Also, you can create other key/value pairs you may need in your object for other functionality in your code. Overall this project was straight forward. It does make you think a little harder about code organization than any previous object. 
 
 Optional Reading Material For Writing Ajax using Promises
   - https://medium.com/coding-design/writing-better-ajax-8ee4a7fb95f
 
 Have A Good Day!!

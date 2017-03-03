Bonfire: Sum all Numbers in a Range

Find the min number. Store in an array.
Find the max number. Store in an array.

Create the Array.
set index 0 of the array to min number
Create var to set length of array = max - min

Create a loop, iterate up to value 
  at arr[idx] set to ++min
  
Run reduce on the new array

Bonfire: Dif Two Arrays
Create 2 new arrays
filter the first array comparing elements with second array
  If array two does not contain element in array one save element
filter the second array comparing elements with 1st array
  If array one does not contain element in array two save element

Concat both elements

Bonfire: Roman Numeral Converter
Parameters should be number
Major Hint: MeDiCaL XaVIer
Create an associate array/ literal object with Basic Combinations values from www.mathisfun.com/roman-numerals.html
then 



function convert(num){
  
  var numArr = "";
  if((num/1000) >= 1){
    var thousands = Math.floor(num/1000);
    num -= thousands * 1000;
    numArr += rmNums[thousands * 1000];
  }
  if((num/100) > 1){
    var hundreds = Math.floor(num/100); 
    num -= hundreds * 100;
    numArr += rmNums[hundreds * 100];
  }
  if((num/10) >= 1){
    var tens = Math.floor(num/10);
    num -= tens * 10;
    numArr += rmNums[tens * 10];
  }
  if(num > 0){
    numArr += rmNums[num];
  }  
 
  return  numArr.toUpperCase();
}





Bonfire: Search and Replace
Check if second argument is uppercase or lowercase
Set third argument case to equal 2nd argument casing
Search string and replace 2nd argument with third argument

Bonfire: Pig Latin
First follow link to pig latin and familarize yourself with the rules of pig latin. Also, look at the examples provided at the link.
Set an array of vowels.
Check the str argument at index 0 to see if it's a vowel. 
if vowel then add "way" to end of str
if not vowel then set variable to all consonants up to index of 1st vowel
then add variable  and "ay" to end of the string.

Future Optionals:
Turn str argument into an array.
Follow above steps.
Time difference in modifying a string vs an array.
LOL motivation after solving slogn... there is no spoon.

Bonfire: DNA Pairing 
Split string into an array.
Create empty dna pair container array
create empty array for holding pairs
Create the dna pairs to compare characters to 
Loop through the array;
  at each index check character
  if character is at idx 0 of pair, push pair to dna container
  
return container
 
Bonfire: Missing letters
Split string and set to array.
set variable allLettersPresent = undefined;
Loop through string
   check if your at end of string if you are at end of string by checking if idx + 1 equals NaN or just set length - 1
     return allLettersPresent
   at each idx convert to charCodeAt +1 compare to idx + 1
    if not equal   
       increment charCodeAt idx, add 1, convert to CharCode, return

Edge Cases maybe???
is a word or a sentence passed in. if a sentence I would remove spaces and then proceed with code above
check for empty string, return string undefined if empty and move on
       
Bonfire: Boo who
=== will match value and type
true != "true"
set an array of bools true and false
check if value in indexOf array

Additional notes
As soon as I solved realized i could have just run a check against true and false primitive values w/o creating array 

Bonfire: Sorted Union
I can flatten the array. 
Create a uniq array
Loop through the flattened array
  check if uniq array does not have value of flattened array at idx
    push to uniq array
return uniq array

Bonfire: Convert HTML Entites
Map html entites to replacement value
For example {"&": "&amp;",
                    "<": "&lt;",
                    ">": "&gt;",
                    '"': "&quot;",
                    "'": "&apos"}
Create regex expressions to check for in string and replace.
Hint: Start small and try changing casing of words

Bonfire: Spinal Tap Cases
Create regex groups to replace string.

After thoughts: I found this problem to be very difficult. I was not able to pass the test case dealing with camel casing using regex. After trying unsuccessfully for a while I looked at someone's regex to handle camelcase using regex. I could have created an array of capital letters. Looped through the orginal string. Found index of capital letters. created a new str inserting a "-" before the capital letters. Really should have just found a brute force way. A lot of time spent paralyzed staring at the problem.

Bonfire: Sum All Odd Fibonacci Numbers
Another tough problem. First you need to find Fibonacci number. If you don't remember or know how to then you have to follow link to wikipedia with a discussion on Fibonacci number. This probem was not intuitive for me. I wish they had an exercise where we found Fibonacci number first. Then this question would be a nice follow-up. Oh well I digress. I ended up looking up the solution for Fibonacci problem. I was having trouble converting the formula. I tried googling for someone asking just the Fibonacci portion could'nt find anyone. 
My first couple attempts I was finding Fibonacci number up to the number that was passed. So I was using the argument as an ending index in my for loop. Of course this failed. My number was a lot bigger than the number expected in the failed test. Eventually I realized they to add fibonacci numbers up to the argument. Then I just iterated a loop finding Fibonacci numbers up to the argument.  Ran a check to see if the if fib number was less than the number passed. If so continue the loop. If not break out of the loop.

function sumFibs(num) {
  var a = 0, 
       b = 1,
       f = 1,
       fibArr = [0, 1];
  
  for (var i = 2; i <= num; i++){
       
    f = a + b;
    if(f > num){
      break;
    }
    fibArr.push(f);
    a = b;
    b = f;
  }
  console.log(fibArr);
  return fibArr.filter(function(element){ 
                        if(element%2 !== 0) { 
                           return element; 
                        }
                       })
               .reduce(function(a,b){ 
                 return a+b; 
               });
}

This was my first sucessful attempt at the problem. Very wordy so I cleaned the code up.

function sumFibs(num) {
  var minusTwo = 0, 
      minusOne = 1,
      fib = 1,
      sum = f;
  for (var i = 2; i <= num; i++){
       
    fib = minusTwo + minusOne;
    if(f > num){  
      break;
    }
    if(f%2 !== 0){
      sum += fib;
    }
    
    minusTwo = minusOne;
    minusOne = fib;
  }
 return sum;
}

Bonfire: Sum all Primes
function sumPrimes(number) {
  Set sum 
  Create isPrime function
    Check if number is Prime function parameter 
      IF number is less than 2 THEN 
        return false
      IF number is 2 Then
        return true
   
      FOR index = 2 to argument, 
      if Number mod current index is 0
        Return false
     else:
      false
    If n
  Create a variable sum to hold values. 
  Outer Loop: count up to argument
 
} 
First problem I actually used composition on by creating a smaller function first. Previously I had used only JS built-in methods.  

Bonfire: Smallest Common Multiple 
The Bonfire asks you to find the smallest common multiple from a range of numbers. As usual a link is provided for more background information. 

First step is to list all the numbers in the range. 
iterate using a for loop 
function smallestCommons(arr) {
  SET scm equal to 0;
  SET index equal to highest number in array
  SET Length equal to Infinity
  FOR index; INCREMENT by index
    SET isScm equal to true
    FOR index2 = lowest number in array 
      IF index mod index2 not equal 0 THEN set scm equal to false break
      END IF
    END FOR
    IF isScm equal to true THEN set scm equal to index, break
    END IF
  END FOR

  RETURN scm
}
It works but it's really slow

Bonfire: Finders Keepers
function find(arr, func){ 
  DECLARE firstElementDivisibleByTwo
  SET index to zero
  SET numbers equal to array of numbers
  SET len to array length
  FOR index less than len
    IF numbers @ current index equal 0 THEN
      CONTINUE;
    IF numbers @ current index mod 2 equals 0  || IF func returns true THEN 
      SET firstElementDivisibleByTwo to numbers @ current index 
      RETURN true
    END If
  ENDFOR
  RETURN firstElementDivisibleByTwo;
}

I solved the problem using Array.some() to loop through the array. The psuedo code is a way to reason about the code but not the same as the implementation.

Bonfire: Drop it
function drop(arr, func){
  
  SET newArray equal to first argument converted over to an array 
  FOR arr at index 0 to array length
    IF func passed argument arr @ index THEN
      RETURN arr;
    ELSE
      remove first element from newArray
    END IF
  ENDFOR
  
  RETURN newArray
}

Bonfire: Steamroller
Flatten a nested array.
Iterate over the array, test if element isArray yes then concat with array, no then push value to new value

function steamroller(arr){

  SET newArray equal to empty array
  FOR arr to arr length
    IF element in array equal array Then
      LOOP through each element in array and push to new array
    ELSE
      push to element to newArray
    END IF
  ENDFOR
  
  RETURN newArray

}

first close attempt 
function steamRoller(arr){
  var idx = 0;
  var len = arr.length;
  var temp = [];
  var newArray = [];
  
  for(idx; idx<len; idx++) {
    console.log("idx: " + idx);
    temp = arr[idx];
    while(Array.isArray(temp)){
      temp = temp[0];
      
    } 
 
    newArray.push(temp);
    temp = [];
         
  }
  return newArray;
}

second attempt
function steamroller(arr) {
  // I'm a steamroller, baby
  return arr.join()
            .split(",")
            .filter(function(element){ return element !== "" ; })
            .map(function(element){ 
              if(!isNaN(element)){
                 return parseInt(element, 10);
              } else {
                 return element;
              }
            });
}
Sigh the cheater's attempt. I just gamed the solution code. Took me awhile to do it. The reason this code is bad is that it does'nt account for objects. Objects turned to strings with this code is [object Object]. Cheater's never win but they can pass test. I was having a hard time dealing with deeply nested arrays such as [3, [[4]]]
I stumbled upon turning array elements to strings flattens them by accident while trying to solve this problem

third attempt
function steamroller(arr) {
  // I'm a steamroller, baby
  var newArray = arr.slice(0);

  function isElementArray(element){
    if(Array.isArray(element)){
      return true;
    } else {
      return false;
    }
  }
  
  while(newArray.some(isElementArray)){    
    newArray = newArray.reduce(function(a,b){
      return a.concat(b);
    },[]);
  }
  
  return newArray;
}

Finally, I ended up combining the previous lesson Array.some function with Array.isArray... hmm

attempt 4
function steamroller(arr) {
  // I'm a steamroller, baby
  var newArray = arr.slice(0);
 
  while(newArray.some(Array.isArray)){    
    newArray = newArray.reduce(function(a,b){
      return a.concat(b);
    },[]);
  }
  
  return newArray;
}
In the middle of writing the previous sentence I realized Array.isArray and isElementArray is redundant. So the above code is better than attempt 2 because it's not hard-coded to the solution. Solution two was written because I knew the test case arrays only contained numbers and strings. Now if the arrays can contain objects and I will keep the object intact with converting it to a string aka "[object Object]". The world is now a better place. 
Why did I chose to follow the reduce path?
In MDN documentation there is a demonstration of flattening arrays using returning Array.concat inside of a reduce function. Look at the Exampes section sub-heading (Flatten an array of arrays)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce]. 
The syntax for reduce function is arr.reduce(callback[, initialValue]). So I passed reduce a empty array which concats with each element in newArray. 
So where is the magic?
Aha, the magic is in the (the documentation)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat] of couse. : )  Read the description sub-heading first paragraph. If the element(b) is an array return the elements it contains else return the element itself. Then since I keep checking if there is an array in newArray if so I just concat all the elements in the array. 
Im sure there is another multiple other ways to solve this problem but time to move on.

Bonfire: Binary Agents
Helpful links are really mandatory reads unless you are comfortable with the language. I find myself reading the whole linked page top to bottom. Initially I felt they could be skipped when the algorithims were easier. My opinion has changed drastically. You need to try using the methods provided in the links a few times to get some elementary understanding of how they work. If your skilled JS programmer or coming from another language you may be able to read the link just once or not at all. I find everytime I re-read a link I glean some new insight. The most important part though is the seeds its plants or the possibilites they show of using the function. It takes a little time before you grasp the many ways the method could potentially be used. TLDR if you are wondering why the algorithms are getting harder and you no clue how to start. Also, you have been skipping over all the helpful links and never try to use the methods provided in the helpful links. Then start reading the links in their entirety. In a few days you will start to approach problems differently.
function binaryAgent(str){
  SET newArray equal to argument str converted to an Array.
  SET convertedCharArray equal to empty array
  FOR newArray index 0 to end of array
    SET number equal to element converted to number
    SET newCharCode equal to number converted to char("string in js")
    push newCharCode to convertedCharArray
  ENDFOR
  RETURN convertedCharArray converted to string
}
I will most likely use .map to do conversions on elements.  

First Attempt
function binaryAgents(str){
  return str.split(" ").map(function(element){ return String.fromCharCode(parseInt(element, 2)); }).join("");
}

Wow!! All the documentation reading and struggles from the last bonfire paid off. This bonfire was easier than the last 9 for me. The bonus I could map out the entire problem in my head after a minute or two. 

Bonfire: Everything Be True
This bonfire has two links which I read. The name of the function for this bonfire is every. I felt like this may be a sublte hint to Array.prototype.every() so I also read that page of documentation.

PsuedoCode:
function every(collection, pre){
  FOR each element in the collection
    IF element does not have property pre
      RETURN false;
    END IF
  END FOR
}
I will try to use Array.prototype.every().
First Attempt
function every(collection, pre) {
  collection.every(function(element){ return element.hasOwnProperty(pre); });
}

This algorithm problem was easy for me. Felt like the sublte hint was more than enough to get through the problem. I'm expecting the next problem to be harder to solve.

Bonfire: Arguments Optional
Fortunately are unfortunately the last problem offers no new insight. I have seen a problem like this before so I'm guessing it will be simple to solve.
First read the provided links from beginning to end.
function add() {
  SET newArgs equal to arguments that have been sliced.  
  IF newArgs.length greater than one THEN
    RETURN function that has a single parameter and returns parameter plus initial argument from add
  ELSE
    RETURN newArgs element at zero index plus newArgs element at one index
  END IF
  
}
First Attempt
function add() {
   var newArray = Array.prototype.slice.call(arguments);
   if(arguments.length > 1){
    return newArray[0] + newArray[1];
   } else {
    return function(number) { return number + newArray[0]; };
   }
}
Failed some test cases. Why? Failed to read all the instructions. Ah the most frustrating error. So I need to add some checks to my code for arguments being numbers. I initially tried using isNaN but got back false when argument is array. My quick read of the (isNaN)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN] suggests trying typeof to see if value is Not-A-Number. For the curious. The issuse with isNaN is explained under the sub-heading Confusing special-case behavior. Therefore my array was being turned into zero after being coerced into a number.
  new Number([]); // type into console. you get back 0. If pass 0 to isNaN you get back false.

So my second attempt 
function add() {
  var newArray = Array.prototype.slice.call(arguments);
   
  if(arguments.length > 1){
    return (typeof newArray[0] === "number" && typeof newArray[1] === "number") ? newArray[0] + newArray[1] :undefined;
  } else {
    return isNaN(newArray[0])? undefined: function(number) { return typeof number === "number" ? number + newArray[0] : undefined;      };
  }
}
Just added checks for types. My return results are in a ternary operator. condition?true:false Link to read about (ternary operator) [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator]

Bonfire: Make a Person
create six functions that will create a person.
I over engineered my answer a lot. I initially thought they were looking for variables to be contained in the function constructor and all methods to be placed on the prototype object. I had private variable in my function constructor. The problem was I was returning back my own object containing variables with function references to the six functions we needed to create. This is wrong because it overrides the keyword new functionailty. This causes people objects created using person constructor function to not equal instance of Person. The function constructor behind the scences creates and returns it's own object. Also, another test I failed was concerning the object.keys() count on my new person object. Methods being attached to the prototype object are not owned by the instantiated person object. 
My solution was to add the function directly on the object. Hide my variables first and last name using the keyword var. Define all functions needed and invoke the fullName function with the parameter firstAndLast name. Test passed yay!!

Bonfire: Map the Debris
The bonfire starts with a description of the problem and provides two helpful links. I will start by following both links:
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/pow 
2. https://en.wikipedia.org/wiki/Orbital_period
function orbitalPeriod(arr) {
  SET GM
  SET earthRadius
  SET pi 
  SET orbitalPeriodsArray
  SET len to equal arr length
  SET idx to equal zero
  calculate Kepler's Third Law and push to orbitalPeriodsArray
  FOR each object in arr
    SET newObject
    newObject property name equal object property name 
    COMMENT Kepler's Third Law
    newObject property orbitalPeriod equal to 2 multiplied by pi multiplied by ((arr property avgAlt plus earthRadius)^3/ GM)^0.5 then round number
    push newObject to orbitalPeriodsArray
  RETURN orbitalPeriodsArray
  
}

I still need to improve my pseudocode. Post-Mortem the problem was not to complicated but I did initially make two errors. First error was not accounting for multiple arrays. Second, error was small syntax error of multiplying avgAlt by earthRadius instead of adding. If I redo the problem I would use forEach on collection instead of for loop. 

Bonfire: Pairwise
 Solve the problem in 2 steps. First solve for array element plus any other element equals target  argument. 
 function pairwise(arr, arg) {
   SET pairArray equal empty array;
   FOR each element in array
     FOR starting at current inner element index plus one 
       IF inner index greater than outer index
         IF element + element equals target argument THEN
           IF pairArray index of inner index is -1 && pairArray index of outer index is -1        
             push index for both elements to pairArray
         END IF
       END IF
     END FOR
   END FOR
   RETURN sum of pairArray elements;
 }
 Initially failed test case because I pushed indices to pairArray before checking for their existence. Post-mortem I'm having mixed feelings about psuedocode. I rarely solve the problem on my initial attempt using psuedo code. Normally I almost solve the problem. Try implementing the pseudo code and then find out I forgot something. Then I fix the issue and end up changing the psuedo code to sorta match my implementation. I do like the psuedo code because it helps me think about the problem faster and not the code "syntax". 
 

 
 Zipline: Build a Random Quote Machine
 Problem Explanation:
   The zipline starts with the rules to follow while creating your project. A summary of the three rules is reverse engineer the project without looking at the code using any libraries or APIs you like. Next , are the user stories. The first user story is mandatory, display a quote when user clicks a button.
   The second optional user story is create a button for a user to tweet out a quote.
   The first user story can be implemented by creating your own quotes or using an existing api. First, I built a prototype to make sure I understood the problem.  
 Hint: 1
   Build a prototype testing button functionality.
   
  Spoiler alert!
    Solution ahead!
    
  Solution Code: 
    var strings = ["a", "b", "c", "d"];
  
    var count = 0; 
  
    $("#quote").click(function() {
      if(count < strings.length){
        $("#new-quote").html(strings[count++]);
      } else {
        count = 0;
        $("#new-quote").html(strings[count++]);
      }
    
    });
    
  Code Explanation: 
    First, I created a new codepen and included jquery. You can do this by clicking settings tab, navigating to javascript, clicking on Quick-add and selecting jquery. I created an array of strings and saved to a variable strings. Next I assigned 0 to count variable. Then I created a conditonal to see if count was less than the array length. If true I added strings array at index equal to count to my div new-quote. Else if the conditional was false I set the count back to zero. Then added the string at index zero in strings array to the div new-quote.
    
  Next, I implemented the (API)[http://forismatic.com/en/api/ ] given in step eight of the zipline instructions. I used ajax method from Jquery to call the API. The API will not return data successfully using dataType json. An error response is given 
  <code>XMLHttpRequest cannot load http://api.forismatic.com/api/1.0/?method=getQuote&format=json&lang=en. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://s.codepen.io' is therefore not allowed access.</code>
  The issue is codepen.io and api.forismatic.com are different domains. Therefore, my ajax response from api.forismatic.com are checked for Access-Control-Allow-Origin a CORS(Cross-Origin Resource Sharing) header by the browser. The browser does not find my domain as an allowed domain and a XMLHttpRequest error is thrown. For more details read the following wiki link about (Same-origin policy)[https://en.wikipedia.org/wiki/Same-origin_policy], this link from stackoverflow on (access-control-allow-origin) [http://stackoverflow.com/questions/10636611/how-does-access-control-allow-origin-header-workdetails] and tutorial on (CORS)[http://www.html5rocks.com/en/tutorials/cors/#toc-adding-cors-support-to-the-server]. Luckily, forsmatic API does accept jsonp request as stated on there documentation (page)[http://forismatic.com/en/api/]. You can look at my codepen to see the ajax request I created (here)[http://codepen.io/Reggie01/pen/gaYaax]. 
  Next, goal was to do the bonus user story. Let a user, press a button to tweet out a quote. 
    https://twittercommunity.com/t/insert-dynamic-content-into-data-text-attribute/19598/4
    
    http://marcus-christie.blogspot.com/2011/07/how-to-dynamically-change-tweet-buttons.html
    
    How to make tweet buttons
    https://dev.twitter.com/web/tweet-button/parameters

 API Guidelines
 This will discuss the methods you will use when dealing with APIs http://www.w3schools.com/tags/ref_httpmethods.asp. The most important one for now is GET method.
  This is a general video about REST APIs - https://www.youtube.com/watch?v=7YcW25PHnAA
  These will give you a high level overview of what your trying to accomplish. 
      
 
Zipline: Build a Tic Tac Toe Game

Resources: 
  http://neverstopbuilding.com/minimax

 
Waypoint: Scope Your Variables
How do I feel about Waypoints? 
Waypoints seem to give a lot FCC beginner coders feelings of inadquecy about programming. My two cent is that people should read a couple articles on how to learn. One thing that sticks out to me is that reading is not learning. Some articles I have read suggest a tri-fecta reading, applying and teaching. Your comprehension of a subject from reading alone is say 33%. Then after applying 66%. Lastly teaching 90%+. TLDR Waypoints are equivalent of reading so yes you will not understand the material in any depth from just doing the waypoint. You will understand more after doing the algorithims. I can not write about the ziplines and basejumps because I haven't started them yet.
Scopes 
Lexical Scoping 


can you spot the error??

function largestOfFour(arr) {
  // You can do this!
  var nArr=[]
  for(var i = 0; i<arr.length; i++){
    nArr.push(arr[i].sort().slice(3).join(','))
   
  }
  return nArr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
["5", "27", "39", "857"]

How to time functions?
---------------------------
http://stackoverflow.com/questions/313893/how-to-measure-time-taken-by-a-function-to-execute
var a = performance.now();
alert('do something...');
var b = performance.now();
alert('It took ' + (b - a) + ' ms.');

Psuedocode Standard
http://users.csc.calpoly.edu/~jdalbey/SWE/pdl_std.html

Greenheart
@kimsimmons Watch out, this might be a long one! 
1. You need good communication (voice chat works the best)
2. When you start working together; talk about how your workflow should look like so that both you and your partner can benefit from the time spent coding.
3. Don't give too much away right away if you know the answer (and ask your partner to do the same for you) --> instead, let your partner think about the problem and use questions to guide him/her right.
Questions help the other person learn easier, because then he/she really gets to think about what you're asking.

Hope that helped! :)
I might as well add something like this on freeCodeCamp's wiki under pair programming, because I believe this is something more people will find useful! ^^

Greenheart
Hey everyone! Me and some friends just added some articles about pair programming on FCC to the community wiki. We hope that you find this useful
https://github.com/FreeCodeCamp/freecodecamp/wiki/Why-You-Should-Try-Pair-Programming
https://github.com/FreeCodeCamp/freecodecamp/wiki/Tips-on-How-To-Become-A-Good-Pair-Programmer
Happy coding! :grinning:


Debugging video 
https://www.youtube.com/watch?v=-q1z8BPFItw


Productivity tools 
http://stackoverflow.com/questions/9115134/indent-javascript-code-written-in-on-line-in-notepad-or-else
js beautifier
  Remove unused css
http://addyosmani.com/blog/removing-unused-css/
https://github.com/giakki/uncss
  Compress and gzip css on web server
https://varvy.com/pagespeed/enable-compression.html
  Browser caching
https://varvy.com/pagespeed/leverage-browser-caching.html
  Compress images
https://tinyjpg.com/

Ajax Tutorial Material
https://www.youtube.com/watch?v=fEYx8dQr_cQ
https://www.youtube.com/watch?v=7YcW25PHnAA
http://www.w3schools.com/tags/ref_httpmethods.asp
https://www.youtube.com/watch?v=obaSQBBWZLk

How-to-Create IE-Only Stylesheet
https://css-tricks.com/how-to-create-an-ie-only-stylesheet/

Inspiration/Programmer Map
http://www.vikingcodeschool.com/posts/why-learning-to-code-is-so-damn-hard


Module Pattern
http://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope/

Regex Resources
http://regexcrossword.com/challenges/tutorial/puzzles/7
https://github.com/freecodecamp/freecodecamp/wiki/js-regex

Stats
http://ashleynolan.co.uk/blog/frontend-tooling-survey-2015-results

Zipline: Build a Personal Portfolio
http://www.w3schools.com/cssref/pr_background-attachment.asp

HTML5 Safari
https://developer.apple.com/library/safari/documentation/AudioVideo/Conceptual/Using_HTML5_Audio_Video/PlayingandSynthesizingSounds/PlayingandSynthesizingSounds.html

if('webkitAudioContext' in window) {
    var context = new webkitAudioContext();
} else {
var context = new AudioContext();};

FreeCodeCamp Icon
https://s3.amazonaws.com/freecodecamp/favicons/favicon-32x32.png

Code Guide by @mdo HTML and CSS
http://mdo.github.io/code-guide/

Web Site for Unit conversions
https://www.unitjuggler.com/convert-speed-from-ms-to-mph.html

How to Debug Javascript in console
http://www.briangrinstead.com/blog/devtools-snippets
https://developer.chrome.com/devtools/docs/authoring-development-workflow#snippets

Help Channels FCC
wiki help channels  -- cmd

Javascript Prototypes
http://blog.pluralsight.com/understanding-javascript-prototypes

Jquery to Angular
http://stackoverflow.com/questions/14994391/thinking-in-angularjs-if-i-have-a-jquery-background

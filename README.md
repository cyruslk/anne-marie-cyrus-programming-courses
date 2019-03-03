# anne-marie-cyrus-week-1 (2019.01.25)

## Useful links:

1. W3SCHOOLS
   1. https://www.w3schools.com/js/js_string_methods.asp
   2. https://www.w3schools.com/js/js_strings.asp
   3. https://www.w3schools.com/js/js_array_methods.asp
2. This video:
   1. https://www.youtube.com/watch?v=rRgD1yVwIvE
3. Ressources for questions and debugging:
   1. https://stackoverflow.com/

## AS A WARM UP...

1. From a string, return an array of letters. 
2. From an array, return a string.
3. If a number is passed into a function that accepts only strings or arrays, return something like `sorry, wrong parameter`.

------



1. From a string, return the first letter only. If another parameter is passed, return `undefined`. 

2. From a string, return the last letter only. If another parameter is passed, return `undefined`. 

3. From a string, return only the letter located at position `2`. If the word length is too short for this program, return the following log: `Please enter a longer word.`

4. From a string, return only letters located at position `2` and at position `5`.  If the word length is too short for this program, return the following log: `Please enter a longer word.`

5. From a string, return the same string with first and last letters removed. If, for an example, I'm passing to the program the following string: `Hello`, the program should return me `ello`.   If the word length is too short for this program, return the following log: `Please enter a longer word`. 

6. From a string, return the same string with the letter located at position `5` removed.

7. From a string, return only the even letters. If the word is `Hello world`, the returned string should be someting like `Hlowl`. 

8. From a string, return a new version of this string where each letters would be outputted twice. If the word is `Hello world`, the returned string should be something like `HHeelloo  wwoorrlldd`

9. From a string, return its reversed version. If the word if `Hello`, the returned word should be `olleH`.

------

# anne-marie-cyrus-week-2 (2019.02.08)

1. Using the ` map()` method:
   1. recreate: 8
   2. recreate: 9
2. Using the `filter() ` method:
   1. recreate: 6
   2. recreate: 7 
3. Using both `filter()` and `map()` together:
   1. Return the even strings of all the numbers located in this following string: `hell1234o w5678orl90d`. 
4. Using a simple `for()` loop, return the sum of the following array of numbers: `[1, 2, 3, 4, 5, 6];`
5. Same exercise using a `map()` method.
6. Using both `filter()` and `map()` method,  return the sum of the following array of numbers except the numbers located at position `0` and `3`: `[1, 2, 3, 4, 5, 6];`
7. Using both `filter()` and `map()` method,  return the sum of the following array of numbers except the numbers located at position `0` and `3`: `[1, 2, 3, 4, 5, 6];`
8. Using both `filter()` and `map()` method,  return the sum of numbers located in this following string: `hell1234o w5678orl90d`. 
9. Using both `reduce()`,  return the sum of the following array of numbers: `[1, 2, 3, 4, 5, 6]`;
10. Using `map() `and `reduce()`,  return the sum of numbers located in this following string: `hell1234o w5678orl90d`. 

------

# anne-marie-cyrus-week-3 (TBD)

As a warm up:

1. Same result -> only with 3 chained methods.

   ```
   const reversedLetters = letters
   .split('')
   .reverse()
   .map(letter => letter)
   .join('');
   console.log('--Ex.1.2')
   console.log(reversedLetters);
   ```

2. After a quick look [here](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Fonctions/Fonctions_fl%C3%A9ch%C3%A9es), rewrite this function using the `=>` :

   ```
   const fiveRemoved = letters
   .split('')
   .filter(function(letter, index) { if (index !== 5) {return letter}}) // Ask Cyrus how to turn this into arrow function
   .join('');
   
   console.log('--Ex.2.1')
   console.log(fiveRemoved);
   ```

3. Reverse-engeneer this code by commenting it line by line. Can you guess its result for the given `v12v` without running it?

   ```
   function filteringWithMap(string){
      const filteredArray = [];
      string.split("").map((ele, index) => {
      if(ele === "v"){
      return filteredArray.push({ele, index});
      }
      })
      return filteredArray;
    }
   ```

4. Starting from the code you wrote for ex. 4,  rewrite the same logic using a `map()` function. TIP: you need to have a counter to store the changing value.

5. Only with `.map()` return the sum of the numbers located in each element of the array returned by the `filteringWithMap()`.  Try to do all this computation inside this function. 

------

Before going to Node.js: introduction to objects, methods and the `this` keyword. These videos might be useful:

- https://www.youtube.com/watch?v=4uVwGw317QM
- https://www.youtube.com/watch?v=uLmdvseykQM&t=5s

1. Create an object entitled `me` with `name` as a key, your name as the value. Inside this object, create a `method`  named `helloMe`  that, when you call it, logs `Hello, dear {your name}`.  

   Ex: if the name is `Mélo`, it shouls logs `Hello, dear Mélo`

------

SMALL NODE.JS PROJECT! - going closer to 'full stack-projects' we'll do soon!

- Fetching data from external API's.

  - Have a look here: https://github.com/toddmotto/public-apis

  - Have a look here: https://any-api.com/

- Let's see if we can fix your git. Otherwise, you'll use a `c9` workspace.

1. Is npm installed? If so, `npm init` inside a new folder. Inside this folder, install `prompt`, then `axios` or `request-promise`. Find these NPM packages on the internet!
2. Ask the user of the program his nickname. Once this nickname is received, log to the consle : `Hello dear {name}`.  If nothing was entered, prompt again.
3. Fetching data from [this api](http://open-notify.org/Open-Notify-API/ISS-Location-Now/), let the user knows where the ISS space station is located (displaying its GPS lat/long coordinates).
4. Get yourself an API key of this [location/gps service](https://opencagedata.com). Ask the user his location, then use this service to retrieve the user's location lat/long. Display on the terminal: `Hello dear {name}, the ISS is located at {x, y} and you're located at {x,y} `.
5. Using this [JavaScript formula](https://www.movable-type.co.uk/scripts/latlong.html), let the user know where how far he is located from the actual position of the ISS.
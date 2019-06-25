## Coding Challenges

Whilst some interviews may be more of a chat - making sure you are a good culture fit - others will lean more towards technical questions. Some of these technical questions will be take home, while others will be on the spot, 'whiteboarding' ones.

#### Take home questions

One of the key things employers will be looking for, is how you scope out a problem. They will usually intentionally give vague instructions to see how you will come to a conclusion.

**Tips**

- Ask them how long you have to complete the project. If they give you the option of creating your own timeline, don't try to impress by pulling an all-nighter and handing it to them at 9AM the next day. Instead, give a reasonable timeline, with good explanation of why - and stick to it!

- Focus on the most important criteria. These will often be at the top of the list. An example might be spending more time ensuring there are no bugs in the routes and controller, rather than styling it, pixel-perfect

##### Example - SWAPI Rails App

This example is one that was given to Dave A and Scott from last cohort. This is not something to do this afternoon, rather something for you to keep for your own reference, and to practice later.

Additional notes: Both Scott and Dave got this challenge on a Friday, and gave themselves until 9AM on Monday to get it completed.

**Description**
Produce a UI for the Star Wars API built using Ruby on Rails. Live Site

**Goal**
Consume film and character information from SWAPI and display it in a clean, performant user interface.

**Acceptance criteria**

- Home screen contains a list of films pulled from the SWAPI
- List should be searchable
- Films can be favourited, this state should be persisted using local storage
- Favourited films should appear at the top of the list
- A stylised user prompt/alert should show when a film is favourited
- Favourited films can be unfavourited
- Film list items can be clicked to show individual film page
- Film page should show all the information pulled from the SWAPI endpoint for an individual film
- Film page should contain a back to home link
- The list of characters should display a tooltip when a list item is hovered
- The tooltip should show the character's bio pulled from the SWAPI endpoint for people
- Provide public GitHub repo to source code
- Host the finished project on Heroku, Surge or similar
- This test is focused on demonstrating Ruby on Rails, do not sweat the styling too much and feel free to use a framework like Bootstrap or similar
- Bonus points (not required)
- Use the tooltip UI to show additional information pertaining to the film like vehicles, spaceships etc
- Demonstrate creative and performant ways of fetching information from SWAPI
- Provide a documented readme inside the GitHub repo explaining the technology used, the setup process and other relevant information

#### WhiteBoard Challenges

Employers will give whiteboard challenges, to see how your thought process works. Because of this, they are not necessarily looking for the correct answer (although, do try your best to get it right), but more seeing how you breakdown the questions and work through the components.

Today, we will give you the following questions. Your challenge is to attempt these questions using only pen and paper. You can use pre-built functions, but you are not allowed to google what these functions are - because you can't use your computer!

On completion, present it to the person next to you, using non-technical descriptors. When you are the person getting presented to, try to think of good questions that an interviewer may ask, and ask them.

##### Question 1 - Understanding Numbers

What will be the output of the following code snippet? Why?:

`console.log(0.1 + 0.2 === 0.3);`

##### Question 2 - Understanding Loops

What will the following code snippet output?:

```javascript
for (let i = 1; i <= 10; i++) {
  if (i === 2) continue;
  if (i === 6) break;
  console.log(i);
}
```

##### Question 3 - Understanding Timing

What will the following code snippet output? Think about timing and explain why?:

```javascript
for (let i = 1; i <= 5; i++) {
  setTimeout(() => {
    console.log(i);
  }, i * 2000);
}
```

##### Question 4 - Understanding Arrays

What will the following code snippet output and why?:

```javascript
let arr1 = "john".split("");
let arr2 = arr1.reverse();
let arr3 = "jones".split("");
arr2.push(arr3);
console.log("array 1: length=" + arr1.length + " last=" + arr1.slice(-1));
console.log("array 2: length=" + arr2.length + " last=" + arr2.slice(-1));
```

##### Question 5 - Find the Vowels

Write a function that takes a string as argument and returns the number of vowels contained in that string. The vowels are "a", "e", "i", "o", "u"

**Examples**

findVowels('hello')
--> 2

findVowels('why')
--> 0

##### Question 6 - FizzBuzz

Write a function that does the following:

- console logs the numbers from 1 to n, where n is the integer the function takes as its parameter
- logs fizz instead of the number for multiples of 3
- logs buzz instead of the number for multiples of 5
- logs fizzbuzz for numbers that are multiples of both 3 and 5

**Example**

fizzBuzz(5)
-->
// 1
// 2
// fizz
// 4
// buzz

##### Question 7 - Anagram

A word is an anagram of another word if both words have the same letters, in the same quantity, but arranged differently. Write a function that checks if two provided strings are anagrams of each other. Spacing, letter casing and punctuation do not matter.

**Example**

anagram('finder', 'Friend')  
--> true

anagram('hello', 'bye')
--> false

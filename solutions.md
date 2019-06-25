##### Question 1 - Understanding Numbers

It will output false, as `0.1 + 0.2` will approx equal `0.30000000000000004`

##### Question 2 - Understanding Loops

**Output**

```javascript
// 1
// 3
// 4
// 5
```

**Why:**

When i is equal to '2' that iteration is skipped. When i is equal to '6', the whole loop is broken out of, before logging 6

##### Question 3 - Understanding Timing

**Output:**

```javascript
// 1
// 2
// 3
// 4
// 5
```

**Why:**

1 to 5 are logged out, as the loop will break when i > 5. These numbers are printed out 1-by-1 with a 2 second break in between each.

The reason this 2 second break occurs, is due to the 2nd part of our setTimeout function `i * 2000`. If this was just `2000`, what would happen?

##### Question 4 - Understanding Arrays

**Output:**

```javascript
"array 1: length=5 last=j,o,n,e,s";
"array 2: length=5 last=j,o,n,e,s";
```

**Why:**

The `reverse()` method will reverse the actual array as well.

Passing an array to the `push()` method will push the entire array in as one element.

##### Question 5 - Find the Vowels

```javascript
const findVowels = str => {
  let count = 0;
  const vowels = ["a", "e", "i", "o", "u"];
  for (let char of str.toLowerCase()) {
    if (vowels.includes(char)) {
      count++;
    }
  }
  return count;
};

// Obviously there are other solutions as well
```

##### Question 6 - FizzBuzz

```javascript
const fizzBuzz = num => {
  for (let i = 1; i <= num; i++) {
    // check if the number is a multiple of 3 and 5
    if (i % 3 === 0 && i % 5 === 0) {
      console.log("fizzbuzz");
    } // check if the number is a multiple of 3
    else if (i % 3 === 0) {
      console.log("fizz");
    } // check if the number is a multiple of 5
    else if (i % 5 === 0) {
      console.log("buzz");
    } else {
      console.log(i);
    }
  }
};
```

##### Question 7 - Anagram

```javascript
// Solution with code comments!!

// helper function that builds the
// object to store the data
const buildCharObject = str => {
  const charObj = {};
  for (let char of str.replace(/[^\w]/g).toLowerCase()) {
    // if the object has already a key value pair
    // equal to the value being looped over,
    // increase the value by 1, otherwise add
    // the letter being looped over as key and 1 as its value
    charObj[char] = charObj[char] + 1 || 1;
  }
  return charObj;
};

// main function
const anagram = (strA, strB) => {
  // build the object that holds strA data
  const aCharObject = buildCharObject(strA);
  // build the object that holds strB data
  const bCharObject = buildCharObject(strB);

  // compare number of keys in the two objects
  // (anagrams must have the same number of letters)
  if (Object.keys(aCharObject).length !== Object.keys(bCharObject).length) {
    return false;
  }
  // if both objects have the same number of keys
  // we can be sure that at least both strings
  // have the same number of characters
  // Now we can compare the two objects to see if both
  // have the same letters in the same amount
  for (let char in aCharObject) {
    if (aCharObject[char] !== bCharObject[char]) {
      return false;
    }
  }
  // if both the above checks succeed,
  // you have an anagram: return true
  return true;
};
```

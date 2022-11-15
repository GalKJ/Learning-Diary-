# My learning diary 📖

## A reflective process to record what I learn as I learn it.

### FormData

- The FormData interface provides a way to easily construct a set of key/value pairs representing form fields and their values, which can then be easily sent using the fetch() or XMLHttpRequest.send() method. It uses the same format a form would use if the encoding type were set to "multipart/form-data".
- https://developer.mozilla.org/en-US/docs/Web/API/FormData
- Using this Web API make's it very easy to interpolate a user's input into a data field for use as a query parameter for example.  

### Keeping my code dry ☀️

-Today I wrote a function that creates inner HTML that renders on the page. 
`function createInnerHTML (el, keys, values) {
        // Default loading text in case user has to wait for data 
        el.innerHTML = `<p>...loading</p>`;

        el.innerHTML = 
                `<p>${keys[0]}-${values[0]}</p>
                 <p>${keys[10]}-${values[10]}</p>
                 <p>${keys[4]}-${values[4]}</p>
                 <p>${keys[9]}-${values[9]}</p>
                 <p>${keys[15]}-${values[15]}</p>
                 <p>${keys[17]}-${values[17]}</p>`
}` 
-By writing this re-usable function I can avoid repeating myself.

### css refactoring. The adjacent sibilng combinator.

- While researching the best way to refactor the css on a site I maintain I came across a great wealth of css docs.   
- `The adjacent sibling combinator (+) separates two selectors and matches the second element only if it immediately follows the first element, and both are children of the same parent element.` 
- https://developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_combinator

### Template literals 
- I've been using template literals mainly for string interpolation in order to combine strings and expressions.
- Today i discovered Tagged template literals and I'm excited to use them.
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals
- https://wesbos.com/tagged-template-literals

### Exiting Vim 
- Firstly if you are in `insert` mode hit `esc` to exit into `command` mode
- To exit Vim type `:q` and hit enter
- To save your changes type `:w`
- To exit Vim and save your changes type `:wq`
- To exit Vim and lose and unsaved changes type `:q!`

### One liner sleep function 
- `function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}`
- By seperating the new Promise constructor from the rest of the code you make your code simpler to read.
- `console.log('Sleeping...');
new Promise(resolve => setTimeout(resolve, 1500))
  .then(() => {
    console.log('Awake!');
  });`
 - becomes...
 - `console.log('Sleeping...');
sleep(1500)
  .then(() => {
    console.log('Awake!');
  });`
  - 😴

### Vim motions 
- Motions (as in movements) are how you move around in Vim. They are commands that when typed move the cursor around with high speed and precision.
- You can use the w (word) command to jump to the beginning of the next word 
- Use b (back) to jump to the beginning of a word backwards
- Use e (end) to jump to the end of a word
- Use ge to jump to the end of a word backwards

### Arguments & Parameters
- A parameter is a variable in a function definition. It is a placeholder and hence does not have a concrete value. An argument is a value passed during function invocation. In a way, arguments fill in the place the parameters have held for them.

### https://httpstat.us/
- This is a super simple service for generating different HTTP codes.
- It's useful for testing how your own scripts deal with varying responses.
- Just add the status code you want to the URL, like this: httpstat.us/200
- We'll return a response like this:
`HTTP/1.1 {status code} {status description}`
    `Content-Type: text/plain or application/json`
    `Content-Length: {something}`
    `{any custom response headers}`
    
    `{status code} {status description}`
    `{list of any custom response headers we added}`
    
### Make sure your tests can FAIL 😱
- https://kentcdodds.com/blog/make-your-test-fail
- This blog post by Kent C. Dodds expalins why it's important to make sure you can make your tests fail as you expect them to. If your test examples don't have enough characters for example and your function first checks for character.length it will fail over before reaching any later syncronous code such as if the result you're passing it is missing an uppercase character. 
- The video post in this blog is very helpful. ❇️

    
 ### Regex basic character classes
 - \d recognises digits 0 - 9
 - \s recognises whitespace such as \n (new line)
 
 ### Keyup & Keydown 
 - You can alternate the background colour of an input by listening for both events
- `function keydownFunction() {
  document.getElementById("demo").style.backgroundColor = "red";
}`
- `function keyupFunction() {
  document.getElementById("demo").style.backgroundColor = "green";
}`

### Array destructuring 
- `const letters = ['a', 'b', 'c', 'd'];
const [a, b, c] = letters;
[a, b, c];
Result:
['a', 'b', 'c']`
- This feature is called "destructuring". An array has some structure: certain values at certain indexes. We use destructuring syntax to unpack that structure and access the individual pieces. We "de-structure" the array.

###  Array destructuring, default values
- Elements with and without defaults can be mixed. In the example below, d has a default but e doesn't. The matched array has no value for e, so it will get the value undefined.
- `const letters = ['a', 'b', 'c'];
const [a, b, c, d='dee', e] = letters;
[d, e];
Result:
['dee', undefined]`

### Array destructuring, rest parameters
- We can collect any remaining elements using ..., similar to how we used "rest parameters" in function definitions. The ... in the next example collects all of the array elements that weren't matched in the destructuring.
- `const letters = ['a', 'b', 'c'];
const [a, ...others] = letters;
others;
Result:
['b', 'c']`

### Burnout and pacing
- During FAC26 or in fact any intense period of work or learning it's easy to push yourself just a little bit further everyday. This can help you to reach goals you may have thought unattainable but beware! Whilst challenging oneself is necessary be careful not to keep adding on another 30 mins to the end of beginning of your work day because before you know it, there's not more hours in the day!
- Regular breaks during intense periods are not only pleasurable but also integral to a good working brain and one that doesn't suffer from to much stress and tension. Happy brains are powerful brains!

### Tagged template literals
- TTL's give the user the power to manipulate strings and values that are being pulled in from elsewhere. 
- See the example below 
- `function doubleNumbers(strings, ...values) {`
- `let result = '';`
- `for (let i=0; i<strings.length; i++) {`
- `result += strings[i];`
- `if (i < values.length) {`
-   `result += values[i] * 2` 
-  `}`
- `}`
- `return result;`
- `}`
- 
- `doubleNumbers``the numbers ${1} and ${2}``;`

 


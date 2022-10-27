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


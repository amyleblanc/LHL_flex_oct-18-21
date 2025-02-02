# Module 4 Week 8 - Client Side JavaScript & jQuery

[Lecture Slides](https://github.com/letsandeepio/LHL_flex_oct-18-21/blob/main/w8-client-side-javascript-jquery/Client%20Side%20JavaScript%20%26%20jQuery.pdf)

[Notes & Code](https://github.com/letsandeepio/LHL_flex_oct-18-21/tree/main/w8-client-side-javascript-jquery)


👋🏻 Thanks for coming to the lecture. All topics covered are in the attached slides.


## Demo Notes - Using Live Server Extension with VSCodes

Live Server Extension allows us to run our code nodemon style in the browser, it will refresh our code as we make changes.

Install it from here: https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer

## Client Side JS
> Client side JavaScript is JS that runs in the browser. Here, `client` is as opposed to `server`

### What is the DOM?
**D**ocument **O**bject **M**odel

> The DOM is a data representation of HTML (or XML).

By creating an object model of the HTML the browser allows us to interact with our HTML document using JavaScript.

### Browser events
> Events are triggered whenever something happens in the browser, ususally a user action

We can use JavaScript to listen for browser events and run code based on them.

### Client side objects
There are a few objects available to us *only* on the client side.

* `event` — info about a browser event
* `window` — the window containing a DOM document, usually a tab
* `navigator` — info about the user's browser
* `document` — the DOM document for the page

## jQuery
You can read more about jQuery here: https://api.jquery.com/

jQuery lets us use the `$()` function which is super powerful. One of the main uses is to get elements from the DOM using a very similar syntax to CSS selectors.

```javascript
// This will return the element with the id of "special-element"
$("#special-element")
// This will return all elements with a class of "list-items"
$(".list-items")
```

### Event handling
Once we have retrieved an element we add an event listener to it using the `.on()` function.

```javascript
// This will add a click event listener to all elements with the "button" class
$(".button").on("click", (event) => {
  // do something here
})
```

### Creating elements
We can also use the `$()` function to create new HTML elements. One way to do this is to pass the opening tag of an element as an argument to the function. This will create that element for us to then use.

```javascript
// This creates an HTML li element
const $item = $("<li>")
// Then we retrieve an existing element from our document
const $list = $("#my-list")
// Then we add our li element to the bottom of the list element
$list.append($item)
```
# rolePlayingGame
Free Code Camp - Responsive Web Design - Learn basic JavaScript by building a role playing game

## **Step 1** 
JavaScript is a powerful language which allows you to build websites that are interactive.<br>
<i>Note</i>: For all of the projects in this curriculum, you will need to have a basic level knowledge of HTML and CSS. If you are new to HTML and CSS, please go through the <u>Responsive Web Design Certification first</u>.<br>
To get started, create your standard HTML boilerplate with a `DOCTYPE`, `html`, `head`, and `body`, then add a `meta` tag for the `charset`. Add a `title` element and use the text `RPG - Dragon Repeller` for it. Include a `link` tag for your stylesheet to link the `styles.css` file.<br>
Finally, create a `div` element with `id` set to `game` within your `body`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="./styles.css">
    <title>RPG - Dragon Repeller</title>
  </head>
  <body>
    <div id="game">
    </div>
  </body>
</html>
```

## **Step 2** 
Now you can start writing your JavaScript. Begin by creating a `script` element. This element is used to load JavaScript into your HTML file. You should use an opening `<script>` and closing `</script>` tag.

```html
<script></script>
```

## **Step 3** 
One of the most powerful tools is your developer console. Depending on your browser, this might be opened by pressing `F12` or `Ctrl+Shift+I`. On Mac, you can press `Option + ⌘ + C` and select "Console". You can also click the "Console" button above the preview window to see our built-in console.<br>
The developer console will include errors that are produced by your code, but you can also use it to see values of variables in your code, which is helpful for debugging.<br>
Add a `console.log("Hello World");` line between your `script` tags. Then click the "Console" button to open the console. You should see the text `"Hello World"`.<br>
Note how the line ends with a semi-colon. It is common practice in JavaScript to end your code lines with semi-colons.

```js
console.log("Hello World");
```

## **Step 4** 
Before you start writing your project code, you should move it to its own file to keep things organized.<br>
Remove your `console.log("Hello World");` line. Then give your now empty `script` element a `src` attribute set to `./script.js`.

```html
<script src="./script.js"></script>
```

## **Step 5** 
Your view has been switched to your new `script.js` file. Remember that you can use the tabs above to switch between files.<br>
Add your `console.log("Hello World");` line to this file, and see it appear in your console.

```js
console.log("Hello World");
```

## **Step 6** 
Remove your `console.log("Hello World");` line to begin writing your project code.<br>
In JavaScript, a <i>variable</i> is used to hold a value. To use a variable, you must first <i>declare</i> it. For example, to declare a variable called `camperbot`, you would write:<br>
`let camperbot;`<br
The let keyword tells JavaScript you are declaring a variable. Declare a variable called xp.

```js
let xp;
```

## **Step 7** 
Variables can be <i>assigned</i> a value. When you do this while you declare it, this is called <i>initialization</i>. For example:<br>
`let age = 32;`<br>
This would initialize the `age` variable with a value of `32`, a number.<br>
Initialize your `xp` variable to have a value of `0`, a number.

```js
let xp = 0;
```

## **Step 8** 
Initialize another variable called `health` with a value of `100`, and a variable called `gold` with a value of `50`.

```js
let health = 100;
let gold = 50;
```

## **Step 9** 
Create another variable called `currentWeapon` and set it to `0`.<br>
When a variable name has multiple words, the convention in JavaScript is to use what's called <i>camelCase</i>. The first word is lowercase, and the first letter of every following word is uppercase.<br>
`let thisIsCamelCase;`

```js
let currentWeapon = 0;
```

## **Step 10** 
Declare a variable called `fighting` but do not initialize it with a value. Remember to end your line with a semi-colon.

```js
let fighting;
```

## **Step 11** 
Declare two more variables named `monsterHealth` and `inventory`, but do not initialize them.

```js
let monsterHealth;
let inventory;
```

## **Step 12** 
The variables you have assigned have all had values that are numbers. JavaScript has multiple different data types. The next one you will use is the <i>string</i>. Strings are used to store things like words or text. Strings are surrounded with double quotes, single quotes, or backticks. Here is an example of declaring a variable with a string:<br>
`let developer = "Naomi";`<br>
Assign the `inventory` variable to have the value of `stick`.

```js
let inventory ="stick";
```

## **Step 13** 
The player's inventory in your game will be able to hold multiple items. You will need to use a data type that can do this. An <i>array</i> can be used to hold multiple values. For example:<br>
`let order = ["first", "second", "third"];`
This is an array which holds three values. Notice how the values are separated by commas.<br>
Change your `inventory` variable to be an array with the strings `"stick"`, `"dagger"`, and `"sword"`.

```js
let inventory = ["stick", "dagger", "sword"];
```

## **Step 14** 
For now, you want the player to start with just the `"stick"`. Change the `inventory` array to have `"stick"` as its only value.

```js
let inventory = ["stick"];
```

## **Step 15** 
In your role playing game, users will be able to track their stats, buy weapons, and fight monsters. Before you can continue with the interactive JavaScript portion of the game, you need to first create the HTML elements that will display the game information.<br>
Create four `div` elements within your `#game` element. Give them the following respective `id` values, in order: `stats`, `controls`, `monsterStats`, and `text`.

```html
<div id="stats"></div>
<div id="controls"></div>
<div id="monsterStats"></div>
<div id="text"></div>
```

## **Step 16** 
Create three `span` elements within your `#stats` element. Give each of them the class `stat`. Then give the first one the text `XP: 0`, the second one the text `Health: 100`, and the third one the text `Gold: 50`.

```js
<span class="stat">XP: 0</span>
<span class="stat">Health: 100</span>
<span class="stat">Gold: 50</span>
```

## **Step 17** 
Wrap the numbers `0`, `100`, and `50` in `span` elements, and wrap those new `span` elements in strong elements. Then give your new `span` elements `id` values of `xpText`, `healthText`, and `goldText`, respectively.<br>
Your answer should follow this basic structure:<br>
`<span class="stat">TEXT <strong><span id="VALUE">TEXT</span></strong></span>`

```html
<span class="stat">XP: <strong><span id="xpText">0</span></strong></span>
<span class="stat">Health: <strong><span id="healthText">100</span></strong></span>
<span class="stat">Gold: <strong><span id="goldText">50</span></strong></span>
```

## **Step 18** 
For your `#controls` element, create three `button` elements. The first should have the `id` set to `button1`, and the text `Go to store`. The second should have the `id` set to `button2`, and the text `Go to cave`. The third should have the `id` set to `button3`, and the text `Fight dragon`.

```html
<button id="button1">Go to store</button>
<button id="button2">Go to cave</button>
<button id="button3">Fight dragon</button>
```

## **Step 19** 
JavaScript interacts with the HTML using the <i>Document Object Model</i>, or DOM. The DOM is a tree of objects that represents the HTML. You can access the HTML using the `document` object, which represents your entire HTML document.<br>
One method for finding specific elements in your HTML is using the `querySelector()` method. The `querySelector()` method takes a CSS selector as an argument and returns the first element that matches that selector. For example, to find the `<h1>` element in your HTML, you would write:<br>
`let h1 = document.querySelector("h1");`<br>
Note that `h1` is a string and matches the CSS selector you would use.<br>
Create a `button1` variable and use `querySelector()` to assign it your element with the `id` of `button1`. Remember that CSS `id` selectors are prefixed with a `#`.

```js
let button1 = document.querySelector("#button1");
```

## **Step 20** 
We have run into a slight problem. You are trying to query your page for a button element, but your `script` tag is in the `head` of your HTML. This means your code runs before the browser has finished reading the HTML, and your `document.querySelector()` will not see the button - because the browser hasn't processed it yet.<br>
To fix this, move your `script` element out of the `head` element, and place it at the end of your `body` element (just before the closing `</body>` tag.)

```html
```

## **Step 21** 
`button1` is a variable that is not going to be reassigned. If you are not going to assign a new value to a variable, it is best practice to use the `const` keyword to declare it instead of the `let` keyword. This will tell JavaScript to throw an error if you accidentally reassign it.<br>
Change your `button1` variable to be declared with the `const` keyword.

```js
const button1 = document.querySelector("#button1");
```

## **Step 22** 
Use `querySelector()` to get the other two `button` elements using their `id`s: `button2` and `button3`. Store them in variables called `button2` and button3. Remember to use `const`.<br>

```js
const button2 = document.querySelector("#button2");
const button3 = document.querySelector("#button3");
```

## **Step 23** 
Similar to your `#stats` element, your `#monsterStats` element needs two `span` elements. Give them the class `stat` and give the first element the text `Monster Name:` and the second the text `Health:` . After the text in each, add a `strong` element with an empty nested `span` element. Give the first inner `span` element an `id` of `monsterName` and the second inner `span` element an `id` of `monsterHealth`.

```html
<span class="stat">Monster Name: <strong><span id="monsterName"></span></strong></span>
<span class="stat">Health: <strong><span id="monsterHealth"></span></strong></span>
```

## **Step 24** 
Give your `#text` element the following text:<br>
`Welcome to Dragon Repeller. You must defeat the dragon that is preventing people from leaving the town. You are in the town square. Where do you want to go? Use the buttons above.`

```html
<p>Welcome to Dragon Repeller. You must defeat the dragon that is preventing people from leaving the town. You are in the town square. Where do you want to go? Use the buttons above.</p>
```

## **Step 25** 
Now we need some quick styling. Start by giving the `body` a `background-color` set to `#0a0a23`.

```css
body {
  background-color: #0a0a23;
}
```

## **Step 26** 
Give the `#text` element a `background-color` of `#0a0a23`, a `color` of `#ffffff`, and `10px` of padding on all sides.

```css
#text {
  background-color: #0a0a23;
  color: #ffffff;
  padding: 10px;
}
```

## **Step 27** 
Give your `#game` a maximum width of `500px` and a maximum height of `400px`. Set the `background-color` to `#ffffff` and the `color` to `#ffffff`.<br>
Use margins to center it by setting the top margin to `30px`, bottom margin to `0px`, and the left and right margin to `auto`.<br>
Finally, give it `10px` of padding on all four sides.

```css
#game {
  max-width: 500px;
  max-height: 400px;
  background-color: #ffffff;
  color: #ffffff;
  margin-top: 30px;
  margin-bottom: 0; 
  margin-left: auto;
  margin-right: auto;
  padding: 10px;
}
```

## **Step 28** 
Using a selector list (`selector1, selector2`) give both your `#controls` and `#stats` elements a `border` of `1px solid #0a0a23`, a `#0a0a23` text color, and `5px` of `padding`.

```css
#controls, #stats {
  border: 1px solid #0a0a23;
  color: #0a0a23;
  padding: 5px;
}
```

## **Step 29** 
Give your `#monsterStats` element the same `border` and `padding` as your `#stats` element. Set its color to `#ffffff` and give it a `#c70d0d` background.

```css
#monsterStats {
  border: 1px solid #0a0a23;
  padding: 5px;
  color:  #ffffff;
  background: #c70d0d;
}
```

## **Step 30** 
For now, hide your `#monsterStats` element with the `display` property. Do not change any of the other styling.

```css
display: none;
```

## **Step 31** 
Next, give your `.stat` elements a `padding-right` of `10px`.

```css
.stat {
  padding-right: 10px;
}
```

## **Step 32** 
Finally, you will need to add some styles for your buttons. Start by setting the `cursor` property to `pointer`. Then set the text `color` to `#0a0a23` and the `background-color` to `#feac32`.<br>
Then set the `background-image` property to `linear-gradient(#fecc4c, #ffac33)`. Lastly, set the `border` to `3px solid #feac32`.

```css
button {
  cursor: pointer;
  color: #0a0a23;
  background-color: #feac32;
  background-image: linear-gradient(#fecc4c, #ffac33);
  border: 3px solid #feac32;
}
```

## **Step 33** 
Just like you did with the buttons, create variables for the following `id`s and use `querySelector()` to give them the element as a value:<br>
`text`, `xpText`, `healthText`, `goldText`, `monsterStats`, and `monsterName`.<br>
Remember to declare these with the `const` keyword, and name the variables to match the `ids`.

```js
const text = document.querySelector("#text");
const xpText = document.querySelector("#xpText");
const healthText = document.querySelector("#healthText");
const goldText = document.querySelector("#goldText");
const monsterStats = document.querySelector("#monsterStats");
const monsterName = document.querySelector("#monsterName");
```

## **Step 34** 
Finally, use `querySelector()` to get the `#monsterHealth` element. Because you have already declared a `monsterHealth` variable earlier, you need to use a different variable name for this element.<br>
Declare a new variable with the `const` keyword and name it `monsterHealthText`.

```js
const monsterHealthText = document.querySelector("#monsterHealth");
```

## **Step 35** 
Functions are special tools that allow you to run sections of code at specific times. You can declare functions using the `function` keyword. Here is an example of a function called `functionName` - note the opening and closing curly braces. These indicate the section of code that is within the function.<br>
`function functionName() {`<br>
`}`<br>
Create an empty function named `goStore`.

```js
function goStore() {}
```

## **Step 36** 
For now, make your `goStore` function output the message `"Going to store."` to the console. For example, here is a function that outputs the message `"Hello World"`.<br>
`function functionName() {`<br>
    `console.log("Hello World");`<br>
`}`<br>

```js
function goStore() {
  console.log("Going to store.");
}
```

## **Step 37** 
Now create a `goCave` function that prints `"Going to cave."` to the console.

```js
function goCave() {
  console.log("Going to cave.");
}
```

## **Step 38** 
Now create a `fightDragon` function that prints `"Fighting dragon."` to the console.

```js
function fightDragon() {
  console.log("Fighting dragon.");
}
```

### **Step 39** 
Comments allow you to add notes to your code. In JavaScript, single-line comments can be written with `//` and multi-line comments can be written with `/*` and `*/`. For example, here are single and multi-line comments that say "Hello World":<br>
`// hello world`<br>
`/*`<br>
  `hello world`<br>
`*/`<br>
Add a single-line comment that says `initialize buttons`.

```js
// initialize buttons
```

## **Step 40** 
`button1` represents your first `button` element. These elements have a special property called `onclick`, which you can use to determine what happens when someone clicks that button.<br>
You can access properties in JavaScript a couple of different ways. The first is with <i>dot notation</i>. Here is an example of using dot notation to set the `onclick` property of a button to a function reference.<br>
`button.onclick = myFunction;`<br>
In this example, `button` is the button element, and `myFunction` is a reference to a function. When the button is clicked, `myFunction` will be called.<br>
Use dot notation to set the `onclick` property of your `button1` to the function reference of `goStore`. Note that `button1` is already declared, so you don't need to use `let` or `const`.

```js
button1.onclick = goStore;
```

## **Step 41** 
Using the same syntax, set the `onclick` properties of `button2` and `button3` to `goCave` and `fightDragon` respectively.<br>
Once you have done that, open your console and try clicking the buttons on your project.

```js
button2.onclick = goCave;
button3.onclick = fightDragon;
```

## **Step 42** 
The `innerText` property controls the text that appears in an HTML element. For example:<br>
`<p id="info">Demo content</p>`<br> 
`const info = document.querySelector("#info");` <br>
`info.innerText = "Hello World";`<br>
The following example would change the text of the `p` element from `Demo content` to `Hello World`.<br>
When a player clicks your `Go to store` button, you want to change the buttons and text. Remove the code inside the `goStore` function and add a line that updates the text of `button1` to say `"Buy 10 health (10 gold)"`.

```js
function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
}p;
```

## **Step 43** 
Now, add a line that updates the text of `button2` to say `"Buy weapon (30 gold)"` and update the text of `button3` to say `"Go to town square"`.

```js
button2.innerText = "Buy weapon (30 gold)";
button3.innerText = "Go to town square";
```

## **Step 44** 
You will also need to update the functions that run when the buttons are clicked again.<br>
In your `goStore()` function, update the `onclick` property for each button to run `buyHealth`, `buyWeapon`, and `goTown`, respectively.

```js
button1.onclick = buyHealth;
button2.onclick = buyWeapon;
button3.onclick = goTown;
```

## **Step 45** 
Now you need to modify your display text. Change the `innerText` property of the `text` to be `"You enter the store."`.

```js
text.innerText = "You enter the store.";
```


## **Step 46** 
Create three new empty functions called `buyHealth`, `buyWeapon`, and `goTown`.

```js
function buyHealth() {}
function buyWeapon() {}
function goTown() {}
```

## **Step 47** 
Move your `goTown` function above your `goStore` function. Then copy and paste the contents of the `goStore` function into the `goTown` function.

```js
function goTown() {
  button1.innerText = "Buy 10 health (10 gold)";
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
  button1.onclick = buyHealth;
  button2.onclick = buyWeapon;
  button3.onclick = goTown;
  text.innerText = "You enter the store.";
}
```

## **Step 48** 
In your `goTown` function, change your `button` elements' `innerText` properties to be `"Go to store"`, `"Go to cave"`, and `"Fight dragon"`. Update your `onclick` properties to be `goStore`, `goCave`, and `fightDragon`, respectively.<br>
Finally, update `innerText` property of your `text` to be `"You are in the town square. You see a sign that says Store."`.

```js
function goTown() {
  button1.innerText = "Go to store";
  button2.innerText = "Go to cave";
  button3.innerText = "Fight dragon";
  button1.onclick = goStore;
  button2.onclick = goCave;
  button3.onclick = fightDragon;
  text.innerText = "You are in the town square. You see a sign that says Store.";
}
```

## **Step 49** 
You need to wrap the text `Store` in double quotes. Because your string is already wrapped in double quotes, you'll need to escape the quotes around `Store`. You can escape them with a backslash `\`. Here is an example:<br>
`const escapedString = "Naomi likes to play \"Zelda\" sometimes.";`<br>
Wrap the text `Store` in double quotes within your `text.innerText line`.

```js
\"Store\"
```

## **Step 50** 
You have repetition in the `goTown` and `goStore` functions. When you have repetition in your code, this is a sign that you need another function. Functions can take parameters, which are values that are given to the function each time it is run. Here is a function that takes a parameter called `param`:<br>
`function myFunction(param) {`<br>
    `console.log(param);`<br>
`}`<br>
Create an empty `update` function that takes a parameter called `location`.

```js
function update(location) {}
```

## **Step 51** 
In your role playing game, you will be able to visit different locations like the <b>store</b>, the <b>cave</b>, and the <b>town square</b>. You will need to create a data structure that will hold the different locations.<br>
Use `const` to create a variable called `locations` and assign it an empty array.

```js
const locations = [];
```

## **Step 52** 
Before you can begin to build out your `locations` array, you will first need to learn about objects. Objects are an important data type in JavaScript. The next few steps will be dedicated to learning about them so you will better understand how to apply them in your project.<br>
Objects are non primitive data types that store key-value pairs. Non primitive data types are mutable data types that are not `undefined`, `null`, `boolean`, `number`, `string`, or `symbol`. Mutable means that the data can be changed after it is created.<br>
Here is the basic syntax for an object:<br>
`{`<br>
  `key: value`<br>
`}`<br>
You will learn about keys and values in the next few steps.<br>
For now, create a `const` variable called `cat` and assign it an empty object `{}`.<br>
Below that `cat` variable, add a `console.log(cat)` statement to see the object in the console.

```js
const cat = {};
console.log(cat)
```

## **Step 53** 
Objects are similar to `arrays`, except that instead of using indexes to access and modify their data, you access the data in objects through `properties`.<br>
Properties consist of a key and a value. The key is the name of the property, and the value is the data stored in the property.<br>
Here is an example of an object with a single property:<br>
`const obj = {`<br>
  `name: "Quincy Larson"`<br>
`};`<br>
Inside your `cat` object, add a new property. The key should be `name` and the value should be the string `"Whiskers"`.<br>
Open up the console to see the updates to your object.

```js
const cat = {
  name: "Whiskers"
};
```

## **Step 54** 
If the property name (key) of an object has a space in it, you will need to use single or double quotes around the name.<br>
Here is an example of an object with a property name that has a space:<br>
`const spaceObj = {`<br>
  `"Space Name": "Kirk",`<br>
`};`<br>
If you tried to write a key without the quotes, it would throw an error:<br>
`const spaceObj = {`<br>
  `// Throws an error`<br>
  `Space Name: "Kirk",`<br>
`};`<br>
Add a new property with a key of `"Number of legs"` and value of `4` to the `cat` object.<br>
Open up the console to see the output.

```js
"Number of legs": 4
```

## **Step 55** 
There are two ways to access the properties of an object: dot notation (`.`) and bracket notation (`[]`), similar to an array.<br>
Dot notation is what you use when you know the name of the property you're trying to access ahead of time.<br>
`object.property;`<br>
Here is a sample of using dot notation (`.`) to read the `name` property of the `developer` object:<br>
`const developer = {`<br>
  `name: "Jessica",`<br>
`}`<br>
`// Output: Jessica`<br>
`console.log(developer.name);`<br>
Update your console statement to access the `name` property of the `cat` object using dot notation.<br>
Open up the console to see the `name` of `"Whiskers"` logged to the console.

```js
console.log(cat.name);
```

## **Step 56** 
The second way to access the properties of an object is bracket notation (`[]`). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.<br>
`objectName["property name"];`<br>
Here is a sample of using bracket notation to read an object's property:<br>
`const spaceObj = {`<br>
  `"Space Name": "Kirk",`<br>
`};`<br>
`spaceObj["Space Name"]; // "Kirk"`<br>
Update your console statement to use bracket notation to access the property `"Number of legs"` of the `cat` object.<br>
Open up the console to see the output.

```js
console.log(cat["Number of legs"]);
```

## **Step 57** 
Later on in the curriculum, you will dive deeper into objects. But for now, it is time to apply what you have learned to your role playing game.<br>
Start by deleting your `cat` object and console statement.

```js
```

## **Step 58** 
Your locations `array` will hold different locations like the <b>store</b>, the <b>cave</b>, and the <br>town square</br>. Each location will be represented as an object.<br>
Inside your locations array, add an object. Inside that object add a key called `name` with a value of `"town square"`.<br>
Remember to follow this syntax:<br>
`{`<br>
  `key: value`<br>
`}`<br>

```js
const locations = [
  {
    name: "town square"
  }
];
```

## **Step 59** 
Just like array values, object properties are separated by a comma. Add a comma after your `name` property and add a `button text` property with the value of an empty array.<br>
Since the property name has a space in it, you will need to surround it with quotes.<br>
`{`<br>
  `name: "Naomi",`<br>
  `"favorite color": "purple"`<br>
`}`<br>

```js
"button text": []
```

## **Step 60** 
Give your `empty button` text array three string elements. Use the three strings being assigned to the button `innerText` properties in the `goTown` function. Remember that array values are separated by commas.

```js
"button text": ["Go to store", "Go to cave", "Fight dragon"]
```

## **Step 61** 
Create another property in your object called `button functions`. Give this property an array containing the three functions assigned to the `onclick` properties in the `goTown` function. Remember that these functions are variables, not strings, and should not be wrapped in quotes.

```js
"button functions": [goStore, goCave, fightDragon]
```

## **Step 62** 
Add one final property to the object named `text`. Give this property the same string value as the one assigned to `text.innerText` in the `goTown` function.

```js
text: "You are in the town square. You see a sign that says \"Store\"."
```

## **Step 63** 
Add a second object to your `locations` array (remember to separate them with a comma). Following the pattern you used in the first object, create the same properties but use the values from the `goStore` function. Set the `name` property to `store`.

```js
{
  name: "store",
  "button text": ["Buy 10 health (10 gold)", "Buy weapon (30 gold)", "Go to town square"],
  "button functions": [buyHealth, buyWeapon, goTown],
  text: "You enter the store."
}
```

## **Step 64** 
Now you can consolidate some of your code. Start by copying the code from inside the `goTown` function and paste it into your `update` function. Then, remove all the code from inside the `goTown` and `goStore` functions.

```js
function update(location) {
  button1.innerText = "Go to store";
  button2.innerText = "Go to cave";
  button3.innerText = "Fight dragon";
  button1.onclick = goStore;
  button2.onclick = goCave;
  button3.onclick = fightDragon;
  text.innerText = "You are in the town square. You see a sign that says \"Store\".";
}
```

## **Step 65** 
Instead of assigning the `innerText` and `onclick` properties to specific strings and functions, the `update` function will use data from the `location` that is passed into it. First, that data needs to be passed.<br>
Inside the `goTown` function, call the `update` function. Here is an example of calling a function named `myFunction`:<br>
`myFunction();`

```js
function goTown() {
  update();
}
```

## **Step 66** 
Now it is time to use your `update` function. Pass in your `locations` array into the `update` function call.<br>
You pass arguments by including them within the parentheses of the function call. For example, calling `myFunction` with an `arg` argument would look like:<br>
`myFunction(arg)`<bnr>
Pass your `locations` array into the `update`call.

```js
update(locations);
```

## **Step 67** 
The `locations` array contains two locations: the `"town square"` and the `"store"`. Currently you are passing that entire array into the `update` function.<br>
Pass in only the first element of the `locations` array by adding `[0]` at the end of the variable. For example: `myFunction(arg[0]);`.<br>
This is called <i>bracket notation</i>. Values in an array are accessed by index. Indices are numerical values and start at `0` - this is called zero-based indexing. `arg[0]` would be the first element in the `arg` array.

```js
update(locations[0]);
```

## **Step 68** 
Now your `update` function needs to use the argument you pass into it.<br>
Inside the `update` function, change the value of the `button1.innerText` assignment to be `location["button text"]`. That way, you use bracket notation to get the `"button text"` property of the `location` object passed into the function.

```js
button1.innerText = location["button text"];
```

## **Step 69** 
`location["button text"]` is an array with three elements. Change the `button1.innerText` assignment to be `location["button text"][0]` which represents the first element of the array.

```js
button1.innerText = location["button text"][0];
```

## **Step 70** 
Now update `button2.innerText` and `button3.innerText` to be assigned the second and third values of the `"button text"` array, respectively.

```js
button2.innerText = location["button text"][1];
button3.innerText = location["button text"][2];
```

## **Step 71** 
Following the same pattern as you did for the button text, update the three buttons' `onclick` assignments to be the first, second, and third values of the `"button functions"` array.

```js
button1.onclick = location["button functions"][0];
button2.onclick = location["button functions"][1];
button3.onclick = location["button functions"][2];
```

## **Step 72** 
Finally, update the `text.innerText` assignment to equal the `text` from the `location` object. However, instead of using bracket notation, use <i>dot notation</i>.<br>
Here is an example of accessing the `name` property of an object called `person`:<br>
`person.name`

```js
text.innerText = location.text;
```

## **Step 73** 
Now update your `goStore` function to call the `update` function. Pass the second element of the `locations` array as your argument.<br>
To make sure your refactoring is correct, try clicking your first button again. You should see the same changes to your webpage that you saw earlier.

```js
update(locations[1]);
```

## **Step 74** 
Create two more empty functions named `fightSlime` and `fightBeast`. These functions will be used in your upcoming `cave` object.

```js
function fightSlime() {}
function fightBeast() {}
```

## **Step 75** 
Add a third object to the `locations` array. Give it the same properties as the other two objects.<br>
Set `name` to `cave`. Set `button text` to an array with the strings `"Fight slime"`, `"Fight fanged beast"`, and `"Go to town square"`. Set the `"button functions"` to an array with the variables `fightSlime`, `fightBeast`, and `goTown`. Set the `text` property to `"You enter the cave. You see some monsters."`.

```js
{
  name: "cave",
  "button text": ["Fight slime", "Fight fanged beast", "Go to town square"],
  "button functions": [fightSlime, fightBeast, goTown],
  text: "You enter the cave. You see some monsters."
}
```

## **Step 76** 
Now that you have a `"cave"` location object, update your `goCave` function to call `update` and pass that new `"cave"` location. Remember that this is the third element in your `locations` array.<br>
Don't forget to remove your `console.log call!`

```js
update(locations[2]);
```

## **Step 77** 
Now that your `"store"` and `"cave"` locations are complete, you can code the actions the player takes at those locations. Inside the `buyHealth` function, set `gold` equal to `gold` minus `10`.<br>
For example, here is how you would set `num` equal to `5` less than `num`: `num = num - 5;`.

```js
gold = gold - 10;
```

## **Step 78** 
After the `gold` is updated, add a line to set `health` equal to `health` plus `10`.

```js
health = health + 10;
```

## **Step 79** 
There is a shorthand way to add or subtract from a variable called <i>compound assignment</i>. For example, changing `num = num + 5` to compound assignment would look like `num += 5`.<br>
Update both lines inside your `buyHealth` function to use compound assignment.

```js
gold -= 10;
health += 10;
```

## **Step 80** 
Now that you are updating the `gold` and `health` variables, you need to display those new values on the game screen.<br>
After your assignment lines, assign the `innerText` property of `goldText` to be the variable `gold`. Use the same pattern to update `healthText` with the `health` variable.<br>
Here is an example:<br>
`let value = 100;`<br>
`const total = document.querySelector('#total');`<br>
`total.innerText = value;`<br>
You can test this by clicking your `"Go to store"` button, followed by your `"Buy Health"` button.<br>
<b>Note</b>: Your answer should only be two lines of code.

```js
goldText.innerText = gold;
healthText.innerText = health;
```

## **Step 81** 
What if the player doesn't have enough gold to buy health? When you want to run code conditionally, you can use the <i>if</i> statement.<br>
An `if` statement is used to make decisions in code. The keyword `if` is followed by a condition in parentheses. If the condition is true, the code inside the curly braces `{}` is executed. If the condition is false, the code inside the curly braces is skipped.<br>
Here is an example of an `if` statement:<br>
`const num = 5;`<br>
`if (num >= 3) {`<br>
  `console.log("This code will run because num is greater than or equal to 3.");`<br>
`}`<br>
Start by placing all of the code in your `buyHealth` function inside an `if` statement. For the `if` statement condition, check if `gold` is greater than or equal to `10`.

```js
function buyHealth() {
  if (gold >= 10) {
    gold -= 10;
    health += 10;
    goldText.innerText = gold;
    healthText.innerText = health;
  }
}
```

## **Step 82** 
Now when a player tries to buy health, it will only work if they have enough money. If they do not, nothing will happen. Add an `else` statement where you can put code to run if a player does not have enough money.<br>
Here is an example of an empty `else` statement:<br>
`if (num >= 5) {`<br>
`} else {`<br>
`}`

```js
  if (gold >= 10) {
    gold -= 10;
    health += 10;
    goldText.innerText = gold;
    healthText.innerText = health;
  } else { 
  }
```

## **Step 83** 
Inside the `else` statement, set `text.innerText` to equal `"You do not have enough gold to buy health."`.

```js
text.innerText = "You do not have enough gold to buy health.";
```

## **Step 84** 
Use `const` to create a `weapons` variable above your `locations` array. Assign it an empty array

```js
const weapons = [];
```

## **Step 85** 
Just like your `locations` array, your `weapons` array will hold objects. Add four objects to the `weapons` array, each with two properties: `name` and `power`. The first should have the `name` set to `"stick"` and the `power` set to `5`. The second should be `"dagger"` and `30`. The third, `"claw hammer"` and `50`. The fourth, `"sword"` and `100`.

```js
{
  name: "stick",
  power: 5
},
{
  name: "dagger",
  power: 30
},
{
  name: "claw hammer",
  power: 50
}, 
{
  name: "sword",
  power: 100
}
```

## **Step 86** 
Inside your `buyWeapon` function, add an `if` statement to check if `gold` is greater than or equal to `30`.

```js
if (gold >= 30){}
```

## **Step 87** 
Similar to your `buyHealth` function, set `gold` equal to `30` less than its current value. Make sure this is inside your `if` statement.

```js
gold -= 30;
```

## **Step 88** 
The value of the `currentWeapon` variable corresponds to an index in the `weapons` array. The player starts with a `"stick"`, since `currentWeapon` starts at `0` and `weapons[0]` is the `"stick"` weapon.<br>
In the `buyWeapon` function, use compound assignment to add `1` to `currentWeapon` - the user is buying the next weapon in the `weapons` array.

```js
currentWeapon += 1;
```

## **Step 89** 
Increasing a value by 1, or <i>incrementing</i>, has a special operator in JavaScript: `++`. If you wanted to increase `num` by `1`, you could write `num++`.<br>
Change your `currentWeapon` assignment to use the increment operator.

```js
currentWeapon++;
```

## **Step 90** 
Now update the `goldText` element to display the new value of `gold`, and update the `text` element to display `"You now have a new weapon."`.

```js
gold--;
goldText.innerText = gold;
text.innerText = "You now have a new weapon.";
```

## **Step 91** 
You should tell the player what weapon they bought. In between the two lines you just wrote, use `let` to initialize a new variable called `newWeapon`. Set this to equal `weapons`.

```js
let newWeapon = weapons;
```


## **Step 92** 
Use bracket notation to access an object within the `weapons` array and assign it to your `newWeapon` variable. Place the variable `currentWeapon` within the brackets.<br>
When you use a variable in bracket notation, you are accessing the property or index by the <i>value</i> of that variable.<br>
For example, this code uses the `index` variable to access a value of `array`.<br>
`let value = array[index];`

```js
let newWeapon = weapons[currentWeapon];
```

## **Step 93** 
`weapons[currentWeapon]` is an object. Use dot notation to get the `name` property of that object.

```js
let newWeapon = weapons[currentWeapon].name;
```

## **Step 94** 
You can insert variables into a string with the <i>concatenation operator</i> `+`. Update the `"You now have a new weapon."` string to say `"You now have a "` and the name of the new weapon. Remember to end the sentence with a period.<br>
Here is an example that creates the string `"Hello, our name is freeCodeCamp."`:
`const ourName = "freeCodeCamp";`<br>
`const ourStr = "Hello, our name is " + ourName + ".";`<br>

```js
text.innerText = "You now have a " + newWeapon + ".";
```

## **Step 95** 
Back at the beginning of this project, you created the `inventory` array. Add the `newWeapon` to the end of the `inventory` array using the `push()` method.<br>
Here is an example:<br>
`const arr = ["first"];`<br>
`const next = "second";`<br>
`arr.push(next);`<br>
`arr` would now have the value `["first", "second"]`.

```js
inventory.push(newWeapon);
```

## **Step 96** 
Up until now, any time `text.innerText` was updated, the old text was erased. This time, use the `+=` operator to add text to the end of `text.innerText`.<br>
Add the string `" In your inventory you have: "` - include the spaces at the beginning and the end.

```js
text.innerText += " In your inventory you have: ";
```

## **Step 97** 
At the end of the second `text.innerText` string you just added, use the concatenation operator to add the contents of `inventory` to the string.

```js
text.innerText += " In your inventory you have: " + inventory;
```

## **Step 98** 
Add an `else` statement to your `buyWeapon` function. In that statement, set `text.innerText` to equal `"You do not have enough gold to buy a weapon."`.

```js
else {
  text.innerText = "You do not have enough gold to buy a weapon.";
}
```

## **Step 99** 
Once a player has the best weapon, they cannot buy another one. Wrap all of the code in your `buyWeapon` function inside another `if` statement. The condition should check if `currentWeapon` is less than `3` - the index of the last weapon.

```js
function buyWeapon() {
  if(currentWeapon < 3) {
    if (gold >= 30) {
      gold -= 30;
      currentWeapon++;
      goldText.innerText = gold;
      let newWeapon = weapons[currentWeapon].name;
      text.innerText = "You now have a " + newWeapon + ".";
      inventory.push(newWeapon);
      text.innerText += " In your inventory you have: " + inventory;
    } else {
      text.innerText = "You do not have enough gold to buy a weapon.";
    }
  }
}
```

## **Step 100** 
Arrays have a `length` property that returns the number of items in the array. You may want to add new values to the `weapons` array in the future.<br>
Change your `if` condition to check if `currentWeapon` is less than the length of the `weapons` array. An example of checking the length of an array `myArray` would look like `myArray.length`.

```js
if (currentWeapon < weapons.length)
```


## **Step 101** 
You now have an error to fix. The `currentWeapon` variable is the index of the `weapons` array, but array indexing starts at zero. The index of the last element in an array is one less than the length of the array.<br>
Change the `if` condition to check w`eapons.length - 1`, instead of `weapons.length`.

```js
if (currentWeapon < weapons.length -1)
```

## **Step 102** 
Add an `else` statement for your outer `if` statement. Inside this new `else` statement, set `text.innerText` to `"You already have the most powerful weapon!"`.

```js
else {
  text.innerText = "You already have the most powerful weapon!";
}
```

## **Step 103** 
Once a player has the most powerful weapon, you can give them the ability to sell their old weapons.<br>
In the outer `else` statement, set `button2.innerText` to `"Sell weapon for 15 gold"`. Also set `button2.onclick` to the function name `sellWeapon`.

```js
button2.innerText = "Sell weapon for 15 gold";
button2.onclick = sellWeapon;
```

## **Step 104** 
Create an empty `sellWeapon` function.

```js
function sellWeapon() {}
```

## **Step 105** 
Players should not be able to sell their only weapon. Inside the `sellWeapon` function, add an `if` statement with a condition that checks if the length of the `inventory` array is greater than `1`.

```js
if (inventory.length > 1) {}
```

## **Step 106** 
Inside the `if` statement, set `gold` equal to `15` more than its current value. Also update `goldText.innerText` to the new value.

```js
gold += 15;
goldText.innerText = gold;
```

## **Step 107** 

## **New section - updated steps!**
***Updated steps*** to the role playing game project from freeCodeCamp

## **Step 103** 
The next step is to create a variable called `currentWeapon`.<br>
Notice that you already have a `currentWeapon` variable elsewhere in your code. Since this new `currentWeapon` variable will be inside an `if` statement, it will be scoped only to that block of code.<br>
Scope is the term used to describe where a variable can be accessed. If a variable is declared inside a block of code, it is only accessible to the code inside that block. This is called block scope.<br>
`let num = 1;`
`if (num === 1) {`
  `let num = 2; // this num is scoped to the if statement`
  `console.log(num); // expected output: 2`
`}`
`console.log(num); // expected output: 1(the global variable)`<br
Use the `let` keyword to create a variable named `currentWeapon`. Don't assign it a value yet.

```js
let currentWeapon 
```

## **Step 104** 
In the previous project, you learned how to work with the `shift()` method to remove the first element from an array like this:<br>
`const myArray = ["first", "second", "third"];`
`const firstElement = myArray.shift();`
`// myArray is now ["second", "third"]`<br>
Use the `shift()` method to take the first element from the `inventory` array and assign it to your `currentWeapon` variable.

```js
currentWeapon = inventory.shift();
```

## **Step 105** 
After your `currentWeapon`, use the concatenation operator to set `text.innerText` to the string `"You sold a "`, then `currentWeapon`, then the string `"`.".

```js
text.innerText = "You sold a " + currentWeapon + ".";
```

## **Step 106** 
Now use the `+=` operator to add the string `" In your inventory you have: "` and the contents of `inventory` to the `text.innerText`. Make sure to include the space at the beginning and end of the `" In your inventory you have: "` string.

```js
text.innerText += " In your inventory you have: " + inventory;
```

## **Step 107** 
Use an `else` statement to run when the `inventory` length is not more than one. Set the `text.innerText` to say `"Don't sell your only weapon!"`.

```js
else {
  text.innerText = "Don't sell your only weapon!";
}
```

## **Step 108** 
Now you can start the code to fight monsters. To keep your code organized, your `fightDragon` function has been moved for you to be near the other `fight` functions.<br>
Below your `weapons` array, define a `monsters` variable and assign it an array. Set that array to have three objects, each with a `name`, `level`, and `health` properties. The first object's values should be `"slime"`, `2`, and `15`, in order. The second should be `"fanged beast"`, `8`, and `60`. The third should be `"dragon"`, `20`, and `300`.

```js
const monsters = [
  {name: "slime", level: 2, health: 15},
  {name: "fanged beast", level: 8, health: 60},
  {name: "dragon", level: 20, health: 300}
]
```

## **Step 109** 
Fighting each type of monster will use similar logic. Create an empty function called `goFight` to manage this logic.

```js
function goFight() {}
```

## **Step 110** 
In your `fightSlime` function, set `fighting` equal to `0` - the index of `slime` in the `monsters` array. Remember that you already declared `fighting` earlier in your code, so you do not need `let` or `const` here.<br>
On the next line, call the `goFight` function.

```js
fighting = 0;
goFight();
```

## **Step 111** 
Following the same pattern as the `fightSlime` function, use that code in the `fightBeast` and `fightDragon` functions. Remember that `beast` is at index `1` and `dragon` is at index `2`. Also, remove the `console.log` call from your `fightDragon` function.

```js
function fightBeast() {
  fighting = 1;
  goFight();
}

function fightDragon() {
  fighting = 2;
  goFight();
}
```

## **Step 112** 
At the end of your code, create two empty functions named `attack` and `dodge`.

```js
function attack() {}
function dodge() {}
```

## **Step 113** 
Add a new object to the end of the `locations` array, following the same properties as the rest of the objects. Set `name` to `"fight"`, `"button text"` to an array with `"Attack"`, `"Dodge"`, and `"Run"`, `"button functions"` to an array with `attack`, `dodge`, and `goTown`, and `text` to `"You are fighting a monster."`.

```js
{
  name: "fight",
  "button text": ["Attack", "Dodge", "Run"],
  "button functions": [attack, dodge, goTown],
  text: "You are fighting a monster."
}
```

## **Step 114** 
In the `goFight` function, call your `update` function with the fourth object in `locations` as an argument.

```js
update(locations[3]);
```

## **Step 115** 
Below your `update` call, set the `monsterHealth` to be the health of the current monster. You can get this value by accessing the `health` property of `monsters[fighting]` with dot notation.

```js
monsterHealth = monsters[fighting].health;
```

## **Step 116** 
By default, the HTML element that shows the monster's stats has been hidden with CSS. When the player clicks the "Fight dragon" button, the monster's stats should be displayed. You can accomplish this by using the <i>style</i> and <i>display</i> properties on the `monsterStats` element.<br>
The `style` property is used to access the inline style of an element and the `display` property is used to set the visibility of an element.<br> an example of how to update the display for a paragraph element:<br>
`const paragraph = document.querySelector('p');`
`paragraph.style.display = 'block';`<br>
Display the `monsterStats` element by updating the `display` property of the `style` property to `block`.

```js
monsterStats.style.display = 'block';
```


## **Step 117** 
Now, you will need to update the text for the current monster's name and health.<br>
Start by assigning `monsters[fighting].name` to the `innerText` property of `monsterName`. Then, assign `monsterHealth` to the `innerText `property of `monsterHealthText`.

```js
monsterName.innerText = monsters[fighting].name;
monsterHealthText.innerText = monsterHealth;
```

## **Step 118** 
Now you can build the `attack` function. First, update the `text` message to say `"The <monster name> attacks."`, replacing `<monster name>` with the name of the monster. Remember you can use the concatenation operator for this.

```js
text.innerText = "The " + monsters[fighting].name + " attacks.";
```

## **Step 119** 
On a new line, use the addition assignment operator(`+=`), to add the string `" You attack it with your <weapon>."` to the `text` value, replacing `<weapon>` with the player's current weapon. Additionally, remember that this line of text starts with a space so it will properly display.

```js
text.innerText += " You attack it with your " + weapons[currentWeapon].name + ".";
```

## **Step 120** 
Next, set `health` to equal `health` minus the monster's level. Remember you can get this from the `monsters[fighting].level` property.

```js
health -= monsters[fighting].level;
```

## **Step 121** 
Set `monsterHealth` to `monsterHealth` minus the power of the player's current weapon.<br>
Remember that you can access the power of the player's current weapon using `weapons[currentWeapon].power`.

```js
monsterHealth -= weapons[currentWeapon].power;
```

## **Step 122** 
The `Math` object in JavaScript contains static properties and methods for mathematical constants and functions. One of those is `Math.random()`, which generates a random number from `0` (inclusive) to `1` (exclusive). Another is `Math.floor()`, which rounds a given number down to the nearest integer.<br>
Using these, you can generate a random number within a range. For example, this generates a random number between `1` and `5`: `Math.floor(Math.random() * 5) + 1`;.<br>
Following this pattern, use the addition operator (`+`) to add a random number between `1` and the value of `xp` to your `monsterHealth -= weapons[currentWeapon].power`.

```js
monsterHealth -= weapons[currentWeapon].power + Math.floor(Math.random() * xp) + 1;
```

## **Step 123** 
Update `healthText.innerText` and `monsterHealthText.innerText` to equal `health` and `monsterHealth`.

```js
healthText.innerText = health;
monsterHealthText.innerText = monsterHealth;
```

## **Step 124** 
Add an `if` statement to check if `health` is less than or equal to `0`. If it is, call the `lose` function.

```js
if (health <= 0){
  lose();
}
```

## **Step 125** 
You can make an `else` statement conditional by using `else if`. Here's an example:<br>
`if (num > 10) {`<br>
`} else if (num < 5) {`<br>
`}`<br>
At the end of your `if` statement, add an `else if` statement to check if `monsterHealth` is less than or equal to `0`. In your `else if`, call the `defeatMonster` function.

```js
else if (monsterHealth <= 0 ){
  defeatMonster();
}
```

## **Step 126** 
At the end of your code, create the `defeatMonster` and `lose` functions. Leave them empty for now.

```js
function defeatMonster() {}
function lose() {}
```

## **Step 127** 
Inside the `dodge` function, set `text.innerText` equal to the string `"You dodge the attack from the <monster>"`. Replace `<monster>` with the name of the monster, using the `name` property.

```js
text.innerText = "You dodge the attack from the " + monsters[fighting].name;
```

## **Step 128** 
In your `defeatMonster` function, set `gold` equal to `gold` plus the monster's level times `6.7`. Remember you can get the monster's level by using `monsters[fighting].level`.<br>
Here is an example of setting `num` to `num` plus `5` * `8`: `num += 5 * 8`. Use `Math.floor()` to round the result down.

```js
gold += Math.floor(monsters[fighting].level * 6.7);
```

## **Step 129** 
Set `xp` to `xp` plus the monster's level.

```js
xp += monsters[fighting].level;
```

## **Step 130** 
Now update `goldText` and `xpText` to display the updated values.

```js
goldText.innerText = gold;
xpText.innerText =  xp;
```

## **Step 131** 
Finish the `defeatMonster` function by calling the `update` function with `locations[4]` as the argument.

```js
update(locations[4]);
```

## **Step 132** 
Your `locations` array doesn't have a fifth element, so `locations[4]` doesn't work.<br>
Add a new object at the end of the `locations` array, following the same structure as the other objects. Set `name` to `"kill monster"`, set `"button text"` to an array with three `"Go to town square"` strings, set `"button functions"` to an array with three `goTown` variables, and set `text` to `"The monster screams Arg! as it dies. You gain experience points and find gold."`.

```js
{
  name: "kill monster",
  "button text": ["Go to town square", "Go to town square", "Go to town square"],
  "button functions": [goTown, goTown, goTown],
  text: "The monster screams Arg! as it dies. You gain experience points and find gold."
}
```

## **Step 133** 
The word `"Arg!"` should have quotes around it. Besides escaping quotes, there is another way you can include quotation marks inside a string.<br>
Change the double quotes around the string `"The monster screams Arg! as it dies. You gain experience points and find gold."` to single quotes `'`, then add double quotes around `"Arg!"`.

```js
text: 'The monster screams "Arg!" as it dies. You gain experience points and find gold.'
```

## **Step 134** 
After a monster is defeated, the monster's stat box should no longer display.<br>
On the first line of the `update` function, use `monsterStats.style.display` to change the `display` value to none.

```js
monsterStats.style.display = "none";
```

## **Step 135** 
In the `lose` function, call the `update` function and pass in the sixth object of your `locations` array. Note that you haven't created this object just yet.

```js
update(locations[5]);
```

## **Step 136** 
At the end of your code, create a `restart` function. Inside this function, set `xp` to `0`, `health` to `100`, `gold` to `50`, `currentWeapon` to `0`, and set `inventory` to an array with the string `stick`.<br>
Also update the `innerText` properties of `goldText`, `healthText`, and `xpText` to their current values.<br>
Finally, call the `goTown()` function.

```js
function restart() {
  xp = 0;
  health = 100;
  gold = 50;
  currentWeapon = 0;
  inventory = ['stick'];
  goldText.innerText = gold;
  healthText.innerText = health;
  xpText.innerText = xp;
  goTown();
}
```

## **Step 137** 
In the `locations` array, add another object at the end. Set the `name` property to `"lose"`, set `"button text"` to an array with three `"REPLAY?"` strings, set `"button functions"` to an array with three `restart` variables, and set text to `"You die. &#x2620;"`.<br>
In a later step, you will update the code for the `&#x2620;` emoticon text to properly display on the page.

```js
{
  name: "lose",
  "button text": ["REPLAY?", "REPLAY?", "REPLAY?"],
  "button functions": [restart, restart, restart],
  text: "You die. &#x2620;"
}
```

## **Step 138** 
Back to your `attack` function - inside the `else if` block, create another `if` and `else` statement. If the player is fighting the dragon (`fighting` would be `2`), call the `winGame` function. Move the `defeatMonster()` call to the `else` block.<br>
For this step, you will need to use the strict equality (`===`) operator to check if `fighting` is equal to `2`.

```js
if (fighting === 2) {
  winGame ();
  } else {
  defeatMonster();
}
```

## **Step 139** 
In order for the `&#x2620;` emoticon text to properly display on the page, you will need to use the <i>innerHTML</i> property.<br>
The `innerHTML` property allows you to access or modify the content inside an HTML element using JavaScript.<br>
Here is an example of updating the content for this paragraph element using the `innerHTML` property.<br>
`<p id="demo">This is a paragraph.</p>`<br>
`document.querySelector("#demo").innerHTML = "Hello, innerHTML!";`<br>
In the `update` function, change `text.innerText` to `text.innerHTML`.

```js
text.innerHTML = location.text;
```

## **Step 140** 
After the `lose` function, create a function called `winGame`. Inside the `winGame` function, call the `update` function and pass in `locations[6]`.

```js
function winGame() {
  update(locations[6]);
}
```

## **Step 141** 
Add another object in the `locations` array. Everything should be the same as the `lose` object, except the `name` should be `"win"` and the text should be `"You defeat the dragon! YOU WIN THE GAME! &#x1F389;"`.

```js
{
  name: "win",
  "button text": ["REPLAY?", "REPLAY?", "REPLAY?"],
  "button functions": [restart, restart, restart],
  text: "You defeat the dragon! YOU WIN THE GAME! &#x1F389;"
}
```

## **Step 142** 
While your game is feature-complete at this stage, there are things you can do to make it more fun and engaging. To get started, you'll give `monsters` a dynamic attack value.<br>
Inside your `attack` function, change your `health -= monsters[fighting].level;` line to `health -= getMonsterAttackValue(monsters[fighting].level);`. This sets `health` equal to `health` minus the return value of the `getMonsterAttackValue` function, and passes the `level` of the monster as an argument.

```js
health -= getMonsterAttackValue(monsters[fighting].level);
```

## **Step 143** 
Below your `attack` function, create an empty function named `getMonsterAttackValue`. It should take `level` as a parameter.

```js
function getMonsterAttackValue (level) {}
```

## **Step 144** 
The attack of the monster will be based on the monster's `level` and the player's `xp`. In the `getMonsterAttackValue` function, use `const` to create a variable called `hit`. Assign it the equation `(level * 5) - (Math.floor(Math.random() * xp));`.<br>
This will set the monster's attack to five times their `level` minus a random number between `0` and the player's `xp`.

```js
const hit = (level * 5) - (Math.floor(Math.random() * xp));
```

## **Step 145** 
Log the value of `hit` to the console to use in debugging. Remember that you can do this with `console.log()`.

```js
console.log(hit);
```

## **Step 146** 
In the previous project, you learned how to work with the `return` keyword to return a value from a function like this:<br>
`function add(num1, num2) {`<br>
  `return num1 + num2;`<br>
`}`<br>
Use the `return` keyword to return the value of `hit` at the end of the function.

```js
return hit;
```

## **Step 147** 
If you play the game in its current state you might notice a bug. If your `xp` is high enough, the `getMonsterAttackValue` function will return a negative number, which will actually add to your total health when fighting a monster! You can fix this issue by using a <i>ternary</i> operator to ensure negative values are not returned.<br>
The `ternary operator` is a conditional operator and can be used as a one-line `if-else` statement. The syntax is: `condition ? expressionIfTrue : expressionIfFalse`.<br>
Here is an example of returning a value using an `if-else` statement and a refactored example using a ternary operator:<br>
`// if-else statement`
`if (score > 0) {`<br>
  `return score`<br>
`} else {`<br>
  `return default_score`<br>
`}`<br>
`// ternary operator`<br>
`return score > 0 ? score : default_score`<br>
In `getMonsterAttackValue`, change `return hit` to a ternary operator that returns `hit` if `hit` is greater than `0`, or returns `0` if it is not.

```js
return hit > 0 ? hit: 0;
```

## **Step 148** 
In your `attack` function, below the `health` variable, create an `if` statement. Set the condition to call the `isMonsterHit` function.

```js
if (isMonsterHit()) {}
```

## **Step 149** 
Move your `monsterHealth` assignment into your `if` block.

```js
if (isMonsterHit()) {
    monsterHealth -= weapons[currentWeapon].power + Math.floor(Math.random() * xp) + 1;
  }
```

## **Step 150** 
Add an `else` statement to the first `if` statement inside your `attack()` function. In the `else` statement, use the `+=` operator to add the text `" You miss."` to the end of `text.innerText`.

```js
else {
  text.innerText += " You miss.";
}
```

## **Step 151** 
Now create the `isMonsterHit` function. This will return a <i>boolean</i> value (true or false) to be used in your `if` statement. Return the result of the comparison `Math.random() > .2`.

```js
function isMonsterHit () {
  return Math.random() > .2;
}
```

## **Step 152** 
The player should hit if either `Math.random() > .2` <b>or</b> if the player's health is less than `20`.<br>
At the end of your `return` statement, use the <i>logical OR</i>operator `||` and check if `health` is less than `20`.<br>
The logical OR operator will use the first value if it is truthy – that is, anything apart from `NaN`, `null`, `undefined`, `0`, `-0`, `0n`, `""`, and `false`. Otherwise, it will use the second value.<br>
For example: `num < 10 || num > 20`.

```js
return Math.random() > .2 || health < 20;
```

## **Step 153** 
On every attack, there should be a chance that the player's weapon breaks. At the end of the `attack` function, add an empty `if` statement with the condition `Math.random() <= .1`.

```js
if (Math.random() <= .1) {}
```

## **Step 154** 
Use the `+=` operator to add `" Your <weapon> breaks."`, with a space in front of Your, to the end of `text.innerText`. Replace `<weapon>` with the last item in the `inventory` array using `inventory.pop()`, which will remove the last item in the array AND return it so it appears in your string.

```js
text.innerText += " Your " + inventory.pop() + " breaks.";
```

## **Step 155** 
Remember that the increment operator `++` can be used to increase a variable's value by `1`. There is also a decrement operator `--` that can be used to decrease a variable's value by `1`. For example:<br>
`let num = 10;`<br>
`num--;`<br>
`console.log(num); // Output: 9`<br>
Decrement the value of `currentWeapon` in your `if` statement, after you update the text.

```js
currentWeapon --;
```

## **Step 156** 
We don't want a player's only weapon to break. The logical AND operator checks if two statements are true.<br>
Use the <i>logical AND</i> operator `&&` to add a second condition to your `if` statement. The player's weapon should only break if `inventory.length` does not equal (`!==`) one.<br>
Here is an example of an `if` statement with two conditions:<br>
`if (firstName === "Quincy" && lastName === "Larson") {`<br>
`}`

```js
if (Math.random() <= .1 && inventory.length !== 1)
```

## **Step 157** 
Now you can add a small easter egg (hidden feature) to your game.<br>
Create a new function called `easterEgg` which calls the `update` function with `locations[7]` as the argument.

```js
function easterEgg() {
  update(locations[7]);
}
```

## **Step 158** 
Create an empty `pick` function with a parameter named `guess`.

```js
function pick(guess) {}
```

## **Step 159** 
Create two new functions named `pickTwo` and `pickEight`.<br>
Inside each of those, call the `pick()` function and pass either `2` or `8` as the argument depending on the function name.

```js
function pickTwo() {
  pick(2);
}

function pickEight() {
  pick(8);
}
```

## **Step 160** 
Add another object to your `locations` array. Set `name` to `"easter egg"`, set `"button text"` to an array with the strings `"2"`, `"8"`, and `"Go to town square?"`, set `"button functions"` to an array with the variables `pickTwo`, `pickEight`, and `goTown`, and `text` to `"You find a secret game. Pick a number above. Ten numbers will be randomly chosen between 0 and 10. If the number you choose matches one of the random numbers, you win!"`.

```js
{ 
  name: "easter egg", 
  "button text": ["2", "8", "Go to town square?"], 
  "button functions": [pickTwo, pickEight, goTown], 
  text: "You find a secret game. Pick a number above. Ten numbers will be randomly chosen between 0 and 10. If the number you choose matches one of the random numbers, you win!" 
}
```

## **Step 161** 
Inside `pick`, use `const` to initialize a variable named `numbers` and set it to an empty array.

```js
const numbers = [];
```

## **Step 162** 
After your `numbers` array, create a `while` loop that runs as long as `numbers.length` is less than `10`.<br>
In the previous project, you learned how to work with `while` loops like this:<br>
`while (condition) {`<br>
  `// code to run<`<br>
`}`<br>

```js
while (numbers.length < 10){}
```

## **Step 163** 
Inside your `while` loop, push a random number between `0` and `10` to the end of the `numbers` array. You can create this random number with `Math.floor(Math.random() * 11)`.

```js
numbers.push(Math.floor(Math.random() * 11));
```

## **Step 164** 
After the `while` loop, set `text.innerText` to equal `"You picked <someGuess>. Here are the random numbers:"`. Replace `<someGuess>` with the `guess` function parameter.

```js
text.innerText = "You picked " + guess + ". Here are the random numbers:"
```

## **Step 165** 
At the end of the string, before the final quote, insert the new line escape character `\n`. This will cause the next part you add to `text.innerText` to appear on a new line.

```js
text.innerText = "You picked " + guess + ". Here are the random numbers:\n";
```

## **Step 166** 
In the previous project, you learned how to work with `for` loops like this:<br>
`for (let i = 0; i < 5; i++) {`<br>
  `// code to run`<br>
`}`<br>
`for` loops are declared with three expressions separated by semicolons: `for (a; b; c)`, where `a` is the initialization expression, `b` is the condition, and `c` is the final expression.<br>
In this step, create a `for` loop where `i` is initialized to `0`, the loop runs as long as `i` is less than `10`, and `i` is incremented by `1` after each iteration using the increment operator `++`.

```js
for (let i = 0; i < 10; i++){}
```

## **Step 167** 
Now you can write the logic to run in the loop. Inside your `for` loop, use the `+=` operator to add to the end of `text.innerText`. Add the number at index `i` of the `numbers` array, using `numbers[i]`. Then add a new line, using the escape sequence you used earlier.

```js
text.innerText += numbers[i] + "\n";
```

## **Step 168** 
The `.includes()` method determines if an array contains an element and will return either `true` or `false`.<br>
Here is an example of the `.includes()` syntax:<br>
`const numbersArray = [1, 2, 3, 4, 5]`<br>
`const number = 3`<br>
`if (numbersArray.includes(number)) {`<br>
  `console.log("The number is in the array.")`<br>
`}`<br>
After your `for` loop, add an `if` statement to check if the `guess` is in the `numbers` array. You can use the .`includes()` method to check if the array contains the `guess`.

```js
if (numbers.includes(guess)) {}
```

## **Step 169** 
Inside the `if` statement, add the string `"Right! You win 20 gold!"` to the end of `text.innerText`. Also, add `20` to the value of `gold` and update the `goldText.innerText`.

```js
text.innerText += "Right! You win 20 gold!";
gold += 20;
goldText.innerText = gold;
```

## **Step 170** 
Now add an `else` statement. Inside, add `"Wrong! You lose 10 health!"` to the end of `text.innerText`. Subtract `10` from `health` and update `healthText.innerText`.

```js
else {
  text.innerText += "Wrong! You lose 10 health!";
  health -= 10;
  healthText.innerText = health;
}
```

## **Step 171** 
Since you subtracted health from the player, you need to check if the player's `health` is less than or equal to `0`. If it is, call the `lose` function.

```js
if (health <= 0) {
  lose();
}
```

## **Step 172** 
Looking at your `"kill monster"` object, `"button functions"` currently has three `goTown` variables. Replace the third one with `easterEgg` - this is how a player will access the hidden feature of the game. Do not change the `"button text"`.<br>
With this, your RPG game is complete! You can now play around - can you defeat the dragon?

```js
"button functions": [goTown, goTown, easterEgg],
```
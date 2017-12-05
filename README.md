# Pizzabot – Part 1

Today's assignment is to create a little text-based pizzabot in which you can order pizza on your computer. The goal is to practice basic programming concepts in JavaScript like variables, types, if-statements and functions.

## How to complete this assignment

A really good thing is to look through the readings for this assignment - you will find them helpful this time.

Write your bot in `code/pizzabot.js`, then open `code/index.html` in the browser to use the bot.

### 2. Practice variables and types

Before you start writing your "bot", there's a few things you should know about your pizzeria:

* Your pizzeria only serves 3 different pizzas right now; *Vegetarian*, *Hawaiian* and *Pepperoni*.
* All the pizzas have the same price - 80 SEK.
* Because of the popularity of your pizzeria, and long queues, you can only order multiple pizzas of the same sort.

We're going to be using a combination of `prompt()` and `alert()` to create the interaction between customer and bot in our pizzeria. Read more about how to use them here - https://www.w3schools.com/js/js_popup.asp

#### 2.1 Modeling the menu

To start you off, we've defined 4 variables in code/pizzabot.js which you'll use throughout the rest of this assignment:

```
const vegetarian = "Vegetarian Pizza"
const hawaiian = "Hawaiian Pizza"
const pepperoni = "Pepperoni Pizza"

const pizzaPrice = 80
```

#### 2.2 Greeting the customer

In code/pizzabot.js, you can start coding the bot interaction. The first step is to greet a new customer.

Use `alert()` to print the message `"Hey! Happy to serve your pizza. On our menu we have X, Y and Z"`.

Use the variables `vegetarian`, `hawaiian` and `pepperoni` to replace `X`, `Y` and `Z` in the message so that it reads `"Hey! Happy to serve your pizza. On our menu we have Vegetarian Pizza, Hawaiian Pizza and Pepperoni Pizza"`

#### 2.3 Ask the user which pizza they want, and how many

Use `prompt()` to ask the user which pizza they want. The message in the prompt should read `Enter the name of the pizza you want to order today.`. Their response should be stored in a new variable called `orderName`.

Next, ask the user (with another `prompt()`) how many they'd like: `How many of X do you want?`. X should be replaced with the `orderName` variable so that it if I ordered "Hawaiian Pizza" it would read "How many of Hawaiian Pizza do you want?". As before, the response from this prompt should be stored in a variable, this time called `orderQuantity`

#### 2.4 Finalizing the order

Calculate the total price of the order using the `orderQuantity` and `pizzaPrice` variables and store it in a variable called `orderTotal`. Use an alert to tell the user:  `Great, I'll get started on your X right away, it will cost Y kr` (where X should be replaced by the `orderName` variable and Y should be replaced by the `orderTotal` variable).

For example, if I ordered 3 Hawaiian pizzas, the message should read: "Great, I'll get started on your Hawaiian Pizza right away, it will cost 240 kr"

### 3. Conditionals

We want you to add three conditionals statements (if-statements) to your program to improve it.

#### 3.1 Checking that the Pizza is on the menu

When the user enters the `orderName` prompt, add an if-statement to check if the input text matches any of the pizza name variables (`vegetarian`, `hawaiian`, `pepperoni`).

#### Show cooking times

Before you print the final `Great, I'll get started on your X right away, it will cost Y kr` message to the user, calculate the cooking time based on these rules and add it to the message:

* 1-2 pizzas: `The pizzas will take 10 minutes.`
* 3-5 pizzas: `The pizzas will take 15 minutes.`
* 6+ pizzas: `The pizzas will take 20 minutes.`

For example, if I ordered 3 Hawaiian pizzas, the message should now read: "Great, I'll get started on your Hawaiian Pizza right away, it will cost 240 kr. The pizzas will take 15 minutes."

### 4. Functions

Finally, clean up your code by moving some code into functions and then calling that function when needed.

The functions should all reflect the tasks we've completed so far. So, the functions should be:

1. `checkOrderName()` which should take the `orderName` variable as an argument and return `true` or `false` if the pizza is on the menu or not.
1. `totalCost()` which takes `orderQuantity` as an argument and returns the total cost for the order.
1. `cookingTime()` which takes `orderQuantity` and returns the number of minutes it will take to finish the order.

### :books: Reading List

* [MDN - const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
* [MDN - let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
* [MDN - if/else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
* [MDN - arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

---

### :boom: Success!

After completing this assignment your should:

* Be comfortable using variables
* Know some string methods to modify strings
* Understand control flow and the use of conditionals statements
* Be able to write basic functions which take arguments and return values

---

### :runner: Stretch Goals

Done with the main task? Here's some ideas for things to continue with:

1. Go to the Wikipedia Article about [Hawaiian Pizza](https://en.wikipedia.org/wiki/Hawaiian_pizza) and:

* Copy the first three paragraphs. Store the text in a String
* Make your program count the number of words in the string
* Make your program count the number of times the word pineapple appears.

2. Instead of having your pizzabot live in the console make a form in HTML for the input from the user, pizza type and number of pizzas. Then make your program print it's response in HTML instead.

A combination of these two examples will help you on the way: [Forms submissions with JavaScript](https://www.w3schools.com/js/tryit.asp?filename=tryjs_form_submit) and [Get Element by ID](https://www.w3schools.com/js/exercise.asp?filename=exercise_arrays4).

---
layout: post
title:      "Fetching, Return and Async in JS "
date:       2019-01-18 04:44:50 +0000
permalink:  fetching_return_and_async_in_js
---


The more I work with JavaScript the more I realize that app development is about passing data. While working with JavaScript I have learned new ways of handling data on the front end. No longer am I required to communicate with the backend to render data. But in order to do this I had utilize and understand three main concepts: fetching, return and asynchronous.

### Fetching and Return

Fetch and return go hand in hand. The overarching functionality behind the two is a *Promise*. The goal is to return a *Promise* from a fetch() call. So, what is a *Promise*? First, we need to understand that fetch() takes an argument of a path to the resource you want to retrieve. Then, fetch() return a *Promise* which contains the reponse you were expecting. In it's simplest form, fetch() takes one argument to return a promise like the example below:

```
fetch('http://localhost:3000/api/places')
      .then(response => response.json())
```

It is also important to note that the purpose of a return statement is to terminate a function and return a specified value. If  return is called in a function body then that function's execution is stopped. This way we can ensure to retrieve the promised result.

### Async

In JavaScript we are enabled with the power to retrieve data instantly when it is updated on the display without talking to the server by utilizing asynchronous calls. In a nutshell, a fetch() is an asynchronous call. Therefore, the JavaScript code that is run will not wait for a value to be returned before moving on to the next statements. This kind of functionality was previously achieved using XMLHttpRequest.

These three functionalities all need to work together to render data to the page asynchronously.

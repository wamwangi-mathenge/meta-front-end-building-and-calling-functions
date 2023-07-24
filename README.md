# Building and calling functions

The purpose of this reading is to provide you with an example of function declaration (build) and function invocation (call).

By the end of this reading you should be able to:
- Code simple functions that can accept an array and iterate through it.

Let's start with giving our function declaration a name:
~~~
function listArrayItems(arr) {
    // ... code to be added ...
}
~~~

A function listArrayItems has been declared and set up to accept a single parameter, arr - which stands for an array.

Now, code a for loop over an array.
A for loop needs the following information:
1. the starting loop counter value as a temporary variable i
2. the exit condition (the maximum value of the loop counter variable i, above which the loop no longer runs) 
3. how to update the value of i after each loop

For this function declaration:
1. The loop's starting counter will be 0
2. The loop's exit condition is when the value of i is equal or greater than arr.length. (i < arr.length)
3. To make sure that none of the items in the arr array are skipped, I have to increase the value of i by 1 after each loop.

~~~
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        // ... code pending here ...
    }
}
~~~

You can decide to output each item from the received arr array by console logging the array item index of the value of i;

~~~
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(arr[i])
    }
}
~~~

When you invoke the listArrayItems function, you can, for example, give it the following array of colors:
~~~
var colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple', 'pink'];
listArrayItems(colors);
~~~

The output will be:
~~~
red
orange
yellow
green
blue
purple
pink
~~~

You can update the output any way you like. For example:
~~~
//function that takes an array as input and display all items of this array
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(i, arr[i])
    }
}
var colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple', 'pink'];
listArrayItems(colors);
~~~

The output will be as follows:
~~~
0 'red'
1 'orange'
2 'yellow'
3 'green'
4 'blue'
5 'purple'
6 'pink'
~~~

To start the count from one instead of zero, you can update my function declaration as follows:
~~~
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(i+1, arr[i])
    }
}
~~~

The output will be as follows:
~~~
1 'red'
2 'orange'
3 'yellow'
4 'green'
5 'blue'
6 'purple'
7 'pink'
~~~
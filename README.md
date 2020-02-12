Q1: Is the keyword "fixes" the only way to auto-close an issue from a PR (pull request). Is there other keywords that can accomplish the same thing?

There are other keywords that support linking an issue to a pull request. Other keywords include: close, closes, closed, fix, fixes, fixed, resolve, resolves, resolved.

Q2: Do you have to create a new PR EVERYTIME you want to close an issue, or is it possible to close multiple issues within a single PR? If so, how?

A single pull request can link multiple issues, so you do not need to create a pull request for each issue. To link multiple issues, simply list the issues that are resolved using the supported keywords from question 1 comma-separated.

Q3: Provide an example of using map that is different from the one I have done. Your example must use map both as a named function declaration and with an anonymous function. 
${
// userInput is the string object I am going to use which is defined by the user's input from a browser prompt.
let userInput = prompt("Enter an integer: ");

let userList = [userInput]

/* userList is the array I am calling the method map and I am passing the function I have written within the paratheses as the argument to the map method.
The function simply transforms the string object that I had originally into the type Number. 
The map is a method that accepts a transformation function as a parameter. The function must return a transformed object.
In this example, my anonymous function is simply returning the original object as a type Number.
*/

let newList = userList.map(function(input) {
return Number(input)}) 
}

/* In this example it is a named function called typeNumber and I'm using that function and calling it onto my array elements.*/


function typeNumber(input) {
	return Number(input);
}

let newList = userList.map(typeNumber);

// this will now return "Number" because I have transformed my string object into a Number from using map.
typeOf(newList[0]);

Within comments, explain exactly what map is doing. Finally, why is the "transformation function" we discussed in class sometimes referred to as a callback function.

The function is called a "callback" because the function is "called" on every element in a JSObject or array. The function must take the original element to be processed as an argument, and the it must return the new element that's going to be in place of the original element in the new array or JSObject. But it must also be able to invoke the same process into a second element, and a third element, etc.
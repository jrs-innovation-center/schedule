# Troubleshooting Guide

This is a guide on how one might go about troubleshooting problems with a web application, using tools like console.log, chrome dev tools, the debugger, and other resources.

## Setting up for success

The first part of troubleshooting is breaking tasks down into small little chunks. By doing things in little chunks, you can verify each step. (I recommend for each step to do a `commit`) this will give you an history and a bread crumb trail to narrow down the particular scope that an error may occur.

## Use a linter

> This space can get really confusing fast, there are a lot of opinions.

No Config Solution

* https://standardjs.com/

Configurable Solutions

* http://eslint.org/

Up and coming solution

* eslint and prettier - https://github.com/prettier/prettier

For right now, I would recommend either `standard` or `prettier`, standard will give you more code rules help and prettier will help keep your code formatted.  

## Commitment to keeping your console clean

Another important step to troubleshooting is keeping your console clean, so when something appears, it has high signal that this is an issue I need to deal with. If you have warnings or debug messages, I highly encourage you to create a habit of cleaning these up before committing your code.

## Encountering an error.

When encountering an error, be sure to read the error several times and look for clues. Some errors provide very clear information of what is wrong, others do not. Do not leave the error and go to the next step, at least disable the code that is producing the error, or revert your current changes and go back to a stable state, before moving to the next task.

If you don't recognize the error or have not immediate idea to what the message is saying, look for line number in the stack trace for a file you recognize.

* Run your linter tool via command line.
* Make sure there are no errors showing in your editor
* Look at the code at the line number, are there any typos or common mistakes (if you can't find a line number, use `git diff` to look at all the code you have changed)
* What is calling this code? Verify the data being passed to this code is actually being passed to this code block.
* Verify that the data as a result of this code is being returned.

Use console.log, react dev tools, chrome dev tools, to find the state before the bug and trace through the steps until the error occurs.

If you are using console.log, be sure to add meta data to know where your console log is. `console.log('some info: ', data)`

## Look for resources

If you are still unable to find out what is happening, try to describe the problem.

```
Using the following structure can help with describing an error:

* Introduction - Short description of the problem
* Background - what was the user doing to create this error
* Situation - what is the expectation

 As a User
 I want to …..
 So that I can do ……

* Assessment - Describe the error message and show a git diff between last commit.
```

By describing your error in this way will provide a person trying to help you with enough information to troubleshoot with you. Also include screenshots and links to your repository as well.

Seek help, post in slack, or ask a neighbor or google.

## Future Proof

You will often make the same mistakes in the future or encounter the same errors, if you document the error, take the time to keep a record of the errors you encounter, in either a separate repository, wiki or a document or any place that makes sense for you to go back an find.

Github issues is a great place to keep a record of all the errors you find, or creating a error log repository and adding a markdown document for each error. This can provide a great resource to your future self.

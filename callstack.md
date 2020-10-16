# Call Stack
> ***call*** stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc
- The JavaScript engine (which is found in a hosting environment like the browser) is a single-threaded interpreter comprising of a heap and a single call stack
  - the browser provides web APIs like the DOM, AJAX, and Timers

- when a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function
- any functions that are called by that function are added to the call stack further up
  - run where their calls are reached
- when the current function is finished, the interpreter takes it off the stack 
  - resumes execution where it left off in the last code listing
- **if the stack takes up more space than it had assigned to it, it results in a "stack overflow" error**

>understanding of the call stack will give clarity to how “function hierarchy and execution order” works in the JavaScript engine

The call stack is primarily used for function invocation (call) 
  - the call stack is single 
  - function(s) execution, is done, one at a time, from top to bottom 
    - means the call stack is *synchronous*

In Asynchronous JavaScript, we have a:
1. callback function
2. an event loop
3. task queue 

> The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

### What is the call stack?

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call)

#### Breakdown

- LIFO: operates by the data structure principle of Last In, First Out 
  - means that the last function that gets pushed into the stack is the first to be pop out, when the function returns

#### What causes a stack overflow?
- A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point 
- The browser (hosting environment) has a maximum stack call that it can accommodate before throwing a stack error
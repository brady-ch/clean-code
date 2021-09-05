
# Functions

## Abstract

Properties of a Good Function

| Property | Description/Explanation |
|---|---|
| [[#Small]] | The smaller a function is, usually, the easier it is to understand. |
| [[#Indentation]] | Functions should not be big enough to have nested structures, make a function call within a while loop, or if block. |
| [[#SRP]] | Single Responsibility Principle, functions should do one thing, do it well, and do it only. |
| [[#Abstraction]] | Everything within the function has the same level of abstraction. |
| [[#The Stepdown Rule]] | Reads from top to bottom descending in levels of abstraction. |
| [[Meaningful Names]] | Functions have a meaningful name that helps readers to understand the intent of the function. |
| [[#Few Function Arguments]] | Has few function arguments, the less function arguments the better. |
| [[#No Output Arguments]] | Do not mutate the arguments of a function. |
| [[#No Flag Arguments]] | Flag arguments will have the function do something different depending on the function value. |
| [[#DRY]] | Don't repeat yourself, reuse code when you can. |
| [[#Refactor]] | Making good functions is a process, it will get better as you refine it. |

## Edge Cases

### Switch Statements
Switches will violate many of these rules, however they can be tolerated if they appear only once. Hide them behind an inheritance relationship.

## Property Descriptions

### Small
 Functions should be small, as small as you can make them, make them descriptive, make them precise, make them tell a story leading you to the next part in a meaningful way. Make the inside of a loop, control statement, or try catch block a function call if needed.
 
 ### Indentation
 Functions should be short, make a function call within a loop, or a control statement. This also allows you to help document, it allows you to make a descriptive name for the function you are calling while also keeping the function short.
 
 ### SRP
 Single Responsibility Principle. At the level of abstraction you are working with within the scope of the function, you should be doing only one thing. This will mean your function should be short. If your function is divided into sections, this is a symptom of your function doing more than one thing.
 
 ### Abstraction
 Varying levels of abstraction within a function will tend to confuse the reader.
 
 ### The Stepdown Rule
Start at the highest level, essentially you want to start at the highest level of abstraction needed, stay within that level of abstraction and make calls to functions that are lower both as a level of abstraction and physically than the one you're in. 

### Few Function Arguments
Arguments are hard, the more you add the more complex your code gets. Arguments frequently have a different level of abstraction than the function they are in and need to be interpreted by the reader each time they are read. This also makes it difficult from a testing standpoint because writing tests for all the combinations of arguments will be difficult.

### No Output Arguments
This is not a hard and fast rule, just like anything here, but try the best you can to avoid unexpected mutations and doing multiple things at once. If your function must change the state of something (Assuming OOP) have it change the state of it's owning object. Much of output arguments have become obsolete with the introduction of the this keyword.

Example of what not to do:
```javascript
const arr = ["huh", "kay", "huhkay", "foo", "bar"];

arr.splice(3, 1, "foobar");
```
The issue with the above is not how we are using the spice method, but the splice method itself, it both removes and adds to the array, and also returns the value that was spliced. This may lead the developer to think a copy was returned when it actually modified the array.

### No Flag Arguments
Flag arguments are essentially an argument that will define what the function does, this is bad because it is also is an indicator that the function is doing multiple things.

### DRY
Don't Repeat Yourself. 

### Refactor
Refactor your code to make it better, to better follow these principles. This is how you will achieve truly good functions.



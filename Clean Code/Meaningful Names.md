# Meaningful Names
Names should reveal intent.

- Write meaningful names
- Avoid disinformation
	- example => Adding list to a variable name when it is not a list
- It is fine to have a longer name if it better declares intent
- Be careful of names that look similar or differ in small ways
- Make meaningful distinctions. Make meaningful discriminations between variables, like source and destination instead of a1 and a2
- Use pronounceable names, this is better because humans are better at sounding out names. This will make the code easier to talk about and read/understand. A large portion of our brains have evolved to handle spoken language. 
- Use Searchable Names, make them distinct and long enough that they are unique
- Only use single letter names as a local variable inside of a short method. The length of the name should correspond to the size of its scope.
- Avoid Encodings, it will complicate code when you do not need it to, it is confusing and easy to mistype
- Clarity is King
- Don't be cute, be professional and don't make inside jokes, make it easily recognizable what you are doing not just to yourself and maybe your team, but to everyone.
- One word per concept, pick a word per concept and stick with it. 
- Add context when necessary, if you need to add a prefix to make it more clear what it is your working with, do it when it would add clarity. 
- Don't add gratuitous context, don't add the same prefix for everything within a class, it makes it harder for your IDE to autocomplete for you, and makes much of the naming redundant.
- Short names are better than long names, as long as they are clear, but do not be afraid of long names if they add clarity.

## Properties of a good name

| Property  | Description|
|---|---|
| Avoids Disinformation | huhkayList // When huhkay is not a list |
| Is Visually Distinct | huhkayToArrayFromWord & huhkayToArrayFromWords is bad practice because they look very similar |
| Is Pronounceable | sdl179qr is bad practice |
| Is Searchable | c would not be a good variable as it would find all instances of the letter c |
| Is Not Encoded | Don't encode your names |
| Is Not Type Encoded | This is mostly irrelevant in modern languages |
| Is Clear | You should not have to have your readers translate your code into something else | 
| Is Professional | Don't use slang when making names, don't use inside jokes, don't use something that wouldn't be easily recognizable by everyone. |
| Is Consistent | Stay consistent with your naming, if you use get rather than retrieve, stick with it everywhere. |
| Has Context | There is context for your name, whether that means adding addr for address as a prefix to your name or it is immediately obvious based on the surrounding context |
| DRY | Don't repeat yourself, even in naming. Don't add too much context because your names will get long and redundant. It is important not add too much context in the same way it is important not to add not enough. |
 
### Class Names
Should be a noun, rather than a verb

### Methods
Methods should have verb or verb like names

When constructors are overloaded use static factory methods that describe the argument. 

Example: 
```java
Complex fulcrumPoint = new Complex(23.0);

// This is better because it describes the arguments
Complex fulcrumPoint = new Complex.fromRealNumber(23.0); 
```

You may even force their use by making their constructor private.

### Interfaces
Don't encode the interface, if you have to encode something encode the implementation. 

Example:
```java
CallHandler // Interface

CallhandlerImpl // Implementation
```
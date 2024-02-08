# Summary
One of the things that I've found lacking in some programming training is how to solve problems independently. While you may have received training on how to do things with a  technology in particular, converting an idea into code is something that can be challenging at times; hence why I decided to create this doc.
	1. Understand problems and how to break them down.
1. Google things.
2. Understand what different errors mean.

## Understand problems and how to break them down
Google is a great tool. Look up what your UI element looks like. Look at images of how one should be. Maybe there's even some basic code that fits to your problem, with some adaptations done.
## Google things
Say we did not know how to do something. We'd then have to search on Google to find different solutions. Here are some tips to make searching as smooth as possible:
- Include the technology's name in the search query.
- Add some context to your search.

# Understand errors
This is much more dependent on your programming language. If you're developing a project with Angular, there are several places like the terminal, the browser console, or the page itself where there can be errors. 

# Examples
One of the things we did during the internship was to remove dependencies from certain components. We did this, for example, with the breadcrumb component, where it was previously supplied via primeNG, and was changed to use our own Angular code in the end.

**Understand a problem.** In our instance, we would need to separate the problem we're trying to solve into different mini-problems. How does a breadcrumb look? How do I accept the data that contains the routes? How do I display it, with its particular styling?

Here is where the basic training in whatever programming language you're using is. In our Angular case, we know there's a bunch of attributes and properties we can use (reference [here](angular%20reference)). We need to iterate through an array.

**Understand errors.**

**Google things.** Examples: 
- how to iterate angular 
- display object in angular
- app breaks after angular custom webpack 

**Understand what different errors mean and basic steps.** There's a bunch of stuff in our code that can break. Try undoing changes quickly with ctrl+z (or cmd+z) to see where your code breaks. Remove ``node_modules``.



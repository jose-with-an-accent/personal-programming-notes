Depending on the type of program you're trying to make, there are different ways to debug and simplify the finding-out process.

## C
**GDB** is the main tool used to debug. This tool allows for step-through, step-in, and step-out work that can be used to go to other lines of code, check out null pointers and memory, and even reverse-engineer code in some cases. **Valgrind** is used to check for memory leaks, so it is helpful if there's problems with memory.

This tool can also be connected to apps like Visual Studio, which make it *much much much* easier to use. Otherwise, you have to use cryptic instructions like `ni`, `r`, `si`, etc to fix things.

## Web
Tools like the React extension greatly help understand what's going on in an app. This extension also includes ways to adjust the state and context, inspecting hooks, and can even be used in production apps, albeit with less detail since react-production is stripped of some information. 
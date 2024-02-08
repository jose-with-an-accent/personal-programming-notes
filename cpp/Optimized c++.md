## A bunch of C++ tips, tricks, and more
### Struct alignment
Sometimes, the alignment of a struct is suboptimal. This means that there's a lot of space that shouldn't be needed, just because of the order of fields. Consider this:
```cpp
struct Bloat {
	String s,
	char t
}
```
Because variables have to be aligned, the compiler has to add its own manual alignment. In this example, it has to make things x bytes wide, when if we reorganized things like such: 
```cpp
struct Bloat {
char t,
String s
}
```
Our program would take less memory. These are little things but they can add up, especially when trying to program videogames, real-time things, and in general trying to be a good programmer.
### Union types
Not just a performance tip, but an improvement on code, these allow us to represent the same piece of data in different ways. For example, there are many ways to represent vectors. However, unions allow us to store info in a way that can be used in multiple contexts.

### Constructors
C++ has 4 basic constructors - constructor, destructor, copy constructor, and assignment operator. We can customize each:
```cpp
class Kitchen {
	Kitchen() = void() {
	}
}
```
or use the default ones, if whatever your class is simple enough. However, even if we're using the default ones we should use ` = default;` as this tells the constructor more information that can be used to optimize things. We can also use the `delete` keyword, telling the compiler that the instruction can't be used.

### The Holy Grail: Intrinsics
Intrinsics are something annoying, but they are something that can *really* help speed up our code. These are kinda-cryptic operations that the engineers at the processor companies have figured out how to do as quick as possible, so they're architecture-specific. With these we can even process multiple bits of data in one CPU cycle (like matrixes with SIMD), so they're essential if we want to make fast or real-time code. They are at Intel's website: https://www.intel.com/content/www/us/en/docs/intrinsics-guide/index.html. Some setup is required, including in Visual Studio. A lot of these deal with vectors (matrixes), so they're especially useful for game development and graphics processing.
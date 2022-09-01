# Syntax
Angular has a bunch of special syntax to simplify things.
- ``()`` is syntax for events - for example, click, mouseDown, submit, etc. A function with ``$event`` as an argument is passed.
- ``[]`` lets us do a boolean expression - for example, ``[class.hidden]="hidden"`` hides an item when the hidden variable is set to true on the TypeScript side.
- ``*`` is used as a shorthand - for example, `*ngForOf="let movie of movies; first as first; last as last;"` lets us iterate over movies without having to set a bunch of properties. and in this case gets the current movie, and whether it's the first or last in an array.
# Decorators
Decorators are functions that add more information to code. There are a few noteworthy enough.
- ``ViewRef`` is used to get access to the a certain element's JavaScript properties and methods. add a `#name` to the HTML.
- `Input` is used to get an Angular component's properties.
- `Output` is used to hook up events, for example. 
# Best Practices
Camel Case! Make sure variables and functions are named with the first letter lowercase, and all subsequent words' first letters uppercase!
# Elm - programming language

## Pros

- No runtime errors - that's huge!
- Easy refactoring - basically because compiler will catch all errors (except the logical ones)
- Need for less tests - a lot of stuff is covered with types and a features of ML langauge
- Everything is explicit
  - No surprise where this comes from
  - but alos requires passing stuff around and adds lines of code
- Immutable
- elm-format - automatic formatting of the code

## Cons

- Slow development of the ecosystem
  - One leader to follow
    - Not safe approach
    - To much work for one guy
  - No regular updates on blog nor the libraries
- No serverside rendering
- Sometimes code is unecessary long
  - `let in` tends to spread across a lot of lines
- Acceptance testing
  - External tools are required (most likely JS tools)
  
# Resources

- http://elmprogramming.com
- https://www.elm-tutorial.org


# Unanswered questions

- How to do integration testing
- How to do acceptance testing
- How to handle 404, 301 redirects etc.
- How to do Drag&Drop
- How to Localize app
- How to handle deprecations

# Dev tips

## Working with Maybe

- Actively try to model your data structures to avoid `Maybe`
- Separate code that checks for presence from code that calculates values
- Business functions may return `Maybe`, but may not accept `Maybe` as any of it's arguments

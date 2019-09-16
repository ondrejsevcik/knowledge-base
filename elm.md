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
- "compiler driven development"

## Cons

- One leader to follow
  
# Resources

- https://guide.elm-lang.org/
- http://elmprogramming.com
- https://www.elm-tutorial.org
- https://orasund.gitbook.io/elm-cookbook/


# Unanswered questions

- How to do integration testing
- How to do acceptance testing
- How to handle 404, 301 redirects etc.
- How to do Drag&Drop
- How to Localize app

# Dev tips

- [Patterns for default values](https://discourse.elm-lang.org/t/pattern-for-default-values/3933)
- [Performant Elm](https://juliu.is/performant-elm/)

## Working with Maybe

- Actively try to model your data structures to avoid `Maybe`
- Separate code that checks for presence from code that calculates values
- Business functions may return `Maybe`, but may not accept `Maybe` as any of it's arguments

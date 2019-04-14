# Programming

- [Software Testing Anti-patterns](http://blog.codepipes.com/testing/software-testing-antipatterns.html)
- [Exceptions](https://www.joelonsoftware.com/2003/10/13/13/)
- [Workflows on Refactoring](https://www.youtube.com/watch?v=vqEg37e4Mkw)
- [Guide: Writing Testable Code](http://misko.hevery.com/code-reviewers-guide)
- [Curated list of falsehoods programmers believe in](https://github.com/kdeldycke/awesome-falsehood)
- [Design Patterns for Humans](https://github.com/kamranahmedse/design-patterns-for-humans)


## Some wisdom

> duplication is far cheaper than the wrong abstraction
> - https://www.sandimetz.com/blog/2016/1/20/the-wrong-abstraction

> Traditional organizations assume you have to work towards the best design the first time. However, it's impossible to know what a good design is unless you know all the requirements to be able to see the patterns. That process takes time. - Martin Fowler
> - https://levelup.gitconnected.com/how-to-use-technical-debt-in-your-favor-98bae475ba68?ref=hn322

> Refactoring = code transformation based on what you’ve learnt from the past
>
> Over-engineering = code transformation based on the speculation for the future.
> - https://twitter.com/tjaskula/status/977867361817694209?s=12

> Comments should describe things that are not obvious from code



> - Explicit is better than implicit.
> - Although practicality beats purity.
> - Errors should never pass silently, unless explicitly silenced.
> - There should be one-- and preferably only one --obvious way to do it.
> - If the implementation is hard to explain, it's a bad idea.
> - If the implementation is easy to explain, it may be a good idea.
> 
> [Zen of Python](https://www.python.org/dev/peps/pep-0020/#id3)


## Localization & Internationalization best practices

### Split translation files into multiple files 

TODO: WHY?

### Use unique and descriptive IDs

Ideally it should give a clear context where it's being used. 

```
# Bad
new-event = "Add new event"

# Better
calendar.month-view.add-new-event = "Add new event"
```

### Avoid concatenations, use placeholders instead

This gives translators ability to control grammar structure. It won't be `tos-text + tos-link` in every language!

```
# Wrong 
tos-text = By proceeding you accept the
tos-link = Terms of Services

# Better
tos-text = By proceeding you accept the {{link}}
tos-link = Terms of Services
```

### Don't reuse strings in different contexts

Some words have might have multiple meanings in different context, but that doesn't mean that it's the same for another lagnuages. Take `free` as an example.

### Don't hardcode characters

When you put a space at the end of the string, you can be sure that someone will eventually trim that space in translation. 

```
# Wrong
sum = "Summary: "

# Better
sum = "Summary:"
```

### Design adaptible UI

When designing the UI, keep in mind that some translated strings will be much longer than in your default language and may not fit in your designed UI. 

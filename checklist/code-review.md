# Code review checklist

> No comment should be personal. No comment should be made about the author or the reviewer. A review always must always be about the code!

🤖 things with robot head sohuld be ideally done by computer

## In general

- [ ] Are `names meaningful`?
- [ ] Are classes/functions `small enough`?
- [ ] Does the code "[read like a prose](https://www.goodreads.com/quotes/7029841-clean-code-is-simple-and-direct-clean-code-reads-like)"?
- [ ] Is the code `well-formatted`? 🤖
- [ ] Are the comments worth their existence?


## Security

- [ ] Are there any `threads`?
- [ ] Is external input handled for `XSS` properly?
- [ ] Is external input handled for `SQL injection` properly?

## Tests

- [ ] Are the tests covering all side cases?
- [ ] Do tests test one thing?
- [ ] Are they readable?

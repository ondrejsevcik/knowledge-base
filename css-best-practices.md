# CSS Best practices

Keeping CSS sane is hard. It's like having using only global variables in your code. That's why I like to follow these rules to keep it easy to work with.

Generally, I agree with everything in here https://github.com/sezgi/CSS-Best-Practices, plus I follow a few extra rules.

## Follow default [BEM naming conventions](https://en.bem.info/methodology/naming-convention)

Don't come up with some custom naming strategy. Use something that well known by a community and works very well.

## Don't use ampersand operator

In Sass, you can use ampersand operator to nest classes. 

```scss
.menu-item {
  ...
  &--selected {}
  &--visited {}
}
```

The problem is that it's hard to find. You have to search for `menu-item` and then manually see what other classes are nested. Searching for `menu-item--selected` is even more complicated (Especially if your code is in multiple repos/folders).

Keep it flat!

```scss
.menu-item {}
.menu-item--selected {}
.menu-item--visited {}
```

## Avoid concatenation of classes (selectors) in code

This is bad, it's hard to find.

```scss
.order {}
.order--open {}
.order--closed {}
```

```js
let class = "order--" + order.status;
element.classList.add(class)
```

This may be longer, but it's easier to find.

```js
switch(order.status) {
  case "open":
    element.classList.add("order--open");
    break;
  case "closed":
    element.classList.add("order--closed");
}
```

## Semantics !== visual style

When you have a `<h3>Header</h3>` it doesn't mean it should always look like a header. When you have `<a href="...` it doesn't mean it should always look like a link. Don't style elements, **always use classes**.

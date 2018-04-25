# CSS Best practices

CSS is hard. Really hard. That's why I like to follow these rules to keep it sane.

I like this short paper https://github.com/sezgi/CSS-Best-Practices. But on top of it, I add a few custom rules.

## Follow default [bem naming conventions](https://en.bem.info/methodology/naming-convention)

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

The problem here is that it's hard to find. You have to search for `menu-item` and then manually see what other classes are nested. The same comes for searching `menu-item--selected`. 

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

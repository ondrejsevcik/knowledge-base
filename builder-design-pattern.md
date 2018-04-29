# Builder design pattern

Use when your constructor has too many arguments

```c#
// Convert this
public Burger(int size, bool cheese, bool tomato...) {
  this.size = size;
  this.cheese = cheese;
  this.tomato = tomato;
  ...
}

// to this
public Burger(BurgerBuilder burgerBuilder) {
  this.size = burgerBuilder.size;
  this.cheese = burgerBuilder.cheese;
  this.tomato = burgerBuilder.tomato;
  ...
}

Burger burger = new BurgerBuilder(10).addCheese().addTomato().build();
```


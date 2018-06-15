# Regex to find Ember components with specific attribute

Finds `c-button` component with `action` attribute on it

```
\{\{#c-button(.|\n)*?action(.|\n)*?\}\}
```

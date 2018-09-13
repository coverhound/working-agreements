[Main](../../README.md) >
[Technical Guidelines and Style](../README.md)

# CSS

## Syntax

* When grouping selectors, keep individual selectors to a single line.
* Keep a whitespace after property names (like `color: #000`) and before the opening bracket (as in `.selector {` ).
* Write hexadecimal colors using downcase letters (like `color: #d2d2d2`).
* Write new selectors using `-` as a word separator rather than `_` (`section-title` instead of `section_title`).
   * **Note**: This is if we decide not to use something like [BEM](https://en.bem.info/).


## Naming Conventions

Naming conventions for classes are the major part of what a methodology like [SMACSS](https://smacss.com/), [BEM](https://en.bem.info/), or [OOCSS](https://github.com/stubbornella/oocss/tree/master/oocss) provides.

As a general rule make your classes a lot less loose by naming them a lot more specifically.

### Parent-child Relationships

The advantage of this approach is to avoid errors that may occur with similarly named objects.
```css
.profile {
  ...
}
.profile-full-name {
  ...
}
```

###  Plural Parent Pattern

Similar to parent-child relationship. Handy for containers.

```css
.columns: { ... };
.column: { ... };
```

###  Subclassing Objects

We use the same approach as OOP "An object is a kind of another object". It's useful for inheriting the properties of another object while adding additional behavior.
For sub-classes is to preceed the name of the object with the type of object.

Example:
```scss
.button {
  background: linear-gradient(#eee, #ccc);
  border: 1px solid #999;
}

.dropdown-button {
  &:hover {
    background: linear-gradient(#fff, #ddd);
    color: #111;
  }
}
```

To use it in your markup, you would apply both classes to an element, something like :

```html
<button class="button dropdown-button">
  Dropdown
</button>
```

If you prefer to only use one class in your markup, you can use the Sass `@extend` directive, as shown in the example below:

```scss
.dropdown-button {
  @extend .button;
  &::after { content: " \25BE"; }
}
```

###  Modifiers

SMACSS's naming convention of prefixing state classes is `is-.`

Example:
```scss
.button {
  background: linear-gradient(#eee, #ccc);
  border: 1px solid #999;
}

.is-hidden {
  display: none;
}
```

To use it in your markup, you would apply both classes to an element, something like :

```html
<button class="button is-hidden">
  Dropdown
</button>
```

###  Cheat Sheet

**Elements** are nouns.

```css
.noun {} /* examples: .button, .menu, .textbox, .header
```

**Parent-child** relationships are also nouns

```css
.profile-full-name { ... }
```

**Subclasses** are often proceeded by an adjective describing the type of object:

```css
.blue-text { ... }
.dropdown-button { ... }
```

**Modifier Classes** are proceeded by an `is-` following a description of their state:

```css
.is-active { ... }
.is-visible { ... }
```

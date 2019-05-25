# Best Practices

## General

- Don't use !important ever.

- Define all variables at the top of the file after the imports.

- Rule Ordering:

  - Any @ rules
  - After @ rules, alphabatical

- Use leading zeros for decimal values.

  ```css
  /* Bad example */
  opacity: 0.4;

  /* Good example */
  opacity: 0.4;
  ```

- Try to explicitly set all the property values instead of shorthand declarations if some of the property values are 0.

  ```css
  /* Bad example */
  .element {
    background: red;
    border-radius: 3px 3px 0 0;
    margin: 0 0 10px;
  }

  /* Good example */
  .element {
    background-color: red;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
    margin-bottom: 10px;
  }
  ```

## Media query

- Place media queries as close to their relevant rule sets whenever possible.

## Naming convention

- CSS class names should be lower case, hyphen separated aka "spinal case"

  ```css
  .class-name {
    /* property-name: property-value; */
  }
  ```

- Local variables should be \$snake_lowercase.

- Global constants should be \$SNAKE_ALL_CAPS

## Selectors

- Avoid using HTML tags in CSS selectors

  ```css
  /* Bad example */
  div.class-name {
    color: blue;
  }

  /* Good example */
  .class-name {
    color: blue;
  }
  ```

- When grouping selectors, keep individual selectors to a single line.

  ```css
  /* Bad CSS */
  /* prettier-ignore */
  .selector, .selector-secondary, .selector[type='text'] {
    background-color: #000;
    margin: 0px 0px 15px;
    padding: 15px;
  }

  /* Good CSS */
  .selector,
  .selector-secondary,
  .selector[type='text'] {
    background-color: #000;
    margin: 0px 0px 15px;
    padding: 15px;
  }
  ```

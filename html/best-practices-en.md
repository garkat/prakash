# Best Practices

## Dos

- Use HTML5 doctype.

  ```html
  <!DOCTYPE html>
  ```

- Specify a lang attribute on the root html element.

  ```html
  <html lang="en-us">
    <!-- ... -->
  </html>
  ```

- Quickly and easily ensure proper rendering of your content by declaring an explicit character encoding.

  ```html
  <head>
    <meta charset="UTF-8" />
  </head>
  ```

- The viewport should be set.

  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  ```

- External CSS should be added in the head tag. However, external JavaScript should be added at the bottom, just before the closing of body tag unless you need some JavaScript code to render HTML.

- Always use double quotes in stead of single quotes on attributes.

- Write HTML in lowercase. If you need to change how the text appears, you can use CSS text-transform property. The only exception to this rule is doctype (the first line of any HTML file).

- Image tag should have alt atteribute.

## Don'ts

- Inline style and/or JavaScript should never be used in an HTML page. Embedded style and/or JavaScript should be avoided as much as possible. A good use case for using embedded style is **above the fold** CSS. A good use case for embedded JavaScript could be some data to build the HTML.

- Never ever omit closing tags.

- Don’t use markup for styling. For instance, if you want to have a line break, don’t use `<br />` tag. CSS should be used for look and feel, not HTML.

- Avoid table based layout. Tables should be **only** used when we want to display tabular data.

- Boolean attribute shouldn't have a value. The presence of a boolean attribute on an element represents the true value, and the absence of the attribute represents the false value.

  ```html
  <input type="text" disabled />

  <input type="checkbox" value="1" checked />

  <select>
    <option value="1" selected>1</option>
  </select>
  ```

- Don't add unnecessay markup.

  ```html
  <!-- Not so great -->
  <span class="avatar">
    <img src="..." />
  </span>

  <!-- Better -->
  <img class="avatar" src="..." />
  ```

  Additional resources:

  - https://github.com/hail2u/html-best-practices

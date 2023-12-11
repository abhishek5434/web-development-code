# CSS: Cascading Style Sheet

CSS stands for Cascading Style Sheets. It is a style sheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

CSS provides a way to separate the structure and content of a document from its presentation, making it easier to style and design web pages. With CSS, you can control various aspects of the visual presentation, such as layout, colors, fonts, spacing, and more.

## There are three main ways to add CSS to HTML documents:
Inline, internal (or embedded), and external. Each method has its use case, and the choice often depends on factors like the scope of styling, reusability, and maintainability.

1. **Inline CSS:**
   - Inline CSS is applied directly within the HTML tags using the "style" attribute.
   - This method is suitable for making small, one-off style adjustments.
   - Example:

     ```html
     <p style="color: blue; font-size: 16px;">This is a paragraph with inline CSS.</p>
     ```

2. **Internal or Embedded CSS:**
   - Internal CSS is placed within the `<style>` tag in the `<head>` section of an HTML document.
   - This method is useful when styling is specific to a single page.
   - Example:

     ```html
     <!DOCTYPE html>
     <html lang="en">
     <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <style>
         body {
           font-family: Arial, sans-serif;
           background-color: #f0f0f0;
         }
         h1 {
           color: green;
         }
       </style>
       <title>Internal CSS Example</title>
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph with internal CSS.</p>
     </body>
     </html>
     ```

3. **External CSS:**
   - External CSS is stored in a separate file with a .css extension and linked to the HTML document using the `<link>` element.
   - This method is ideal for maintaining a consistent style across multiple pages.
   - Example:

     **styles.css:**
     ```css
     body {
       font-family: Arial, sans-serif;
       background-color: #f0f0f0;
     }
     h1 {
       color: green;
     }
     ```

     **index.html:**
     ```html
     <!DOCTYPE html>
     <html lang="en">
     <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <link rel="stylesheet" href="styles.css">
       <title>External CSS Example</title>
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph with external CSS.</p>
     </body>
     </html>
     ```

Using external CSS is generally recommended for larger projects as it promotes code organization, reusability, and easier maintenance. It also allows for caching, which can improve page load times for subsequent visits.

## CSS Selectors
CSS selectors are patterns used to select and style HTML elements. They allow you to target specific elements or groups of elements in an HTML document, so you can apply styling rules to them. CSS selectors can be based on various criteria, including element types, IDs, classes, attributes, and their relationships within the document structure.

Here are some common CSS selectors and examples:

1. **Element Selector:**
   - Selects all instances of a specific HTML element.
   ```css
   p {
     color: blue;
   }
   ```
   This selects all `<p>` (paragraph) elements and sets their text color to blue.

2. **ID Selector:**
   - Selects a specific element with a given ID.
   ```css
   #header {
     background-color: lightgray;
   }
   ```
   This selects the element with the ID "header" and sets its background color to light gray.

3. **Class Selector:**
   - Selects all elements with a given class.
   ```css
   .highlight {
     font-weight: bold;
   }
   ```
   This selects all elements with the class "highlight" and makes their text bold.

4. **Descendant Selector:**
   - Selects an element that is a descendant of another element.
   ```css
   article p {
     font-style: italic;
   }
   ```
   This selects all `<p>` elements that are descendants of an `<article>` element and sets their font style to italic.

5. **Child Selector:**
   - Selects an element that is a direct child of another element.
   ```css
   ul > li {
     list-style-type: square;
   }
   ```
   This selects all `<li>` elements that are direct children of a `<ul>` (unordered list) and sets their list style to square.

6. **Attribute Selector:**
   - Selects elements based on their attributes.
   ```css
   input[type="text"] {
     border: 1px solid #ccc;
   }
   ```
   This selects all `<input>` elements with a `type` attribute set to "text" and gives them a 1px solid border.
   - Example:
     ```HTML
     <p dr

8. **Pseudo-class Selector:**
   - Selects elements based on their state or position.
   ```css
   a:hover {
     text-decoration: underline;
   }
   ```
   This selects all `<a>` (anchor) elements when they are being hovered over and underlines their text.
   
10. **Universal selector:**
    
- The universal selector (*) in CSS is a wildcard selector that matches any element. When you use the asterisk (*) as a selector, it selects all elements on the page, applying the specified styles to every HTML element within the targeted scope.

- Here's an example of how the universal selector can be used in CSS:

```css
/* Apply a common style to all elements on the page */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```
In this example:

- `*` is the universal selector.
- The styles within the curly braces apply to all elements on the page.
- This specific example sets the margin, padding, and box-sizing properties to create a consistent box model for all elements.

While the universal selector can be useful for applying a common style reset or normalization across all elements, it should be used judiciously, as it can potentially impact performance when applied globally.

It's often a good practice to use more specific selectors whenever possible to avoid unintentional side effects. For example, if you want to style only specific elements, consider using more targeted selectors like element names, class names, or IDs instead of the universal selector.

## Difference between ID and Class Selector in CSS

In CSS, both ID selectors and class selectors are used to apply styles to HTML elements, but they have some key differences.

### ID Selector:

- **Syntax:** The ID selector is prefixed with a hash (`#`) followed by the ID name.
- **Uniqueness:** IDs must be unique within a page. You should not use the same ID for multiple elements.
- **Specificity:** ID selectors have higher specificity than class selectors, meaning that styles applied using an ID will override styles applied using a class.

**Example:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* CSS */
    #uniqueElement {
      color: red;
    }
  </style>
  <title>ID Selector Example</title>
</head>
<body>
  <p id="uniqueElement">This paragraph has a unique ID.</p>
</body>
</html>
```

### Class Selector:

- **Syntax:** The class selector is prefixed with a dot (`.`) followed by the class name.
- **Reusability:** Classes can be applied to multiple elements, allowing for greater reusability of styles.
- **Specificity:** Class selectors have lower specificity compared to ID selectors.

**Example:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* CSS */
    .highlight {
      background-color: yellow;
    }
  </style>
  <title>Class Selector Example</title>
</head>
<body>
  <p class="highlight">This paragraph has a highlighted background.</p>
  <p>This paragraph does not have a class.</p>
</body>
</html>
```

#### When to Use Each:

- Use an **ID** when the style is unique to a specific element on the page.
- Use a **class** when the style can be applied to multiple elements or when you want to group elements together and style them collectively.

**Note:** It's generally recommended to use classes more frequently than IDs to promote better reusability and maintainability of your styles. Also, excessive use of IDs can lead to a more rigid and less modular design.

## CSS properties

CSS properties are the building blocks of web design. They define the visual appearance of HTML elements, such as their color, size, font, and position. There are over 200 CSS properties available, each with its own unique effect.

### CSS Color

In CSS, the `color` property is used to set the text color of an element. It can accept a variety of color values, including named colors, hexadecimal colors, RGB values, and HSL values. Here are examples of how the `color` property can be used with different color values:

1. **Named Color:**
   - Named colors are predefined color names. Examples include `red`, `blue`, `green`, etc.
     ```css
     p {
       color: red;
     }
     ```

2. **Hexadecimal Color:**
   - Hexadecimal colors represent colors using a six-digit code. Each pair of digits represents the intensity of red, green, and blue.
     ```css
     h1 {
       color: #336699;
     }
     ```

3. **RGB Color:**
   - RGB colors specify the intensity of red, green, and blue using numerical values ranging from 0 to 255.
     ```css
     div {
       color: rgb(255, 0, 128);
     }
     ```

4. **RGBA Color:**
   - RGBA is similar to RGB but includes an additional value for the alpha channel (transparency). The alpha value ranges from 0 to 1.
     ```css
     span {
       color: rgba(0, 128, 0, 0.5);
     }
     ```

5. **HSL Color:**
   - HSL (Hue, Saturation, Lightness) colors use a cylindrical-coordinate representation. The values for hue, saturation, and lightness range from 0 to 360, 0% to 100%, and 0% to 100%, respectively.
     ```css
     a {
       color: hsl(120, 100%, 50%);
     }
     ```

6. **HSLA Color:**
   - Similar to HSL, HSLA includes an alpha channel for transparency.
     ```css
     button {
       color: hsla(240, 100%, 50%, 0.7);
     }
     ```


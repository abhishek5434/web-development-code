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

7. **Pseudo-class Selector:**
   - Selects elements based on their state or position.
   ```css
   a:hover {
     text-decoration: underline;
   }
   ```
   This selects all `<a>` (anchor) elements when they are being hovered over and underlines their text.

These are just a few examples of the many CSS selectors available. Understanding and using selectors effectively is fundamental to styling HTML documents with CSS.

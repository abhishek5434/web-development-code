# web-development-code
It has all the codes of which are being used in the udemy course.

## HTML: Hyper Text Markup Language.
-	Hyper Text is mainly hyperlink which redirects us to another page.
-	Markup Language is HTML tags.
 
### The Heading Elements:
-	We only have h1 to h6 heading tag.
-	Don’t have more than h1.
-	We should have all the header.
- Example
```HTML
<h1> Hello World </h1>
```
```txt
- < or > -- It is called angle bracket.
- <h1>-- It is called opening tag.
- </h1> -- It is called closing tag.
```
- You can go to developer.mozilla.org for the documentation of the html elements.
    
### The Paragraph Element
```HTML
<p> This is a paragraph </p>
```
-	We can use www.lipsum.com to get the random paragraph and you can copy paste from there to use in your website. It can look like a real written text.

### Void element
- ```HTML <hr /> ```
- It gives a horizontal line.
- This can also be written as
```HTML
<hr>
```

### BR Tag
- Break tag
- This can also be written as:
```HTML
<br>
<br />
```

### Unordered List
-	We need to put the items in this as well.
-	This can be used using the <ul> tag </ul>

```HTML
<ul>
<li>Milk</li>
<li>Eggs</li>
<li>Flour</li>
</ul>
```

### Ordered List
 	
-	The ordered list can be written between <ol>
```HTML
<ol>
  <li>Milk</li>
  <li>Eggs</li>
  <li>Flour</li>
</ol>
```

-	Ol in the code refers to ordered list and li refers to line items
Example:
```HTML
<ul>
<li>A</li>
<li>B
    <ol>
        <li>B1</li>
        <li>B2
            <ul>
                <li>B2a
                    <ul>
                        <li>B2aa</li>
                        <li>B2ab</li>
                    </ul>
                </li>
                <li>B2b</li>
                <li>B2c</li>
            </ul>
        </li>
        <li>B3
            <ol>
                <li>B31</li>
                <li>B32</li>
            </ol>
    </ol>
</li>
<li>C</li>
</ul>
```
### HTML attributes

The common form of writing an HTML attributes is : ``` <tag attribute=vale>Content</tag> ```

### Anchor tag
- This tag helps to embbed hyperlink into the webpage.
- The format of writing this is ```<a href = "http://www.google.com"> This is a link of Google </a>```
- In the format you can see the anchor tag starts with ```<a href=``` then takes the link and after the link we close the bracket and then we provide the content which will show in the website and after the content we close the anchor bracket.
- We can also review this website for more HTMl attributes: https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey
- **Example of anchor tag and attribute:**

```HTML
<ol start="3">
    <li><a href="https://chat.openai.com/">ChatGpt</a></li>
    <li><a href="www.theanalyticsexplorer.com"> The analytics exlorer</a></li>
    <li><a href="https://github.com/">Gith hub</a></li>
    <li><a href="www.claude.ai">Claude</a></li>
    <li><a href="www.geeksforgeeks.com">geeksforgeeks</a></li>
</ol>
```

Result:
<ol start="3">
    <li><a href="https://chat.openai.com/">ChatGpt</a></li>
    <li><a href="www.theanalyticsexplorer.com"> The analytics exlorer</a></li>
    <li><a href="https://github.com/">Gith hub</a></li>
    <li><a href="www.claude.ai">Claude</a></li>
    <li><a href="www.geeksforgeeks.com">geeksforgeeks</a></li>
</ol>


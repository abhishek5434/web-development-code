# web-development-code
It has all the codes of which are being used in the udemy course.

![image](https://github.com/abhishek5434/web-development-code/assets/86175919/ecdee888-e192-4478-89ad-e157a4c558ec)


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
- ``` <hr /> ```
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

### Image element
- It does not have closing tag and hence it is also a void element
- This is the simple form of code: ```<img src="url" />```
- We can pick the random image from picsum.photos url
- Do use the alt attribute in this img tag since it can help the user who wants to listen the website via reader
- Here is one example:
```HTML
<img src="https://picsum.photos/200" alt="This is just an example" />
```
**Result:**

<img src="https://picsum.photos/200" alt="This is just an example"/>

Simple project using all the above concepts:

```HTML
<h1>It's my birthday today !</h1>
<h2>On the 1st July</h2>
<img src="https://gifocard.com/en/b/03/a/happy-birthday.gif.pagespeed.ce.EFmm7_XCG_.gif" alt="This is birthday cake"/>
<h3>What to bring:</h3>
<ul>
    <li>Baloons</li>
    <li>Cake</li>
    <li>A gift</li>
</ul>

<h3>This is where you need to go</h3>
<a href="https://maps.app.goo.gl/rLruqpyaKND2s5oG7">Google map link</a>
```
Result:
<h1>It's my birthday today !</h1>
<h2>On the 1st July</h2>
<img src="https://gifocard.com/en/b/03/a/happy-birthday.gif.pagespeed.ce.EFmm7_XCG_.gif" alt="This is birthday cake"/>
<h3>What to bring:</h3>
<ul>
    <li>Baloons</li>
    <li>Cake</li>
    <li>A gift</li>
</ul>

<h3>This is where you need to go</h3>
<a href="https://maps.app.goo.gl/rLruqpyaKND2s5oG7">Google map link</a>

### Relative and Absolute path
**Absolute path**
- An absolute path provides the full and exact location of a file or directory from the root directory.
- Example: ```C:\Users\User\Documents\example.txt```

**Relative path**
- A relative path specifies the location of a file or directory in relation to the current working directory.
- It does not start from the root directory; instead, it assumes a starting point and provides a path from that point.
- Relative paths are often more convenient for specifying locations within the same project or directory structure.
- Example 1 showing picking file from the same directory: ```./documents/example.txt```
- Example 2 showing picking file from the different directory: ```../images/picture.jpg```

We can link an url inside a picture like this:
```HTML
<a href="./public/about.html"> <img src="../../Pic with victor.png" alt="My picture with Victor"/></a>
```
### The HTML Boilerplate

```HTML
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Page Title</title>
    <!-- Add your additional meta tags, stylesheets, or scripts here -->
</head>

<body>
    <!-- Your content goes here -->
    <h1>Hello, World!</h1>

    <!-- Add your HTML content, such as paragraphs, images, links, etc. -->

    <!-- Add your scripts or additional content at the end of the body if needed -->

</body>

</html>
```


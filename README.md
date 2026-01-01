<h1>CSS Selectors</h1>
CSS Selectors are used to target HTML elements on your pages, allowing you to apply styles based 
on their ID, class, type attributes, and more. There are mainly 5 types of selectors.'

<h2>Basic Selectors</h2>
Basic selectors in CSS are simple tools used for selecting by HTML element name (e.g., h1), 
class (.class Name), ID (#idName), or universally (* for all elements).

1. Universal Selector (*): Selects all elements on the page and applies the same style universally. 
For example, setting the font color for every element.

```
<html>
<head>
  <style>
    * {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Header Text</h1>
  <p>Paragraph Text</p>
</body>
</html>
```

2. Element Selector: Targets all elements of a specific type, such as paragraphs or headers. 
For example, setting a common font size for all paragraphs.

```
<html>
<head>
  <style>
    p {
      font-size: 16px;
    }
  </style>
</head>
<body>
  <p>This paragraph styled with font size 16px.</p>
</body>
</html>
```

3. Class Selector (.): Applies styles to elements with a specific class attribute. For instance, 
making all buttons have a blue background.

```
<html>
<head>
  <style>
    .button {
      background-color: blue;
      color: white;
    }
  </style>
</head>
<body>
  <button class="button">Click Me!</button>
</body>
</html>
```

4. ID Selector (#): Styles a single element identified by its unique id. For example, changing 
the background color of a header.

```
<html>
<head>
  <style>
    #header {
      background-color: gray;
    }
  </style>
</head>
<body>
  <div id="header">This is the header section.</div>
</body>
</html>
```

<h2>Combinator Selectors</h2>
Used to define relationships between selectors, allowing you to style elements based on their 
hierarchy or positioning in the document. Common combinators include descendant ( ), child (>), 
adjacent sibling (+), and general sibling (~).

1. Descendant Selectors: Targets an element inside another, such as paragraphs inside div .For 
example, styling paragraphs inside a div.

```
<html>
<head>
  <style>
    div p {
      color: red;
    }
  </style>
</head>
<body>
  <div>
    <p>This paragraph inside a div will be red.</p>
  </div>
</body>
</html>
```

2. Child Selector (>): They only affects the direct child elements of a parent. For example, styling 
direct children paragraphs of a div.

```
<html>
<head>
  <style>
    <div>p {
      margin-left: 20px;
    }
  </style>
</head>
<body>
  <div>
    <p>This is a direct child and has a left margin.</p>
    <div>
      <p>This is not a direct child.</p>
    </div>
  </div>
</body>
</html>
```

3. Adjacent Sibling Selector (+): Styles an element immediately following another .For example, 
making the first paragraph bold after an h1.

```
<html>
<head>
  <style>
    h1+p {
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>This is a header.</h1>
  <p>This is immediately following the header and is bold.</p>
  <p>This will not be bold.</p>
</body>
</html>
```

4. General Sibling Selector (~): Styles all siblings that follow a specific element. For 
example, italicizing all paragraphs following an h1.

```
<html>
<head>
  <style>
    h1~p {
      font-style: italic;
    }
  </style>
</head>
<body>
  <h1>This is a header.</h1>
  <p>This is a sibling of the header and will be italicized.</p>
  <p>This will also be italicized because it's a sibling of the header.</p>
</body>
</html>
```

<h2>Attribute Selectors</h2>
Attribute selectors in CSS target elements based on the presence or value of their attributes. 
Examples include [attr] (selects elements with the attribute), [attr="value"] (matches specific 
values), and [attr^="val"] (matches values starting with "val").


1. Presence Selector: It selects elements that contain a specific attribute. For example, styling all 
inputs with a type attribute.

```
<html>
<head>
  <style>
    input[type] {
      border: 2px solid black;
    }
  </style>
</head>
<body>
  <input type="text" placeholder="Text input">
  <input type="number" placeholder="Number input">
</body>
</html>
```

2. Attribute Value Selector: It targets elements with a particular attribute value. For example, 
styling text inputs.

```
<html>
<head>
  <style>
    input[type="text"] {
      background-color: yellow;
    }
  </style>
</head>
<body>
  <input type="text" placeholder="Text input">
  <input type="password" placeholder="Password input">
</body>
</html>
```

3. Substring Matching(^=): It matches elements where the attribute contains a substring. For 
example, styling links with https in their href.

```
<html>
<head>
  <style>
    a[href^="https"] {
      color: green;
    }
  </style>
</head>
<body>
  <a href="https://example.com/">Secure link</a>
  <a href="http://example.com/">Non-secure link</a>
</body>
</html>
```

4. Wildcard Selector (*=): Matches elements where the attribute value contains a specific string. 
For example, underlining links with example in the URL.

```
<html>
<head>
  <style>
    a[href*="example"] {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <a href="https://example.com/">This contains 'example' and is underlined.</a>
  <a href="https://otherlink.com">This is not underlined.</a>
</body>
</html>
```

<h2>Pseudo-Classes</h2>
Pseudo-classes in CSS define the special states of elements for styling. Examples include :hover 
(applies when an element is hovered), :first-child (targets the first child of a parent), and 
:nth-child(2) (targets the second child).

1. :hover: Styles elements when the user hovers over them. For example, changing the color of a 
link when hovered.

```
<html>
<head>
  <style>
    a:hover {
      color: red;
    }
  </style>
</head>
<body>
  <a href="https://example.com/">Hover over this to see the effect.</a>
</body>
</html>
```

2. :focus: Styles the elements when the user focus on any particular element.

```
<html>
<head>
  <style>
    input:focus {
      outline: 3px solid red;
    }
  </style>
</head>
<body>
  <input type="text">
</body>
</html>
```

3. :first-child: Styles the element which is the first child of it's parent.

```
<html><head></head>
<style>
  p:first-child {
    color: brown;
  }
</style>
<body>
  <div>
    <p>Hello1</p>
    <p>Hello2</p>
  </div>
</body></html>
```

4. :last-child: Style's the element which is the last child of it's parent.

```
<html><head></head>
<style>
  p:last-child {
    color:green;
  }
</style>
<body>
  <div>
    <p>Hello1</p>
    <p>Hello2</p>
  </div>
</body></html>
```

5. :not: Helps to remove a particular element from the styling index or styling context.

```
↔​
        color: blue;
    }
</style>
<body>
  <div>
↔​
```

<h2>Pseudo-Elements</h2>
The Pseudo Element help's to access and control a specific part of an element for inserting content 
before an element or inserting content after an element. Targeting any specific part of a word or 
a sentence. It is usually used to beautify the internal content of an element.

1. ::before: It helps to insert some content before an element.

```
<html><head></head>
<style>
  h1::before {
    content: "★ "
  }
</style>
<body>
  <h1 tabindex="0">Welcome to GFG</h1>
</body></html>
```

2. ::after: It help's to insert some content after an element.

```
<html><head></head>
<style>
  h1:active::before {
    content: "☀ ";
    color: orangered;
  }
</style>
<body>
  <h1 tabindex="0">Welcome to GFG</h1>
</body></html>
```

3.::first-line: Styles the first line of text within a block element. Line breaks mark the 
beginning of a new line.

```
<html><head></head>
<style>
  p::first-line {
    color: red;
  }
</style>
<body>
  <p>Welcome to GFG<br>
    Hello GFG</p>
</body>
</html>
```

4. ::first-letter: It Styles the first-letter of a word or a sentence.

```
<html><head></head>
<style>
  p::first-letter {
    color: red;
    font-size: 23px;
  }
</style>
<body>
  <p>Welcome to GFG</p>
</body></html>
```

5. ::placeholder: Styles the placeholder of a specific input field.

```
<html><head></head>
<style>
  input::placeholder {
    font-size: 20x;
    font-family: sans-serif;
    font-weight: 900;
  }
</style>
<body>
  <input type="text" placeholder="Enter your name">
</body></html>
<html><head></head>
<style>
  input::placeholder {
    font-size: 20x;
    font-family: sans-serif;
    font-weight: 900;
  }
</style>
<body>
  <input type="text" placeholder="Enter your name">
</body></html>
```


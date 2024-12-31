# Tables Using HTML 

Table has an external border, header rows and header cell, body rows and its cells and it could have also a footer row. To make an HTML table, we need a _table_ element that wrap all the rows and the rows wrap all the data cells.


## Basic HTML Table Syntax

The basic structure of an HTML table includes the following elements:

- `<table>`: Wraps the entire table.
- `<tr>`: Represents a table row.
- `<th>`: Represents a header cell (bold and centered by default).
- `<td>`: Represents a data cell.

### syntax:

```html
<table>
  <!-- first row -->
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <!-- Second row -->
  <tr>
    <td>Row 1, Col 1</td>
    <td>Row 1, Col 2</td>
    <td>Row 1, Col 3</td>
  </tr>
  <!-- Third row -->
  <tr>
    <td>Row 2, Col 1</td>
    <td>Row 2, Col 2</td>
    <td>Row 2, Col 3</td>
  </tr>
</table>

```
### Example

```html
<table>
  <tr>
    <td>Name</td>
    <td>Gender</td>
    <td>Country</td>
  </tr>
  <tr>
    <td>Nardos</td>
    <td>Female</td>
    <td>Ethopia</td>
  </tr>
</table>
```
# Multimedia Elements in HTML

## What Are Multimedia Elements?
Multimedia elements in HTML allow you to embed and control media files, such as audio and video, directly within a webpage. The two most commonly used multimedia elements are `<audio>` for audio files and `<video>` for video files. These elements make it easy to include multimedia content without relying on third-party plugins.

## 1. The `<audio>` Element
The `<audio>` element is used to embed audio content, such as music, sound effects, or voice recordings.

### Basic Syntax:
```html
<audio src="path/to/audio.mp3">
    Your browser does not support the audio element.
</audio>
```
### Attributes:

- `src`: Specifies the path to the audio file.
- `controls`: Adds built-in playback controls (play, pause, volume).
- `autoplay`: Automatically starts playing the audio when the page loads.
- `loop`: Makes the audio loop after it finishes playing.
- `muted`: Mutes the audio.

Example:
```html
<audio src="audio/music.mp3">
    Your browser does not support the audio element.
</audio>
```
You can provide multiple sources for better browser compatibility using the `<source>` tag.
```html
<audio controls>
    <source src="audio/music.mp3" type="audio/mp3">
    <source src="audio/music.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>
```
__Purpose__: Offers fallback options for browsers that support different audio formats.

## 2. The `<video>` Element
   
  The `<video>` element is used to embed video content, such as movies, animations, or video tutorials.

### Basic Syntax:
 ```html
 <video src="path/to/video.mp4">
    Your browser does not support the video element.
</video>
```
### Attributes:
- `src`: Specifies the path to the video file.
- `controls`: Adds built-in playback controls (play, pause, volume, fullscreen).
- `autoplay`: Automatically starts playing the video when the page loads.
- `loop`: Makes the video loop after it finishes playing.
- `muted`: Mutes the video.
- `poster`: Displays an image before the video starts playing.
 
 Example:
 ```html
 <video src="video/sample.mp4" controls>
    Your browser does not support the video element.
</video>
```
Just like with audio, you can use `<source>` to specify different video formats for compatibility:
```html
<video controls>
    <source src="video/sample.mp4" type="video/mp4">
    <source src="video/sample.ogv" type="video/ogv">
    <source src="video/sample.webm" type="video/webm">
    Your browser does not support the video element.
</video>
```


# `<input>` Tag and Its Types

The `<input>` element in HTML is used to create interactive controls for web forms. It allows users to input data. The `type` attribute specifies the type of input field to display.

Below are the common types of `<input>` and their uses, along with examples:

---

## 1. Text Input
Used for single-line text input.

```html
<input type="text" name="username" placeholder="Enter your username">
```

## 2. Password Input
Used for entering passwords. The characters are obscured.

```html
<input type="password" name="password" placeholder="Enter your password">
```

## 3. Email Input
Used for email addresses. It validates the input as a properly formatted email.
```html
<input type="email" name="email" placeholder="Enter your email">
```
## 4. Number Input
Used for numeric inputs. You can specify min, max, and step values.
```html
<input type="number" name="age" min="1" max="100" step="1">
```
## 5. Date Input
Used to select a date from a calendar.

```html
<input type="date" name="birthdate">
```
## 6. Checkbox Input
Used for selecting one or more options.
```html
<label>
  <input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
</label>
```
## 7 Radio Button input
used for selecting a single option from multiple choices.
```html
<label>
  <input type="radio" name="gender" value="male"> Male
</label>
<label>
  <input type="radio" name="gender" value="female"> Female
</label>
```
## 8. File Input
Used for uploading files.
```html
<input type="file" name="profilePicture">
```
## 9. Color Input
Used for selecting a color from a color picker.
```html
<input type="color" name="favoriteColor">
```
## 10. Submit Button
used to submit a form.
```html
<input type="submit" value="Submit">
```
### In addition learn more about in [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)







# HTML Form Elements

HTML forms are used to collect user input. They contain various form elements like text fields, checkboxes, radio buttons, and more. Below is a detailed explanation of the most common form elements with examples.

---

## 1. `<form>` Element
The `<form>` tag defines an HTML form and serves as a container for input elements. It requires attributes like `action` (where to send data) and `method` (HTTP method to use).

```html
<form action="/submit" method="post">
  <!-- Form elements go here -->
</form>
```

The `action` and `method` attributes are key components of an HTML `<form>` element, determining where and how form data is submitted. Here's an explanation of each:
### 1. The action Attribute
The `action` attribute specifies the URL where the form data should be sent once the form is submitted.

```html
<form action="URL">
  <!-- Form content -->
</form>
```
#### URL can be an absolute or relative path:
- ***Absolute URL***: The full path to a server (`e.g., https://example.com/submit`).

- ***Relative URL***: A path relative to the current page (e.g., `/submit`).

### Example
```html
<form action="https://example.com/submit" method="post">
  <input type="text" name="username" placeholder="Enter your name">
  <input type="submit" value="Submit">
</form>
```
When the user submits this form, the data is sent to `https://example.com/submit`.
### 2. The method Attribute
The method attribute specifies the HTTP method used to send the form data to the server.

Common Values:

***1.`GET`:***

- Appends form data to the URL as query parameters.
- Data is visible in the browser's address bar.
- Suitable for non-sensitive data or bookmarking.

### Example:
```html
<form action="/search" method="get">
  <input type="text" name="q" placeholder="Search">
  <input type="submit" value="Search">
</form>
```
Submitting the form might result in a URL like:
`https://example.com/search?q=search-term.`

***2.`POST`***:

- Sends form data in the HTTP request body.
- Data is not visible in the URL.
- Suitable for sensitive or large amounts of data

### Example:
```html  
<form action="/search" method="post">
  <input type="text" name="q" placeholder="Search">
  <input type="submit" value="Search">
</form>
````
# Block vs Inline Elements in HTML

## What are Block Elements?
Block elements are HTML elements that occupy the full width of their container, meaning they take up the entire horizontal space available. They are typically used to structure the layout of a webpage. When a block element is placed on the page, it starts on a new line and forces subsequent elements to appear below it.

### Characteristics of Block Elements:
- They take up the full width of their container by default (unless otherwise specified).
- They always start on a new line, stacking vertically.
- They can have width, height, margins, and padding applied to them.
- Block elements can contain other block and inline elements.

### Common Block Elements:
- `<div>`: A generic container element.
- `<header>`: Defines the header of a document or section.
- `<footer>`: Represents the footer of a document or section.
- `<section>`: Groups related content into sections.
- `<article>`: Represents a self-contained content piece, like a blog post.
- `<p>`: Defines a paragraph of text.
- `<ul>` and `<ol>`: Defines unordered and ordered lists.
- `<h1>`, `<h2>`, `<h3>`, etc.: Define headings of various levels.

### Example:
```html
<div>
    <h1>Welcome to My Website</h1>
    <p>This is a block-level element.</p>
</div>
```
## What are Inline Elements?
Inline elements do not start on a new line. They only take up as much width as necessary to fit their content. Inline elements are typically used for small parts of a document, such as text formatting, links, or images.

Characteristics of Inline Elements:

- They only occupy the space they need to display their content, i.e., they do not force the next element to a new line.
- Inline elements cannot have width or height set explicitly (though padding, margin, and border can be applied to them).
- Inline elements can only contain other inline elements or text, not block elements.
  
Common Inline Elements:

- `<a>`: Defines a hyperlink.
 - `<span>`: A generic inline container for text or other inline elements.
- `<strong>`: Defines important text, often rendered as bold.
- `<em>`: Defines emphasized text, often rendered as italic.
- `<img>`: Embeds an image.
- `<b>`: Represents bold text (though `<strong>` is preferred for meaning).
- `<i>`: Represents italicized text (though - - - `<em>` is preferred for meaning).
Example:
```html
<p>This is <a href="#">an inline link</a> within a block-level paragraph.</p>

```
# Page Structure
![My Image](img/Web%20Development%20programing%20tricks%20and%20tips%20for%20beginners%20free.jpg)

## Semantic Tag and Non-semantic tag
![Semantic Tag](img/What%20is%20an%20HTML%20Semantic%20Tag.jpg)

## Understanding the `<div>` Element in HTML

The `<div>` element is a versatile and commonly used HTML tag. It stands for "division" and is primarily used as a container to group other HTML elements. This grouping allows developers to style, position, or manipulate sections of a webpage collectively.

## Key Features of `<div>`:
1. **Block-level Element**: The `<div>` tag is a block-level element, meaning it starts on a new line and stretches across the page horizontally by default.
2. **No Semantic Meaning**: Unlike tags like `<header>` or `<footer>`, the `<div>` element does not convey any semantic meaning. It is purely for structural and styling purposes.
3. **Customizable**: The `<div>` element is often assigned `class` or `id` attributes, making it easy to apply CSS styles or JavaScript functionality.

## Common Uses of `<div>`:
 **Layout and Structure**:
   - Used to create sections or containers in a webpage for better organization.
   - For example, dividing a webpage into a header, main content, and footer.

   ```html
   <div class="header">Header Section</div>
   <div class="main-content">Main Content</div>
   <div class="footer">Footer Section</div>
```

## When to Use `<div>`
 - When you need a general-purpose container without semantic meaning.
- When grouping elements for styling or scripting.
- Avoid overusing `<div>` if __semantic elements__ would provide better clarity and accessibility.

# Semantic Elements in HTML

Semantic elements in HTML are those that clearly define their meaning and purpose in a web page's structure and content. They improve the readability of the code for developers and enhance accessibility for assistive technologies like screen readers. 

Semantic elements also help search engines understand the content better, which can improve SEO (Search Engine Optimization).

## Examples of Semantic Elements:
### Common Semantic Tags:
- `<header>`: Represents a page or section header.
- `<nav>`: Defines a navigation menu.
- `<main>`: Represents the main content of the document.
- `<section>`: Groups related content, typically with its own heading.
- `<article>`: Represents a self-contained piece of content, such as a blog post or news article.
- `<aside>`: Represents content related to the main content, like a sidebar.
- `<footer>`: Represents the footer of a document or section.
- `<figure>` and `<figcaption>`: Used for images with captions.

### Examples:

#### 1. **Using `<header>`**
```html
<header>
    <h1>Welcome to My Website</h1>
    <p>Your one-stop resource for coding tutorials.</p>
</header>
```
__Purpose__: Contains the page's main heading and a tagline.
#### 2. **Using `<nav>`**
```html
<nav>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>
```
__Purpose__: Defines a navigation menu.
#### 3. **Using `<section>`**
```html
<section>
    <h2>Latest News</h2>
    <p>Stay updated with the latest trends in technology.</p>
</section>
```
__Purpose__: Groups content into a distinct section, often with its own heading
#### 4. **Using `<article>`**
```html
<article>
    <h3>How to Learn JavaScript</h3>
    <p>JavaScript is an essential language for modern web development...</p>
</article>
```
__Purpose__: Represents a self-contained piece of content that can stand alone.
#### 5. **Using `<footer>`**
```html
<footer>
    <p>&copy; 2024 My Website. All Rights Reserved.</p>
</footer>
```
__Purpose__: Contains copyright information and closing content.

# Understanding ID and Class in HTML

## What is an ID in HTML?
An `id` is a unique identifier for an HTML element. It is used to identify a single element on the page and can be used in CSS, JavaScript, or for linking to a specific part of a page.

### Key Features of `id`:
- **Unique**: The `id` attribute must be unique within the HTML document. No two elements can have the same `id`.
- **Singular**: An element can only have one `id` at a time.
- **Case-sensitive**: The `id` attribute is case-sensitive (e.g., `#header` is different from `#Header`).
- **Used in CSS and JavaScript**: You can reference an `id` in CSS to style a specific element, or in JavaScript to interact with it.

### Example of Using ID:
```html
<div id="header">This is the header</div>
<p id="intro">This is an introduction paragraph.</p>
```

## What is a Class in HTML?
A `class` is used to group multiple HTML elements together that share common styles or behavior. Unlike `id`, a `class` can be assigned to multiple elements on the same page, allowing you to apply the same style to many elements.

Key Features of class:

- Non-unique: Multiple elements can share the same class, making it easier to apply common styles to groups of elements.
- Reusable: You can use the same class across different elements on the page.
- Flexible: An element can have multiple classes (separated by spaces).
- Used in CSS and JavaScript: Just like id, classes can be used to style elements and to interact with them in JavaScript.
  
### Example of Using Class:
```html
<div class="content">This is content 1</div>
<div class="content">This is content 2</div>
```
## Differences Between ID and Class

| Feature              | ID                                    | Class                                |
|----------------------|---------------------------------------|--------------------------------------|
| **Uniqueness**        | Must be unique in the document.       | Can be used for multiple elements.   |
| **Usage**             | Used to identify a single element.    | Used for grouping similar elements.  |
| **Syntax**            | `id="elementId"`                      | `class="className"`                  |
| **CSS Selector**      | `#elementId`                          | `.className`                         |
| **JavaScript Access** | `document.getElementById()`           | `document.getElementsByClassName()`  |

# Introduction to CSS (Cascading Style Sheets)

## What is CSS?
CSS (Cascading Style Sheets) is a stylesheet language used to control the presentation (layout, colors, fonts, spacing, etc.) of HTML elements. CSS enhances the look and feel of web pages by separating the content (HTML) from its design (CSS). 

Without CSS, a webpage would be just plain text and images with minimal structure. CSS allows developers to create visually appealing and user-friendly web designs.

## Key Features of CSS:
1. **Separation of Content and Style**: CSS keeps the structure of the page (HTML) separate from its presentation (CSS), making web pages easier to maintain.
2. **Responsive Design**: CSS enables web pages to adjust their layout based on the screen size, device, and orientation, creating a better user experience on desktops, tablets, and smartphones.
3. **Styling Flexibility**: With CSS, you can modify a range of properties like colors, fonts, margins, padding, and positioning to create a visually cohesive design.
4. **Efficient Styling**: CSS allows you to apply styles globally or to specific elements, reducing the need to repeat code.

## Basic Syntax of CSS:
A CSS rule is composed of:
- **Selector**: Specifies which HTML element the style applies to.
- **Declaration**: Defines the property and value of the style.

### Example:
```CSS
selector{
    property: value;
}
```


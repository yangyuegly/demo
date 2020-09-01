---
title: "Building Your First Static Site with Plain HTML"
date: 2020-09-01T15:19:11-04:00
draft: false
---

## **What Are HTML & CSS?**

*HTML*, HyperText Markup Language, gives content structure and meaning by defining that content as, for example, headings, paragraphs, or images. *CSS*, or Cascading Style Sheets, is a presentation language created to style the appearance of content—using, for example, fonts or colors.

The two languages—HTML and CSS—are independent of one another and should remain that way. CSS should not be written inside of an HTML document and vice versa. As a rule, HTML will always represent content, and CSS will always represent the appearance of that content.

With this understanding of the difference between HTML and CSS, let’s dive into HTML in more detail.

## **Understanding Common HTML Terms**

Three common HTML terms you should begin with are *elements*, *tags*, and *attributes*.

### **Elements**

Elements are designators that define the structure and content of objects within a page. Some of the more frequently used elements include multiple levels of headings (identified as `<h1>` through `<h6>` elements) and paragraphs (identified as the `<p>` element); the list goes on to include the `<a>`, `<div>`, `<span>`, `<strong>`, and `<em>` elements, and many more.

Elements are identified by the use of less-than and greater-than angle brackets, `< >`, surrounding the element name. Thus, an element will look like the following:

```html
<a>
```

### **Tags**

The use of less-than and greater-than angle brackets surrounding an element creates what is known as a *tag*. Tags most commonly occur in pairs of opening and closing tags.

An *opening tag* marks the beginning of an element. It consists of a less-than sign followed by an element’s name, and then ends with a greater-than sign; for example, `<div>`.

A *closing tag* marks the end of an element. It consists of a less-than sign followed by a forward slash and the element’s name, and then ends with a greater-than sign; for example, `</div>`.

The content that falls between the opening and closing tags is the content of that element. An anchor link, for example, will have an opening tag of `<a>` and a closing tag of `</a>`. What falls between these two tags will be the content of the anchor link.

So, anchor tags will look a bit like this:

```html
<a>...</a>

```

### **Attributes**

*Attributes* are properties used to provide additional information about an element. The most common attributes include the `id` attribute, which identifies an element; the `class` attribute, which classifies an element; the `src` attribute, which specifies a source for embeddable content; and the `href` attribute, which provides a hyperlink reference to a linked resource.

Attributes are defined within the opening tag, after an element’s name. Generally attributes include a name and a value. The format for these attributes consists of the attribute name followed by an equals sign and then a quoted attribute value. For example, an `<a>` element including an `href` attribute would look like the following:

```html
<a href="http://shayhowe.com/">Shay Howe</a>
```

**Common HTML Terms Demo**

The preceding code will display the text “Shay Howe” on the web page and will take users to http://shayhowe.com/ upon clicking the “Shay Howe” text. The anchor element is declared with the opening `<a>` and closing `</a>` tags encompassing the text, and the hyperlink reference attribute and value are declared with `href="http://shayhowe.com"` in the opening tag.

![https://learn.shayhowe.com/assets/images/courses/html-css/building-your-first-web-page/html-syntax-outline.png](https://learn.shayhowe.com/assets/images/courses/html-css/building-your-first-web-page/html-syntax-outline.png)

**Fig 1** HTML syntax outline including an element, attribute, and tag

Now that you know what HTML elements, tags, and attributes are, let’s take a look at putting together our first web page. If anything looks new here, no worries—we’ll decipher it as we go.

## **Setting Up the HTML Document Structure**

HTML documents are plain text documents saved with an `.html` file extension rather than a `.txt` file extension. To begin writing HTML, you first need a plain text editor that you are comfortable using. Sadly this does not include Microsoft Word or Pages, as those are rich text editors. Two of the more popular plain text editors for writing HTML and CSS are Dreamweaver and Sublime Text. Free alternatives also include Notepad++ for Windows and TextWrangler for Mac.

All HTML documents have a required structure that includes the following declaration and elements: `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`.

The document type declaration, or `<!DOCTYPE html>`, informs web browsers which version of HTML is being used and is placed at the very beginning of the HTML document. Because we’ll be using the latest version of HTML, our document type declaration is simply `<!DOCTYPE html>`. Following the document type declaration, the `<html>` element signifies the beginning of the document.

Inside the `<html>` element, the `<head>` element identifies the top of the document, including any metadata (accompanying information about the page). The content inside the `<head>` element is not displayed on the web page itself. Instead, it may include the document title (which is displayed on the title bar in the browser window), links to any external files, or any other beneficial metadata.

All of the visible content within the web page will fall within the `<body>` element. A breakdown of a typical HTML document structure looks like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>DATA1050</title>
  </head>
  <body>
    <h1>Create your first static site</h1>
    <p>With plain HTML.</p>
  </body>
</html>

```

### **HTML Document Structure Demo**

The preceding code shows the document beginning with the document type declaration, `<!DOCTYPE html>`, followed directly by the `<html>` element. Inside the `<html>` element come the `<head>` and `<body>` elements. The `<head>` element includes the character encoding of the page via the `<meta charset="utf-8">` tag and the title of the document via the `<title>` element. The `<body>` element includes a heading via the `<h1>` element and a paragraph via the `<p>` element. Because both the heading and paragraph are nested within the `<body>` element, they are visible on the web page.

When an element is placed inside of another element, also known as nested, it is a good idea to indent that element to keep the document structure well organized and legible. In the previous code, both the `<head>` and `<body>` elements were nested—and indented—inside the `<html>` element. The pattern of indenting for elements continues as new elements are added inside the `<head>` and `<body>` elements.

### **Self-Closing Elements**

In the previous example, the `<meta>` element had only one tag and didn’t include a closing tag. Fear not, this was intentional. Not all elements consist of opening and closing tags. Some elements simply receive their content or behavior from attributes within a single tag. The `<meta>` element is one of these elements. The content of the previous `<meta>` element is assigned with the use of the charset attribute and value. Other common selfclosing elements include

- `<br>`
- `<embed>`
- `<hr>`
- `<img>`
- `<input>`
- `<link>`
- `<meta>`
- `<param>`
- `<source>`
- `<wbr>`

The structure outlined here, making use of the `<!DOCTYPE html>` document type and `<html>`, `<head>`, and `<body>` elements, is quite common. We’ll want to keep this document structure handy, as we’ll be using it often as we create new HTML documents.

### **Code Validation**

No matter how careful we are when writing our code, we will inevitably make mistakes. Thankfully, when writing HTML and CSS we have validators to check our work. The W3C has built both [HTML](https://validator.w3.org/) and [CSS](https://jigsaw.w3.org/css-validator/) validators that will scan code for mistakes. Validating our code not only helps it render properly across all browsers, but also helps teach us the best practices for writing code.

## **In Practice**

1. Let’s open our text editor, create a new file named `index.html`, and save it to a location we won’t forget. I’m going to create a folder on my Desktop named “styles- conference” and save this file there; feel free to do the same.
2. Within the index.html file, let’s add the document structure, including the `<!DOCTYPE html>` document type and the `<html>`, `<head>`, and `<body>` elements.

    ```html
    <!DOCTYPE html>
    <html lang="en">
      <head>
      </head>
      <body>
      </body>
    </html>

    ```

3. Inside the `<head>` element, let’s add `<meta>` and `<title>` elements. The `<meta>` element should include the proper charset attribute and value, while the `<title>` element should contain the title of the page—let’s say “Styles Conference.”

    ```html
    <head>
      <meta charset="utf-8">
      <title>Styles Conference</title>
    </head>
    ```

4. Inside the `<body>` element, let’s add `<h1>` and `<p>` elements. The `<h1>` element should include the heading we wish to include—let’s use “Styles Conference” again—and the `<p>` element should include a simple paragraph to introduce our conference.

    ```html
    <body>
      <h1>Styles Conference</h1>
      <p>Every year the brightest web designers and front-end developers descend on Chicago to discuss the latest technologies. Join us this August!</p>
    </body>

    ```

5. Now it’s time to see how we’ve done! Let’s go find our index.html file (mine is within the “styles-conference” folder on my Desktop). Double-clicking this file or dragging it into a web browser will open it for us to review.


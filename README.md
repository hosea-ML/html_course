# HTML Crash Course

My notes and practice code from the HTML crash course. This project is a small multi-page website made of three linked pages:

| Page | Purpose |
| --- | --- |
| `index.html` | Home page with all the main HTML building blocks (headings, text, links, lists, form, image) |
| `about.html` | "About us" page with a link back to the home page |
| `contact.html` | "Contact" page |

## What I Learned

### 1. Document Structure

Every HTML page starts with the same skeleton:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML crash course</title>
  </head>
  <body>
    <!-- visible content goes here -->
  </body>
</html>
```

- `<!doctype html>` tells the browser this is an HTML5 document.
- `<head>` holds metadata (character encoding, viewport, page title). It is not shown on the page.
- `<body>` holds everything the user sees.
- Comments are written as `<!-- comment -->`.

### 2. Headings

`<h1>` to `<h6>` give six levels of headings, from most to least important.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<!-- ... down to <h6> -->
```

### 3. Paragraphs and Text Formatting

| Tag | Purpose |
| --- | --- |
| `<p>` | A paragraph of text |
| `<b>` | Bold text |
| `<i>` | Italic text |
| `<span>` | A generic inline wrapper, useful for styling part of a line later with CSS |

```html
<p>Land a job with <span>ASAP Frontend</span></p>
```

### 4. Links (Anchors)

The `<a>` tag creates links using the `href` attribute.

```html
<a href="about.html">Hello</a>                                  <!-- another page in my project -->
<a href="https://asapfrontend.com" target="_blank">Asap frontend</a>  <!-- external site, opens in a new tab -->
```

- Relative paths (`about.html`) link to files in the same project.
- Full URLs link to other websites.
- `target="_blank"` opens the link in a new tab.

**Linking between my own pages:** `index.html` links to `about.html` and `contact.html`, and `about.html` links back home:

```html
<!-- in about.html -->
<h1>About us page</h1>
<a href="index.html">Back to html file</a>
```

`contact.html` currently has just a heading (`<h1>Contact page</h1>`).

### 5. Lists

**Unordered list** (bullets) with `<ul>`:

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>
```

**Ordered list** (numbered) with `<ol>`:

```html
<ol>
  <li>Usain Bolt</li>
  <li>Ronaldo</li>
</ol>
```

Each item in both list types is an `<li>`.

### 6. Forms

Forms collect input from users. Each field is wrapped in a `<div>` with a `<label>` and an `<input>`.

| Element | Type / Purpose |
| --- | --- |
| `<input type="text">` | Single-line text (with a `placeholder` hint) |
| `<input type="email">` | Email address |
| `<input type="password">` | Hidden characters |
| `<input type="number">` | Numbers only |
| `<input type="date">` | Date picker |
| `<textarea>` | Multi-line text, such as a message |
| `<select>` + `<option>` | Dropdown menu (for example sizes S, M, L, XL) |
| `<button>` | Submit or click button |

```html
<form action="">
  <div>
    <label for="">First Name</label>
    <input type="text" placeholder="Type in your first name" />
  </div>

  <div>
    <label for="">Sizes</label>
    <select name="" id="">
      <option value="S">S</option>
      <option value="M">M</option>
    </select>
  </div>

  <button>Submit</button>
</form>
```

### 7. Images

```html
<img src="assets/images/RingoNG_Logo.png" alt="RingoNG_Logo" />
```

- `src` is the path to the image file.
- `alt` is the text description. It is shown if the image fails to load and is read by screen readers.

## Project Structure

```
html_course/
├── index.html
├── about.html
├── contact.html
└── assets/
    └── images/
        └── RingoNG_Logo.png
```

## How to Run

1. Clone or download this project.
2. Open `index.html` in any web browser (or use the VS Code Live Server extension).
3. Use the links to move between the home, about, and contact pages.

## Next Steps

Things I want to improve and learn next:

- [ ] Connect each `<label>` to its input using matching `for` and `id` attributes, so clicking the label focuses the field.
- [ ] Add `name` attributes to form inputs so the data can actually be submitted.
- [ ] Use semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) instead of only `<div>`.
- [ ] Use `<strong>` and `<em>` instead of `<b>` and `<i>` when the text carries emphasis or importance.
- [ ] Learn CSS to style the page.
- [ ] Learn JavaScript to make the page interactive.

## Resources

- [MDN Web Docs: HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [ASAP Frontend](https://asapfrontend.com)

# Box Model

![Boxmodel](img/box-model.png)

Explanation of the different parts:

- Content - The content of the box, where text and images appear
- Padding - Clears an area around the content. The padding is transparent
- Border - A border that goes around the padding and content
- Margin - Clears an area outside the border. The margin is transparent

The box model allows us to add a border around elements, and to define space between elements. 

# Display

## Block-level Elements

A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

The &lt;div> element is a block-level element.
Examples of block-level elements:

```HTML
<div>
<h1> - <h6>
<p>
<form>
<header>
<footer>
<section>
```

## Inline Elements
An inline element does not start on a new line and only takes up as much width as necessary.

This is an inline &lt;span> element inside a paragraph.

Examples of inline elements:

```HTML

<span>
<a>
<img>

```

## Display: none;

display: none; is commonly used with JavaScript to hide and show elements without deleting and recreating them. Take a look at our last example on this page if you want to know how this can be achieved.

The &lt;script> element uses display: none; as default. 

# The float Property

The float property is used for positioning and formatting content e.g. let an image float left to the text in a container.

The float property can have one of the following values:

- left - The element floats to the left of its container
- right - The element floats to the right of its container
- none - The element does not float (will be displayed just where it occurs in the text). This is default
- inherit - The element inherits the float value of its parent

In its simplest use, the float property can be used to wrap text around images.

# Flexbox

[W3Schools Flexbox](https://www.w3schools.com/css/css3_flexbox.asp)

---

# Skipulag vefsíðu - webpage layout

### Viðmið (_Breakpoints_)

#### "Mobile up"

```CSS

body {
background-color: blue;
color: white;
}

@media only screen and (min-width: 37.5em) {  /* skjáir (screen) sem eru stærri en 37.5em (600px) */
  body {
    background-color: lightblue;
  }
}

@media only screen and (min-width: 48em) {  /* skjáir (screen) sem eru stærri en 48em (768px) */
  body {
    background-color: green;
  }
}

@media only screen and (min-width: 60em) {  /* skjáir (screen) sem eru stærri en 60em (960px) */
  body {
    background-color: red;
	max-width: 60em;
	margin: 0 auto;
	border: 2px solid yellow;
  }
}

``` 
### Grid skipulag með _grid-area_

```HTML

<!DOCTYPE html>
<html>
<head>
<style>
.item1 { grid-area: header; }
.item2 { grid-area: menu; }
.item3 { grid-area: main; }
.item4 { grid-area: right; }
.item5 { grid-area: footer; }

.grid-container {
  display: grid;
  grid-template-areas:
    'header header header header header header'
    'menu   main   main   main   right  right'
    'menu   footer footer footer footer footer';
  grid-gap: 10px;
  background-color: #2196F3;
  padding: 10px;
}

.grid-container > div {
  background-color: rgba(255, 255, 255, 0.8);
  text-align: center;
  padding: 20px 0;
  font-size: 30px;
}
</style>
</head>
<body>

<h1>Grid Layout</h1>

<p>This grid layout contains six columns and three rows:</p>

<div class="grid-container">
  <div class="item1">Header</div>
  <div class="item2">Menu</div>
  <div class="item3">Main</div>  
  <div class="item4">Right</div>
  <div class="item5">Footer</div>
</div>

</body>
</html>


```



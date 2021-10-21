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



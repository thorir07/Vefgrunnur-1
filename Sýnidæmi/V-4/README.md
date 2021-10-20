# Svegjanleg hönnun

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

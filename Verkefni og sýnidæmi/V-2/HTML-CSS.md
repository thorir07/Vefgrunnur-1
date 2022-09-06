# Uppsetning HTML vefsíðu 

(*án innihalds*)

```HTML

<!DOCTYPE html><!-- Nýasta útgáfa HTML. Ef yfilýsingin er ekki tekin fram notar vafrinn 4. útgáfuna -->
<html lang="is">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- Hér kemur efni sem birtist í vafra (browser) -->
</body>
</html>

``` 

Mundu að eftirfarandi þarf ávallt að vera til staðar í HTML skjali:

-   **\<!DOCTYPE HTML\>** tilgreinir hvaða útgáfu af HTML staðli vafrinn
    á að nota, þetta er HTML 5 skilgreining.

-   **\<html skipunum\>** á alltaf að loka með **\</\...\>** og enda
    skjalið **\</body\>\</html\>** undantekningar eru nokkrar t.a.m. **\<meta\>, \<img\>,\<br\>, \<hr\> og \<input\>**

-   Vistið skjalið með endingunni **.html** til að hægt sé að opna það í
    vafra (browser).

-   Það má **EKKI hafa** **íslenska stafi** í heiti skjalsins eða hafa
    **stafabil** í heitinu.

-   Þú skoðar html síðuna í vafra með því að smella á html skjalið þar
    sem þú vistaðir það.

________________________________________________________

# CSS stílsetning

![css selector](img/selector.gif)

Valtag (_selector_) bendir á HTML þáttinn (_element_) sem þú vilt stíla.

Hver skipun inniheldur eigindi og gildi.

Valtagið inniheldur eina eða fleiri skipanir sem eru aðgreindar með semikommum.

Margar CSS skipanir eru aðgreindar með semikommum og þær eru umvafðar með slaufusviga.

Dæmi:

```CSS

.header h1 {
    color: #fff;
    line-height: 1.2;
    font-weight: normal;
}

```

#### Stílsíða tengd við HTML vefsíðu

```HTML
    <!--link er í head taginu -->
    <link rel="stylesheet" type="text/css" href="styles.css">

```
#### Vefsíður tengdar saman \<a\> 

```HTML
    <a href="sida2.html" title="Síða 2">Síða 2</a>
```
#### Anchor Pseudo-classes \<a\>

```CSS
    /* unvisited link */
    a:link {
        color: #FF0000;
    }

    /* visited link */
    a:visited {
        color: #00FF00;
    }

    /* mouse over link */
    a:hover {
        color: #FF00FF;
    }

    /* selected link */
    a:active {
        color: #0000FF;
    }
```

[Sjá nánar á w3schools](https://www.w3schools.com/css/css_pseudo_classes.asp)

#### Gildum hlaðið á eigindi 

```CSS

div {
	margin: 10px 20px 30px 40px; 
	   /*-top(1) -right(2) -bottom(3) -left(4) 
	   á bæði við margin og padding */
	
	padding: 10px 20px; 
		/*top+bottom og left+right 
		á bæði við margin og padding */
	
	border: 5px solid #f0f; 
	        /*-weight, -style, -color */
	/* 7 gildi eru í border-style: solid, dotted, dashed, double, ridge, inset, outset,*/
	/*ath! að veja aðeins eitt gildi á border-style:*/
}

```



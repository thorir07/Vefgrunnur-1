# Verkefni 3

### Myndvinnsla og innsetning mynda í vefsíðu

Í **images** möppunni eru nokkrar myndir sem á að setja í vefsíðu eins og sýnt er á næstu síðu. Það þarf að breyta stærð myndanna í myndvinnsluforriti þannig að þær séu þjappaðar í  réttri stærð og fljótar að hlaðast inn á vefsíðuna. Það má nota aðrar myndir ef þú villt.

### 3.1 Stór forsíðumynd 

Myndin er vistuð í fjórum stærðum og vafrinn velur rétta stærð miðað breidd skjásins. 
Viðmið: [0 - 30em] – [30 - 48em] – [48 - 80em] – [80em +]

### 3.2 Myndaröð 
6 myndir eru vistaðar í sömu stærð og þeim raðað mismunandi upp í vefsíðu eftir breidd skjásins

---

#### Myndir í bakgrunni vefsíðu

```CSS

body {
    background-color: #6ff;
    background-image:url(flott-logo.svg);
    background-repeat: no-repeat;     /* repeat-x eða repeat-y */
    background-position: 200px 300px; /* föst staðsetning frá vinstra horni efst */
    background-position: center middle;
    /* X lárétt: left, center, right. Y lóðrétt: top, middle, bottom */
    background-attachment: fixed; /* scroll */	
}
body {			
	background: rgb(3,3,3) url(image.jpg) 0px -5px scroll no-repeat;
            /*  litur,   mynd,  staðsetning X-Y,  fixed,  repeat -x -y */

}

```

#### Myndvinnsluforrit

* Photopea  er forrit (app) sem keyrir í vafra.
* Myndir skornar:  Toolbar -> Crop Tool
* Myndir settar í rétta stærð: Image -> Canvas size.
* Þjöppun fyrir vef  í Photopea  -> Export -> .jpg eða .png
* *Gimp er myndvinnsluforrit sem hægt er að hlaða inn í tölvuna þína ókeypis.
* Myndir skornar: Tools -> Transform Tools -> Crop
* Myndir settar í rétta stærð: Image -> scale image.

* Vefmyndir geta verið þjappaðar saman í .jpg (kb). 
* Myndir í .png formati geta verið með gagnsæjan (transparent) bakgrunn og 5% þjöppun
* Myndir í .gif formati geta verið með gagnsæjan (transparent) bakgrunn og 0% þjöppun
* Myndir sem settar eru á vefsíðuna eiga ekki að vera stærri en stærðin sem myndin birtist í tölvuksjá (max 2000px breidd). Með <picture> taginu er hægt að sortera myndir eftir skjábreidd
Í stílsíðu er mikilvægt er að hafa eftirfarandi grunnstillingu á öllum myndum 

---

# Myndvinnsla

Stafræn mynd er framsetning myndar í tvíundakerfi og getur verið annaðhvort vigur- (_vector_) eða rastamynd (_bitmap_). Yfirleitt á heitið „stafræn mynd“ við rastamynd. Stafrænar ljósmyndavélar og skannar geta búið til rastamyndir. Til að búa til einfalda vigurmynd getum við kóðað hana en oftast notum við hönnunarforrit til að teikna myndina. 

#### Þrenns konar gerðir rastamynda er hægt að setja í vefsíður.

* .jpg – _Joint Photographic Experts Group_. JPEG þjöppun hentar vel fyrir ljósmyndir. JPEG er “_lossy_” þjöppunartækni þar sem m.a. upplýsingar sem mannsaugað greinir ekki eru þjappaðar. .jpg format hentar best fyrir ljósmyndir og flóknari grafík. Eftir því sem myndin er þjöppuð meira því óskýrari verður hún. Hönnuðurinn þarf því að velja á milli gæða myndarinnar og stærðar hennar.
* .png – _Portable Network Graphics_. .png myndir eru svipaðar .gif myndum en bjóða uppá meiri myndgæði. Þjöppun án taps í 24 bita RGB lit. .png getur þjappað 5-25% og hefur möguleika á gagnsæjum bakgrunni.
* .gif – _Graphic Image File_. Gif formatið hentar vel fyrir einfalda grafík en síður fyrir ljósmyndir. Gif myndir hafa mest 256 lita upplausn og taplausa LZW þjöppun. Gif myndir geta verið með litlausan (transparent) bakgrunn. 

#### Myndvinnsluforrit

#### _Adobe Photoshop_

* .psd – skjal er eingöngu notað í Photoshop forritinu. Með því að vista myndir sem .psd er hægt að halda áfram að vinna með myndina í fullum litgæðum. 
* .eps – _Encapsulated PostScript_ og .tiff _Tagged Image File Format_ eru bæði hægt að opna í Photoshop, vinna með og uppfæra fyrir vefinn sem .jpg mynd eða .png mynd.
* .pdf – Portable document format, það er hægt að opna .pdf skjal í Photoshop og vista aftur sem .pdf skjal. 

#### _Gimp_ myndvinnsluforrit (_ókeypis, MAC og PC_)

* .XCF myndaskrár eru búnar til GIMP myndvinnsluforritinu og þær er hægt að uppfæra fyrir vefinn sem .jpg mynd eða .png myndir. 
*  [Það er hægt að opna .psd mynd í Gimp](https://www.howtogeek.com/362162/how-to-open-or-convert-a-photoshop-file-if-you-dont-have-photoshop/)
* Eftirtalin forrit geta unnið með .XCF myndir: _IrfanView, XnView, Inkscape, Paint.NET, CinePaint, digiKam, Krita og Seashore_. 

#### PaintNet (Windows PC) 

#### [Photopea](https://www.photopea.com/) (Vafraforrit - App)

#### Portable Document File .pdf

Pdf skjal er form á skjali, sem er hannað til að standa fyrir önnur skjöl óháð öllum þeim tölvubúnaði sem notaður var til að búa til skjalið. Þegar pdf skjal er opnað, lítur það eins út hvar sem þú opnar það. Ólík stýrikerfi eða skjáupplausn skipta ekki máli. Þessi skjöl geta verið ein blaðsíða, eða þúsundir blaðsíðna, einföld, eða mjög flókin. Pdf skjal getur innihaldið hvaða samsetningu sem er af texta, grafík og myndum. 

#### Vigurteikningar, Vektor myndir .svg

* Til að birta vektor mynd í vafra þarf hún að vera vistuð sem .SVG mynd (_Scalable Vector Graphic_). 
* Teikningar og firmamerki eru unnin í vektorteikniforitum eins og _Adobe Illustrator, InkScape og Corel Draw_. 

Athugið að þetta **er ekki** tæmandi listi yfir myndgerðir sem hægt er að vinna með og yfirfæra í myndvinnsluforritum.
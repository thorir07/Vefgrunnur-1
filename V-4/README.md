# Verkefni 4 

### Leturgerð – Font family

Finndu þér málefni sem þú villt fjalla um, það má vera hvað sem er* td getur þú farið á Vísindavef HÍ til að finna umfjöllunarefni. 

*Athugið að kennari þarf að samþykkja greinina.  

Sækið leturgerðir á Google font vefsíðuna .  Setjið mismunandi stíla á fyrirsögn, millifyrirsagnir og meginmálsletur, tengla, lista.  Leturgerð og litaval á að hæfa efnisinnihaldi vefsíðunnar. Vefsíðan á að vera sveigjanleg, letur og myndir eiga að birtast eðlilega í öllum skjástærðum. 
Skoðaðu hvernig val á leturgerð hefur áhrif á upplifun notandans.  

* Passar leturgerðin sem þú velur, málefninu?  
* Hentar litaþemað sem þú hefur valið, málefninu?

[Dæmi um grein þar sem aðaláherslan er á leturnotkun]()

---

# Leturstillingar í CSS

```CSS

body {
    font-style: normal;      /* italic , obligue */
    font-weight: normal;     /* bold , 100 - 900 */
    font-size: 1em;          /* 1px , 1rem , 100% */
    line-height: 1.5;         /* tekur mið af einingunni sem er á font-size, staðlað 1.3 */
    font-family: Helvetica, sans-serif; 
    /* vafrinn tekur Helvetica ef það er til, annars system font (sans-serif) */ 
}

/* hér er öllum stílum sópað saman í eina skipun "font:"*/
body {
    font:italic bold 100%/120% Georgia, Times, serif;
    /*font-style, -weight, -size/-lineheight -family */
}



```
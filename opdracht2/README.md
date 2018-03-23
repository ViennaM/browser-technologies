# Browser Technologies
//Robuuste, toegankelijke websites leren bouwen …

[Hamburger](https://viennam.github.io/browser-technologies/opdracht2/hamburger.html)

[Modal](https://viennam.github.io/browser-technologies/opdracht2/modal.html)

## Hamburger
De eerste feature is een navigatie die verandert naar een hamburger icoon, zodra het scherm in de breedte kleiner wordt. Als je op de hamburger drukt, verschijnt het menu.

### Werking
Het hamburger menu is opgebouwd uit drie lagen: html, css, js.
- De navigatie zonder css en js wordt in html weergegeven als lijst.
- Zonder js, wordt het hamburger icoon niet weergegeven, maar is de navigatie wel responsive.
- Zonder css, wordt de button niet in de html geladen door javascript.

Het icoon wordt dus met javascript ingeladen en de navigatie is altijd beschikbaar in html.

#### Feature detection
Javascript wordt alleen uitgevoerd, wanneer de functie `classList` beschikbaar is op de desbetreffende browser en wanneer er css beschikbaar is:
`if (nav && nav.classList && document.getElementsByTagName('style').length === 1)`



## Opdracht 2 - 1, 2, 3 Feature Detectie
//Wat laat je zien als een browser of gebruiker 'enhancement' niet kan tonen of zien? Hoe doe je Feature Detection en wat doe je als een techniek niet werkt?

Werk 2 componenten uit in een demo. Je onderzoekt hoe je verschillende features door verschillende browsers worden ondersteund en hoe je voor goede fallback kan zorgen. Gebruik [html5test.com](https://html5test.com), [css3test.com](http://css3test.com) en [kangax.github.io/compat-table/es6/](https://kangax.github.io/compat-table/es6/)

- Per feature: Zoek uit hoe je deze kunt testen. Verzamel uitleg en artikelen. Bouw een (kleine) progressive enhanced demo (zonder extra tools, gewoon in 1 HTML file, zo simpel mogelijk). Test de feature (en fallback) op verschillende browsers en het Device Lab. Let op: Gebruik van polyfills is niet toegestaan.
- Post je 2 demo’s op GitHub met uitleg in een README file. Wat is de feature? Welke browsers/devices ondersteunen deze wel/niet? Hoe zorg je dat de fallback nuttig is?

Beoordelingscriteria
- 2 componenten zijn onderzocht en er is een demo gemaakt.
- De code staat in een repository op GitHub.
- Een Readme is toegevoegd met, per feature:
  -	Een beschrijving van de feature.
  - Bronnen van uitleg en gebruikte artikelen.
  -	Welke browsers/devices ondersteunen deze wel/niet.
  -	Een beschrijving hoe de fallback werkt.

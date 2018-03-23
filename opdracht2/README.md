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

## Modal
De modal is in dit geval een pop-up, die getriggerd wordt door op een link te klikken. 

### Werking
- De modal wordt zonder css en js weergegeven onder de tekst. Door middel van een anchor link scroll je naar de tekst bij het klikken op de link.
- Zonder css is de modal niet zichtbaar, totdat je op de link klikt. Hierbij is de tekst ook te verbergen.
- Zonder js wordt de modal getriggerd met de css `:target` selector.

### Feature detection
Net zoals bij de hamburger feature, wordt er gecheckt of de `classList` functie beschikbaar is: `if (modal && open && modal.classList)`


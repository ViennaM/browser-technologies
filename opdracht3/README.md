# Opdracht 3 - Progressive Enhanced Browser Technologies
Browser Technologies onderzoeken en implementeren als enhancement. Basic functionaliteit van een use case doorgronden.

![Contactenlijst screenshot](images/screenshot.png)

## Contactenlijst
Demo: [https://viennam.github.io/browser-technologies/opdracht3/](https://viennam.github.io/browser-technologies/opdracht3/ "Contactenlijst demo")

De use case waarvan ik een demo heb gemaakt is de contactenlijst. De core functionaliteit hiervan is het filteren en bekijken van details van een contact.

### Features / Browser Technologies

**Features:**
- Toetsenbordvriendelijk
- Zoeken naar een contact
- Responsive


**Browser Technologies:**
- Progressive enhancement (HTML > CSS > JS)
- Details / summary fallback ([bron](https://github.com/tyleruebele/details-shim))

### Werking

![Contactenlijst werking](images/werking.png)

De demo is opgebouwd uit drie lagen: HTML, CSS en JavaScript.

- Zonder JavaScript worden contacten in een lijst weergegeven met het alfabet aan de zijkant om te zoeken op achternaam.
- Zonder CSS is het mogelijk om de contactenlijst te filteren met behulp van een zoekfunctie. 
- Zonder JavaScript en CSS is het mogelijk om contacten op achternaam te zoeken met behulp van anchor links.

### User experience

![User experience](images/ux.png)

In de demo heb ik rekening gehouden met toegankelijkheid voor slechtzienden. Ik heb bijvoorbeeld een 'skip to content' link en focus states toegevoegd voor toetsenbordgebruikers. Het contrast heb ik getest met de [Funkify](http://www.funkify.org/) extensie.

### Feature detection

Om ervoor te zorgen dat JavaScript geen errors geeft, heb ik een feature detection toegevoegd die checkt of de functies die ik gebruik in mijn code wel beschikbaar zijn in desbetreffende browser. Zo niet, dan wordt het script niet uitgevoerd. Dit doe ik met de volgende code:

```
var element = document.createElement('_')
var string = ''
var arr = []
if ('querySelectorAll' in document 
    && 'classList' in element 
    && typeof string.replace === 'function' 
    && typeof arr.includes ===
      'function') {
  // code...
}
```

### Browser ondersteuning

**Browsers**
![Browsers](images/browsers.png)
Aangezien Internet Explorer de HTML tags details en summary nog niet ondersteunt, heb ik getest of de [fallback](https://github.com/tyleruebele/details-shim) wel werkt. Blijkbaar werkt het vanaf IE9. Navigeren op alfabet is nog wel mogelijk.

**Mobiele devices**
![Mobiele devices](images/mobiel.png)
Met behulp van [BrowserStack](https://www.browserstack.com/) heb ik op een aantal mobiele devices getest. Opvallend is dat op de meeste devices JavaScript in de browser wordt ondersteund. Op bijvoorbeeld Nokia Lumia 930 is de details / summary fallback toegepast, ook al wordt de zoekfunctie niet ondersteund.

### To do
- [ ] Contactenlijst server side serveren
- [ ] Contacten kunnen toevoegen / wijzigen / verwijderen
- [ ] Feedback wanneer er geen contacten zijn gevonden

Maak een demo op basis van een use case. Zorg dat alle gebruikers, met alle browsers, in iedere context minimaal de core functionaliteit te zien/horen/voelen krijgen. Bouw je demo in 3 lagen, volgens het principe van Progressive Enhancement. Gebruik als enhanced feature een (hippe, innovatieve, vooruitstrevende) Browser Technologie die je gaat onderzoeken op functionaliteit, toegankelijkheid en (browser) ondersteuning.

## Bronnen

[details-shim](https://github.com/tyleruebele/details-shim)

[Funkify](http://www.funkify.org/)

[BrowserStack](https://www.browserstack.com/)

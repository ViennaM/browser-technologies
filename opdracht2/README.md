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

Het icoon wordt dus met javascript ingeladen en de navigatie is altijd beschikbaar in html.

### Feature detection
#### ClassList
`ClassList` is pas vanaf IE10 deels ondersteund. Om `classList` te kunnen gebruiken, heb ik er een check omheen gezet. Wanneer `classList` niet beschikbaar is, gebruik ik `className`.

```javascript
var nav = document.getElementById('navigation')
if (menu.classList) {
  menu.classList.add('hide');
} else {
  menu.className = 'hide'
}
```
#### AddEventListener
`AddEventListener` wordt pas vanaf IE9 ondersteund. Deze functie vervang ik met `attachEvent` wanneer `addEventListener` niet wordt ondersteund. Ook check ik of `attachEvent` beschikbaar is, omdat deze functie tot IE10 is ondersteund.
```javascript
if (typeof document.addEventListener === 'function') {
  hamburger.addEventListener('click', toggleMenu);
} else if (typeof document.attachEvent === 'function'){
  hamburger.attachEvent('onclick', toggleMenu);
}
```

**Bronnen**

- [https://caniuse.com/#search=addeventlistener](https://caniuse.com/#search=addeventlistener)


## Modal
De modal is in dit geval een pop-up, die getriggerd wordt door op een link te klikken. 

### Werking
- Zonder css en js opent de link een nieuwe pagina met de algemene voorwaarden.
- Met css en zonder js wordt er ook een nieuwe pagina geopend.
- Met js en zonder css worden de algemene voorwaarden onder de link weergegeven. In chrome wordt de modal wel weergegeven, met behulp van het `dialog` element.

### Feature detection
##### Dialog
Het `dialog` element wordt niet ondersteund in alle browsers. Om het element toch als modal te laten functioneren, moeten de tags vervangen worden door een tag die de desbetreffende browser wel ondersteunt. In dit geval `div`.

```javascript
if ("open" in document.createElement('dialog')) {
  // use dialog.open
}
else {
  // replace tags
}
  ```

#### CSS transform
CSS 2D transform wordt in oudere browsers niet ondersteund. Hierdoor zal de modal uit het beeld verdwijnen, omdat `left: 50%;` en `top: 50%;` wel werken. Om dit te voorkomen, detecteer ik of transform beschikbaar is. ([bron](https://stackoverflow.com/a/12625986/6445473))

```javascript
var transformCheck = function () {
  var prefixes = 'transform WebkitTransform MozTransform OTransform msTransform'.split(' ');
  var div = document.createElement('div');
  for (var i = 0; i < prefixes.length; i++) {
    if (div && div.style[prefixes[i]] !== undefined) {
    return prefixes[i];
    }
  }
  return false;
}
```

#### AddEventListener 
Ook AddEventListener wordt niet in elke browser ondersteund. De volgende code gebruik ik om bijvoorbeeld `preventDefault()` uit te voeren op de anchor tags. 

```javascript
if (typeof document.addEventListener === 'function') {
  // preventDefault()
}
```

**Bronnen**

- [https://caniuse.com/#search=dialog](https://caniuse.com/#search=dialog)

- [https://caniuse.com/#search=transform](https://caniuse.com/#search=transform)

- [https://stackoverflow.com/a/12625986/6445473](https://stackoverflow.com/a/12625986/6445473)
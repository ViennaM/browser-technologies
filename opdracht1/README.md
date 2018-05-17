# Opdracht 1.1

## Breedband

### Wat is breedband?
Een snelle verbinding is niet altijd vanzelfsprekend. Je hebt namelijk meestal geen snelle verbinding. Dit kan problemen opleveren voor de user experience. Je moet er dus rekening mee houden tijdens development. In dit onderzoek beschrijf ik de problemen die het zou kunnen opleveren, wat wij als developers eraan zouden kunnen doen en hoe je kunt testen of je er goed genoeg rekening mee hebt gehouden.

**Problemen**

Eventuele problemen van websites geoptimaliseerd voor breedband:
- Wifi in openbare ruimtes (hotels)
- 3G verbinding
- Datalimiet

**Oplossingen**

Voorbeelden van oplossingen voor bovenstaande problemen:
- Geef jezelf een richtlijn (performance budget)
- Compress afbeeldingen
- Voeg critical CSS toe

**Testen**
- Network throttling in DevTools
- Performance test via tools
	- [http://www.webpagetest.org/](http://www.webpagetest.org/)
	- [https://developers.google.com/speed/pagespeed/insights/](https://developers.google.com/speed/pagespeed/insights/)

#### Bronnen

[http://www.webpagetest.org/](http://www.webpagetest.org/)

[https://developers.google.com/speed/pagespeed/insights](https://developers.google.com/speed/pagespeed/insights/)

[https://en.wikipedia.org/wiki/Bandwidth_throttling](https://en.wikipedia.org/wiki/Bandwidth_throttling)

[https://timkadlec.com/2013/01/setting-a-performance-budget/](https://timkadlec.com/2013/01/setting-a-performance-budget/)


## Trackpad

Ook je muis of trackpad heeft invloed op de user experience. Websites horen bruikbaar te zijn zonder muis of trackpad, omdat niet iedereen die wil gebruiken. Soms is het zelfs sneller om een website te gebruiken zonder.

### Problemen

Eventuele problemen van muis of trackpad:
- Motorische beperkingen
- Lege batterijen 
- Smart tv besturing

### Oplossingen

Voorbeelden van oplossingen:
- Focus states (CSS)
- Semantische HTML
- Accesskeys
- Eventueel ARIA labels

#### Bronnen

[https://www.w3schools.com/tags/att_global_accesskey.asp](https://www.w3schools.com/tags/att_global_accesskey.asp)

[https://www.washington.edu/accessibility/checklist/focus/](https://www.washington.edu/accessibility/checklist/focus/)

### Opdracht 1.2 - Fork je OBA
Hoe zit het eigenlijk met Progressive Enhancement van je OBA opdracht? Waarschijnlijk kan daar wel het één en ander aan verbeterd worden, dat ding is immers in een week in elkaar gehackt!

Voor deze opdracht ga je toepassen wat je van opdracht 1.1 hebt geleerd.
- Pas Progressive enhancement toe op je OBA Web App.
- Check je OBA Web App op de 8 features uit opdracht 1.1 en verbeter de code waar mogelijk.
- Test  je OBA Web App in het device lab.
- Laat je OBA Web App voorlezen door een screenreader.
- Gebruik onderstaande artikelen om je code te optimaliseren.
[The accessibility mindset](https://24ways.org/2015/the-accessibility-mindset/) en [Accessibility Originates With UX: A BBC iPlayer Case Study](https://www.smashingmagazine.com/2015/02/bbc-iplayer-accessibility-case-study/)

Beoordelingscriteria
- Zet je code op Github
- Schrijf een Readme met:
  - een beschrijving van de problemen die je hebt gevonden
  - beschrijf hoe je de problemen hebt opgelost
  - of hoe je dit zou oplossen (met todo’s) als je genoeg tijd en budget zou hebben

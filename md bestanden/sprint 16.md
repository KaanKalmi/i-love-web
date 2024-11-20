# Sprint 16 - Don't repeat yourself
### Sprint planning
Dit gaat over component libraries en quality assurance

### wat is een component libraary
> Een component library is een verzameling UI-elementen, zoals het ontwerp van knoppen, de selectie van lettertypen en andere typografische en visuele elementen. ~Google

Een verzameling vooraf gemaakte, geteste en goed gedocumenteerde Ul-componenten die eenvoudig kunnen worden hergebruikt in de gebruikersinterface van een product.
Het zorgt ervoor dat het product een consistente uitstraling en gevoel heeft en bevordert efficiëntie en schaalbaarheid.
Met componentenbibliotheken kunnen ontwerpers en ontwikkelaars snel nieuwe functies en pagina's toevoegen, terwijl de algehele ontwerpconsistentie en kwaliteit behouden blijft.

### Deeltaak component building block
De focus ligt op 't ontwerpen en bouwen van een robuust, goed werkend component, waarin de belangen van de eindgebruiker centraal staan.

### identificeer jouw componenten
analyseer je website en identificeer componenten

### Maak een morphological chart en breakdown
Maak een chart op een A3 (mag ook digitaal) om een analyse te maken van je component e zijn onderdelen

Het is een soort chart waarin je de eisen op een rij zet en dus opties erbij zet

Je moet minstens 8 variaties voor je component maken en werk drna de verschillende versies uit in figma. 
 
## Advanced Component Concepts

We’re not designing pages, Designing systems of components.
 
### Dont repeat yourself component library
Een verzameling herbruikbare en generieke componenten die je aan een project kunt toevoegen, er bestaan vele standaard component libraries die je kunt downloaden en gebruiken.

Het gebruik van een component library:
- Versnelt ontwikkeling door hergebruik
- Consistentie in projecten
- Vergroten van onderhoudbaarheid
 
### Nadelen:
- Grotere kans op fouten
- Alles ziet er hetzelfde uit
- Vergroot de chaos
 
### Afspraken over conventies:
- Naamgeving van componenten
- Naamgeving van variaties van componenten
- Naamgeving van properties binnen componenten
- Metanaamgeving: componenten, patronen, etc.
Indeling van de $lib folder
 
### Metanaamgeving is:
een hiërarchische benadering om het over bepaalde soorten componenten te hebben.
In Principe is alles componenten, maar hoe noemen we:…..
  
Manieren hoe je structuur kunt brengen aan je werk
 
### Page-Section-Component
- Pages: volledige pagina’s of schermen met een specifieke context bestaand uit sections, bijvoorbeeld homepage.
- Sections: secties van een pagina bestaand uit componenten, bijvoorbeeld een hero-banner
- components:…
 
### Functional Layering
- inputs: componenten voor gebruiksinvoer
- Display: componenten voor het weergeven van informatie
- Navigation: componenten voor navigatie, menus, Breadcrumps
- Structure: layout-elementen die structuur bieden, grids, containers.
 
### Lego
- Bricks: kleine, niet herbruikbare stukjes, een icoon of tekstblok
- Blocks: herbruikbare basis componenten, een knop of een afbeelding
- Assemblages: gecombineerde componenten met een specifieke functie, formulier of kaart
- Construction: complexe pagina sections of templates, dashboard
 
### Atomic Design: geschikt voor grote projecten:
- Atoms
- Molecules
- Organism
- Templates
- Pages
 
### Presenter-Container:
- Presentational components
- Container components
- Compositions
 
### Component Library
Atomic design is  een methode om design systems te creëren.
 
Terwijl je aan het werk bent, probeer svelte 5 features toe te passen (als je de tijd voor hebt, moet niet)
Kijk goed naar de documentatie van Svelte.


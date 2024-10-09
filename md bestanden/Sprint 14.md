## Sprint planning
### Sprint 14

Doel v/d sprint: Omarmen van de JAMstack
- Javascript
- Api's
- Markup

Twee groepen technologieen die onder het paraplubegrip JAMstack valt:
- Site generators
- Headless CMS

Jamstack is een manier om websites en webapplicaties te bouwen die sneller, veiliger en schaalbaarder zijn.
Het doet dit door de ervaringslaag van het web los te koppelen van de gegevens en bedrijfslogica.
Hierdoor bevat de ervaringslaag alleen nog maar statische HTML, CSS en JavaScript die zeer snel kan worden geladen.
Gegevens en bedrijfslogica worden opgeslagen in een aparte laag, die ontsloten wordt via APIs.

Jamstack maakt het mogelijk een modulaire architectuur te implementeren.
Het voordeel hiervan is dat verschillende delen van een website of webapplicatie kunnen worden gebouwd en onderhouden door verschillende teams.
Dit maakt het veel eenvoudiger om websites en webapplicaties te ontwikkelen en te onderhouden.

[Jamstack](jamstack.org)

### Mentoring

Je bent mentor van 5/6 1ste jaars studenten, dit doe je met 4 studenten uit je squad dat heet je mentor team.

Squad 2D (Justus) is mentor van squad 1H (Krijn)
Er moet elke ma/wo/vr 1 mentor aanwijzig zijn en dit moet Krijn dus weten!

[Leertaak](github.com/fdnd-task/mentor)

### Coaching

Coach gesprek heb je met je squad leader op ma/wo/vr en neemt je retrospect als uitgangspunt, het gaat over je ontwikkeling!

### Project indeling
- FDND Programma
- Team: Kaan & Ilona
- Preferred stack: SvelteKit en Directus 

## SvelteKit Talk | Justus
### Structure
- In het mapje src staat alles wat sveltekit moet uitvoeren.
- In het mapje static staat alles waar sveltekit niks mee hoeft te doen (Public in nodeJS).
- Het bestand app.html is het beginpunt van je sveltekit applicatie.
- Het mapje routes is verplicht omdat al je pagina's daarin staan.
- In het mapje Lib staat je library van codes die je hergebruikt.
- In het mapje lib/server staat al je server side code in.
- Sensitive informatie mag alleen in je server map, anders is alles te achterhalen  (api key, inlog gegevens etc).
- Afbeeldingen etc horen niet in het mapje Lib, alleen SVG's mogen erin (Dus alles dat niet inline is in HTML).
- De file .gitignore staan patronen voor bestanden die niet naar git gestuurd worden (.env, node modules, etc.).
- In .env staat alles in wat betreft je API key of andere variabelen die niet gepublished mogen zijn.
- In .env.example staan alle variabelen in die anderen kunnen gebruiken die jouw project willen gebruiken om verder te werken.
- In package.json staan al je dependencies en packages.
- In svelte.config.js staat alles in wat betreft de configuratie van sveltekit.
- In vite.config.js staat alles in wat betreft de configuratie van Vite.
- Vite is een soort projectrunner, build tool etc.
- Zet in VSCode je editor preferences op medium zodat je kan zien waar een bestand in staat (bvb src/lib/+page.svelte).

### Routing
- Je kan in de map Routes 2 folders aan maken genaamd [dynamic] voor dynamische routes en [static] voor statische routing.

### Error handling
- Je kan +error.svelte gebruiken, maar dit is alleen als sveltekit nog overeind staat.
- Voor als er niks van sveltekit overeind staat dan gebruik je error.html
- Je kan +layout.svelte gebruiken voor goeie layouts en ook om de errors goed erin te zetten
- Voor errors kan je variabel pakken like page en dan laad je dat in in je html met ($page.error) en een bericht met iets als {$page.error.msg)

### Loading data
- Voor het inladen van gegevens heb je +page.server.js als je het via de server inlaad, hierbij moet je ook `async` erbij zetten, omdat er wachttijd bij zit.
- hoe je data inlaad is met de code:
  `export async function load() {
    return {
      foo: 'bar'
    }
  }`
  
- Om gegevens in te laden moet je `export` gebruiken (als je data vanuit componenten of iets nodig hebt).
- Alles waarbij je expoert zet kan gebruikt worden als data.
- server side mag wel geheime informatie gebruiken

### Binding
- je kan variabelen binden in sveltekit, hierdoor is het overal aangepast.
- Het zorgt ervoor dat in een tekst field dat het mee aangepast wordt, met bvb gegevens.
- Bij een 2de variabele moet je ook een aparte bind gebruiken, dit heet reactive en doe je ipv let een $: dat ziet er dan zo uit:
  ` let name = 'yo'
    $: shout = name + 'sucks'`

- Dit werkt ook voor componenten

### Library
- Hier zet je herhaalbare code in zoals componenten etc.
- In index.js zet je niks anders in dan exports van componenten etc.

### Components
- Bij componenten in de lib moet je ze aanmaken zonder de + maar wel met een hoofdletter dus bvb Header.svelte, dit is een conventie van sveltekit
- In index.js zet je niks anders dan exports van componenten etc.

## We Love Web met Nicolas Garnier
### achtergrond info:
- Started dev in 2012
- freelancer in 2018
- [website](https://nico.computer/)

### Waar hij over sprak:
Wat is een creative dev nu? Het is een fancy term voor een developer die creatief is...

Je kan dus tools en frameworks creatief gebruiken voor het bedenken van een oplossing voor je opdrachtgever.

Important factors for creative coding:
- Anticipation and suprise
- Set the mood and support the narrative
- Engage the user
- Solve design and technical challenges
- Listen to the client and what they want, not everyone wants a site filled with animations.
- Look at the clients website and try to design animations that fit the design choices they made.

## 07/10/2024
### Woordenlijst
- Minimum viable product: Alle Must haves zjin geimplementeerd in het product.
- Optimum viable product: Alle Must, Should haves en Could haves zijn geimplementeerd in het product.
- Velocity: hoeveelheid poker planning punten waar je doorheen gaat in een sprint

## yadayada

### Oplevering
- Refactored code
    - Componenten
    - Pull requests en branches
    - code conventies
    - no commented code
    - no console.logs
- Readme
    - Kenmerken
    - Live link
    - screenshots
    - instructie
    - installatie handeling
    - CMS uitleg
    - Huisstijl en andere bijdragen
    - link naar projectboard
    - Gebruikte techstack
    - Changelog over alle aanpassingen in de sprint
    - Releases erin zetten
- Live zetten
    - Live URL in de description zetten van t proejct
- Testen en resultaten
    - Performance, keyboard, screenreader, lighthouse etc
- Klant
    - Vraag hoe hun het project willen opleveren
    - Vraag hoe hun het project willen opleveren
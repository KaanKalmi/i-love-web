# Sprint 13

## Recap nodejs 
_NodeJS is een JS bs, waardoor je je frontend geode kan connecten via een server naar de database_
- Route: GET, PATCH, POST etc.
- Fetch: Pakt een JSON file op.
- Render: Rendert de pagina op je browser (het versturen van definitieve HTML naar een browser)

## sveltekit
_SvelteKit is een library dat gedraait word in Svelte, wat word gemaakt voor t schrijven van websites net als een framework dus_
### Svelte vs Sveltekit
- Svelte: Compiler
- SvelteKit: Library geschreven in svelte
_hoe maak je iets PE in SvelteKit? Je zet in de HTML tag `enhanced=true` Bijvoorbeeld `<form enhanced=true>`_
### Hoe werkt SvelteKit?
- Folder based routing
- GET en POST request worden 'onder water' afgehandeld
- Elke route heeft o.a. een server en component (view) bestand
- Data word geexporteerd van het server bestand naar het svelte component
- SvelteKit deelt code slim op de client en op de server (hydration)
- De website werkt echter ook als er geen JS beschikbaar is in de browser
- We beginnen SSR-only mode door client side rendering uit te zetten
- Export `let csr = false` (`+page.js` in de root van de route folder)
## directus
_Directus is een Headless CMS en een database bullshit_
- Models : structuur
- Content: Gegevens die je in directus beheart 
- Data: gegevens
### handige informatie dat Justus zegt tijdens zn presentatie
- We hosten in vercel of netlify
- We beginnen zonder serverside ofz idk
- Static folder is hetzelfde als public in EJS
- Src folder is waar alles gebeurd 
- In src folder vind je app.html hier niet aan zitten zolang je niks nodig hebt zoals stylesheet etc.
- De data-sveltekit-preload-data="hover" betekent dat als iemand over een link hovert dat sveltekit alvast de pagina laad (Werkt alleen op desktop, op mobile word het niet ingeladen)
- in de lib folder zitten al je componenten (iets dat je dus hergebruikt)

## Code/Design review 06/09
### Visite kaartjes (jaar 1)
Wij zijn mentors voor 1ste jaars studenten, dus:
- je begeleid 1x per week de 1ste jaars
- Je helpt ze bij het grip krijgen voor webtechnologies, dev cycles en grip krijgen op de opleiding
_Zone of Proximal Development (ZDP) Je moet ze niet te moeilijke dingen laten doen maar juist helpen bij dingen die ze wel kunnen met minimale hints erbij (dus niet zeggen oh het is niet PE, maar eerder gebruik een @media zodat t accessible is._

_Feedback geven op visitekaartjes gaat via issues op github_
### Learning journal / I love web
- Learning journal is een sort logbook waarbij je alles bijhoud
- AFGERADEN om wiki te gebruiken, je kan liever .md bestanden maken en dit vertalen naar HTML met 11ty!
- Je kan het gebruiken als soort etalage oftewel een site waarmee je kan aanduiden wat jij allemaal kan in dit vakgebied
### Feedback squadpage (team)
-2 feedback rondes over de squadpage
- Kijk naar de D.o.D's (zijn dezelfde DoD's als in sprint 12) 
_Feedback geven gaat als volgt:_
- Zit met je team aan 1 tafel en zet de puntjes op de i nog ff
- Tafel naast je geeft 15 min lang feedback aan jou en jij aan hun
- daarna de andere tafel (clockwise)
### Open brainstorm visitekaartje (team)
_Maandag start het officieel het werken aan t visitekaartje_
- Brainstorm ronde doen we via issues in GitHub

## Figma workshop-Kill your darlings 09/09
### Workshop over hoe Cyd werkt met figma
### Hoe begint ze?
- Ze maakt screenshots van verschillende designs die ze leuk vind bvb op linkedin Instagram etc
- Ze maakt daarna schetsen van de opgepakte inspiratie
- Ze maakt ook een assets mapje (ze wou dus bvb werken met depth waardoor ze een map maakte met zwart witte fotos voor diepte)
### Tips & Tricks:
- Gebruik niet teveel fonts 
- Line height is belangrijk,meestal is 120% goed genoeg (1.2)
### Tips voor groepje:
- Figma is trash
- Designing is trash

## Creative Coding with SvelteKit - Joost // Justus
### Progressive Enhancement
Development strategie van Content first, iedereen kan e website gebruiken en mensen met betere internet en browsers etc krijgen een enhanced versie van de website bvb met animaties of interactiviteit.
### Creative coding with CSS
- Scroll-snap-type: x-mandatory; Maakt scroll snap op de X-axis mandatory oftewel verplicht.
- Dit is een non-breaking enhancement, als iemand een niet ondersteunde browser heft hiervoor an hij/zij nogsteeds even goed scrollen alleen heft et niet de scroll snap.
- Een breaking enhancement is dus een enhancement dat wanneer iemand geen ondersteuning heft voor en css techniek dan breekt heel de css bestand voor diegene.
- @support Maakt dus een breaking enhancement een non-breaking enhancement, want als het niet ondersteund word haalt hij gewoon de css code weg.
- Kijk vooral in de docs van SvelteKit omdat niet alles hetzelfde werkt in SvelteKit als vanilla CSS!
### Creative coding with JS
- Dit is wat t meest verandert in sveltekit
- Als je wat interatief wilt maken heb je JS nodig
- Kijk vooral in de docs van SvelteKit omdat niet alles hetzelfde werkt in SvelteKit als vanilla JS!
- document bestaat niet in sveltekit (in de server) hiervoor gebruik je de `onMount` functie in de client
- Of je zet het in de static folder (hierdoor gebruiken alle paginas de script tho)
- met onMount kan je JS maken zoals je gewend bent
- Je kan transities en animaties importeren van sveltekit modules, zo hoef je het zelf niet te coderen. 
- Je kan het dus als een soort class erbij zetten en extra info geven zoals hier aangegeve `<fieldset transition:fade={{duration: 250ms }}>`
### Handy take aways from this talk:
- Creative coding === Progressive Enhancement === Content First
- HTML Supremacy :joy:
- Doe de tutorial van SvelteKit!
-`csr = false` doet Client Side Rendering uit (dus JS staat uit)

## Articles I've read:
- [SvelteKit REPL MediaQuery](https://svelte.dev/repl/26eb44932920421da01e2e21539494cd?version=4.2.19)
- [SvelteKit Docs - Introduction](https://kit.svelte.dev/docs/introduction)
- [SvelteKit Docs - Creating a project](https://kit.svelte.dev/docs/creating-a-project)
- [SvelteKit Docs - Project Structure](https://kit.svelte.dev/docs/project-structure)
- [SvelteKit Docs - Routing](https://kit.svelte.dev/docs/routing)
- [SvelteKit Docs - Adapters](https://kit.svelte.dev/docs/adapters)
- [SvelteKit Docs - Node Servers](https://kit.svelte.dev/docs/adapter-node)
- [SvelteKit Docs - Performance](https://kit.svelte.dev/docs/performance)
- [SvelteKit Docs - Images](https://kit.svelte.dev/docs/images)
- [SvelteKit Docs - Accessibility](https://kit.svelte.dev/docs/accessibility)
- [SvelteKit Docs - SEO](https://kit.svelte.dev/docs/seo)
- [SvelteKit Docs - FAQ](https://kit.svelte.dev/docs/faq)
- [SvelteKit Docs - Loading data](https://kit.svelte.dev/docs/load)
- [SvelteKit Docs - Vercel](https://kit.svelte.dev/docs/adapter-vercel)
- [SvelteKit Docs - onMount](https://svelte.dev/docs/svelte#onmount)
- [SvelteKit Blog - Unlocking view transitions](https://svelte.dev/blog/view-transitions)
- [SvelteKit Docs - How to use view transition API in sveltekit](https://kit.svelte.dev/docs/faq#how-do-i-use-the-view-transitions-api-with-sveltekit)

## Video's I've watched:
- [Fireship - Sveltekit in 100 seconds](https://www.youtube.com/watch?v=H1eEFfAkIik)
- [Joy of Code - The Comprehensive Introduction To SvelteKit](https://www.youtube.com/watch?v=obmiLi3bhkQ&t=839s)
- [Prismic - What companies use sveltekit](https://www.youtube.com/shorts/_Ge-cVPHBjc)
- [Ben Davis - 5 Things I Wish I Knew When I Started Using SvelteKit](https://www.youtube.com/watch?v=eJpPNg-v0Fo)

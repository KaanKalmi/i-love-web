# Recap nodejs 
_NodeJS is een JS bs, waardoor je je frontend geode kan connecten via een server naar de database_

- Route: GET, PATCH, POST etc.
- Fetch: Pakt een JSON file op.
- Render: Rendert de pagina op je browser (het versturen van definitieve HTML naar een browser)

# sveltekit
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

# directus
_Directus is een Headless CMS en een database bullshit_

- Models : structuur
- Content: Gegevens die je in directus beheart 
- Data: gegevens

# demo
_Kijk gewoon naar SvelteKit docs en tutorial oprecht, drnaast kan je directus docs pakken over SvelteKit klaar_

# handige informatie dat Justus zegt tijdens zn presentatie
- We hosten in vercel of netlify
- We beginnen zonder serverside ofz idk
- Static folder is hetzelfde als public in EJS
- Src folder is waar alles gebeurd 
- In src folder vind je app.html hier niet aan zitten zolang je niks nodig hebt zoals stylesheet etc.
- De data-sveltekit-preload-data="hover" betekent dat als iemand over een link hovert dat sveltekit alvast de pagina laad (Werkt alleen op desktop, op mobile word het niet ingeladen)
- in de lib folder zitten al je componenten (iets dat je dus hergebruikt)

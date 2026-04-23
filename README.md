# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src
│   ├── assets
│   │   └── astro.svg
│   ├── components
│   │   └── Welcome.astro
│   ├── layouts
│   │   └── Layout.astro
│   └── pages
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).







# Spin_the_recipe
## Om projektet

Dette projekt er lavet som en del af Tema 9. Vi har lavet et dynamisk website med astro, hvor indholdet bliver hentet fra et selvlavet dataset.

Sitet består af flere sider, hvor brugeren kan:

Se en liste med indhold, klikke sig videre til en detaljeside hvor de kan bruge filtrering, se information om det specifille indhold.

## Links
- GitHub repository:https://github.com/tema9-gruppe3/a-good-case
- GitHub Pages: kan ikke generers
- Figma: https://www.figma.com/design/sWAWqtPpiCw6nbKHfGU0b3/A-Good-Case?node-id=714-2117&t=hAALs1enVJ3CDv2B-0


## Projektstruktur
Projektet er opdelt i Astro-komponenter.

project/
├── pages/
│   ├── index.astro
│   ├── productlist.astro
│   └── [id].astro
├── components/(eksempler)
│   ├── Pcard.astro
│   └── Productgrid.astro
└── README.md

### Filbeskrivelser

- **index.astro** – forsiden  
- **productlist.astro** – viser en liste med data fra API'et som kan filtreres  
- **[id].astro** – viser detaljer om et valgt produkt  


---

## Hvordan koden fungerer

Vi har opdelt JavaScript, så hver side har sin egen logik.

### index.astro

Bruges på forsiden.
Her bliver indhold vist dynamisk, via produkter hentet fra API´et.

### productlist.astro

Henter data fra API'et og viser en liste med øl på siden, som kan filtreres.

**Flow:**

1. Siden loader
2. JavaScript kører
3. Data hentes fra API´et
4. Data bliver gennemgået med loop
5. HTML bliver indsat i DOM'en
6. Brugeren kan filtrere produkter via knapper
7. Brugeren kan klikke på et produkt

### [id].astro

Bruges til detaljesiden. Den læser et id fra URL'en og henter derefter det rigtige produkt fra API'et.

Det gør det muligt at genbruge den samme HTML-side til mange produkter. I stedet for at lave én side per produkt, bruger vi ét id i URL'en til at vise det rigtige indhold.

---

## Navngivning

Vi har navngivet vores filer, variabler og funktioner så de så vidt som muligt er selvforklarende.

### Eksempler på variabler

```javascript
const endpoint
const options
const cards
```

### Eksempler på funktioner

```javascript
function filtrer(e)
```

Vi har brugt camelCase i JavaScript, fordi det gør koden mere ensartet og lettere at læse.

---

## Kommentarer i koden

Ingen kommentarer i koden.





---

## Data og JSON-struktur

Vi henter data fra superbase, som vi selv har lavet.



### Felter vi bruger
- **id** – bruges til at sende brugeren videre til detaljesiden  
- **productname** – navnet på øllen  
- **brand** – producenten/bryggeriet  
- **description** – beskrivelse af øllen  
- **categories** – øltype/kategori (fx IPA, ALE, WILD)  
- **price** – produktets pris  
- **image** – produktbillede  
- **size** – størrelsen på øllen (cl)  
- **ABV** – alkoholprocent  
- **style** – øltype/stil  
- **color** – farveindikator for øllen  
- **allergen** – information om allergener  
- **fault** – årsag til nedsat pris (fx overproduktion eller kort holdbarhed)
---



## Git og branches

Vi har brugt GitHub til at samarbejde om projektet.

Vi har arbejdet med branches, så vi ikke sad og ændrede i det samme på samme tid.

Vi navngav branchene med feature først.

### Eksempler på branches

- `imageswitch`
- `header`
- `idastro`


### Workflow

1. Lave en branch med navn.
2. Kode en feature
3. Committe ændringer
4. Pushe til GitHub
5. Merge til main når det virkede

Det gjorde det nemmere at holde styr på, hvad der blev lavet og at man kunne gå tilbage i tidligere versioner. 

---

## Bæredygtighed

Vi har tænkt bæredygtighed ind i projektet ved at have brugt Astro, hvilket gør løsningen mere bæredygtig, da der sendes mindre data til brugeren og dermed bruges mindre energi.

**Tiltag:**

- Brug af cards
- Ingen tunge frameworks
- Genbruge af kode


---

## Udfordringer undervejs

En af vores udfordringer var at data fra Rest API’et havde billeder som vi ikke kunne definere en størrelse på. 
Der var udfordringer med at få filtreringsknapperne til at virke korrekt. Da filtreringen ikke viste produkter, i og med der var et mismatch mellem data-type i HTML og de værdier vi havde givet i datasættet. 



**Løsninger:**

- at bruge .toLowerCase() og rette så de matchede. 

---

## Mulige forbedringer

Hvis vi skulle arbejde videre med projektet, kunne vi forbedre det ved at tilføje:

- Søgefunktion
- "sidst sete" nederst på siden
- Loading af flere opskrifter ved klik

---

## Gruppemedlemmer

- Signe Skriver Lorentzen
- Cecilie Grehart
- Louise Rasmussen
- Maya Christine Jensen


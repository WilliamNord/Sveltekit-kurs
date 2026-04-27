# SvelteKit-kurs
Dette er en del av et kurs jeg skal holde om SvelteKit.

må laste ned node ----- NOTAT

## Hvordan lage et SvelteKit-prosjekt

### først må vi sjekke om vi har node.js innstallert
kjør kommandoen i terminalen for å sjekke om du har node.
```bash
node -v
```
hvis du får et resultat som `v.22.18.0` har du noe, hvis ikke kan du laste det ned her [node.js download](https://nodejs.org/en/download)
du vil få noen valg for installasjon, da burde det se slik ut:
<img width="1133" height="544" alt="Screenshot 2026-04-27 at 10 34 36" src="https://github.com/user-attachments/assets/0cb26c13-40de-4c19-8617-1356a3dca4ce" />


### 1. i terminalen, gå til mappen du vil ha prosjektet i
Deretter kjører du denne kommandoen.
<br>
du kan endre "mye-app" til navnet du vil ha

```bash
npx sv create my-app
```

---

### 2. Velg oppsett

Når du oppretter prosjektet, får du flere valg.

#### Prosjekttype:
- [x] SvelteKit minimal  
- [ ] SvelteKit demo  
- [ ] Svelte library  

#### Språk:
- [x] Yes, using TypeScript syntax  
- [ ] Yes, using JavaScript with JSDoc comments  
- [ ] No  

Du kan også velge ekstra verktøy som f.eks. tailwindcss.
trykk enter for å bekrefte

---

### 3. Start prosjektet

#### åpne i terminalen:
```bash
cd my-app
npm run dev
```

#### åpne i 


Nå kan du åpne prosjektet i ***din*** tekst editor og starte å utvikle din egen nettside

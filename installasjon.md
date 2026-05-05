# SvelteKit-kurs

> Dette er en guide til hvordan du kan lage ditt eget svelte prosjekt

---

## Innhold

- [Krav – Node.js](#krav--nodejs)
- [Steg 1 – Opprett prosjektet](#steg-1--opprett-prosjektet)
- [Steg 2 – Velg oppsett](#steg-2--velg-oppsett)
- [Steg 3 – Start prosjektet](#steg-3--start-prosjektet)

---

## Krav –> Node.js

Før du begynner må du ha **Node.js** installert. Sjekk om du allerede har node.js ved å kjøre:

```bash
node -v
```

Får du noe som `v22.18.0` kan du gå videre. Hvis ikke, last ned Node.js her:

[Last ned Node.js](https://nodejs.org/en/download)

Slik burde installasjonsvalget se ut:

![Node.js installasjonsvalg](https://github.com/user-attachments/assets/0cb26c13-40de-4c19-8617-1356a3dca4ce)

Kopier kommandoene fra nettsiden og lim dem rett inn i terminalen.

---

## Steg 1 - Opprett prosjektet

Naviger i terminalen til mappen der du vil ha prosjektet, og kjør:

```bash
npx sv create my-app
```

> Bytt ut `my-app` med det navnet du vil gi prosjektet ditt.

---

## Steg 2 – Velg oppsett

Du vil bli spurt om flere valg under opprettelsen. Her er det vi anbefaler:

**Prosjekttype:**

| Valg | Anbefalt |
|------|:--------:|
| SvelteKit minimal | Ja |
| SvelteKit demo | |
| Svelte library | |

**Språk:**

| Valg | Anbefalt |
|------|:--------:|
| Yes, using TypeScript syntax | Ja |
| Yes, using JavaScript with JSDoc comments | |
| No | |

**Ekstra verktøy (valgfritt):**

Du kan også velge tilleggsverktøy som for eksempel:

- **Tailwind CSS** – stilrammeverk
- **Prettier** – kodeformatering

Trykk **Enter** for å bekrefte hvert valg.

---

## Steg 3 – Start prosjektet

```bash
cd my-app
npm run dev
```

Åpne prosjektet i din editor og du har laget ditt eget svelteprosjekt.

# SvelteKit-kurs

> Dette er en del av et kurs jeg skal holde om SvelteKit.

---

## Innhold

- [Krav – Node.js](#krav--nodejs)
- [Steg 1 – Opprett prosjektet](#steg-1--opprett-prosjektet)
- [Steg 2 – Velg oppsett](#steg-2--velg-oppsett)
- [Steg 3 – Start prosjektet](#steg-3--start-prosjektet)

---

## Krav – Node.js

Før du begynner må du ha **Node.js** installert. Sjekk om du allerede har det ved å kjøre:

```bash
node -v
```

Får du noe som `v22.18.0` er du klar. Hvis ikke, last ned Node.js her:

[Last ned Node.js](https://nodejs.org/en/download)

<details>
<summary>Slik ser installasjonsvalget ut</summary>

<br>

![Node.js installasjonsvalg](https://github.com/user-attachments/assets/0cb26c13-40de-4c19-8617-1356a3dca4ce)

Kopier kommandoene fra nettsiden og lim dem rett inn i terminalen.

</details>

---

## Steg 1 – Opprett prosjektet

Naviger i terminalen til mappen der du vil ha prosjektet, og kjør:

```bash
npx sv create my-app
```

> **Tips:** Bytt ut `my-app` med det navnet du vil gi prosjektet ditt.

---

## Steg 2 – Velg oppsett

Du vil bli spurt om flere valg under opprettelsen. Her er det vi anbefaler:

<details>
<summary>Prosjekttype</summary>

<br>

| Valg | Anbefalt |
|------|:--------:|
| SvelteKit minimal | ✅ |
| SvelteKit demo | |
| Svelte library | |

</details>

<details>
<summary>Språk</summary>

<br>

| Valg | Anbefalt |
|------|:--------:|
| Yes, using TypeScript syntax | ✅ |
| Yes, using JavaScript with JSDoc comments | |
| No | |

</details>

<details>
<summary>Ekstra verktøy (valgfritt)</summary>

<br>

Du kan også velge tilleggsverktøy som for eksempel:

- **Tailwind CSS** – stilrammeverk
- **ESLint** – kodekvalitet
- **Prettier** – kodeformatering

</details>

Trykk **Enter** for å bekrefte hvert valg.

---

## Steg 3 – Start prosjektet

```bash
cd my-app
npm run dev
```

Åpne prosjektet i din foretrukne editor og begynn å utvikle.

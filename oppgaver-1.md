# SvelteKit oppgaver

Du kan hoppe over oppgaver som virker *for* enkle.

---

## 1. Routing (sider)

SvelteKit lager sider basert på filer.

Oppgaver:
- Finn `src/routes/+page.svelte`
- Endre teksten på forsiden
- Lag en ny side: `src/routes/about/+page.svelte`
- Gå til `/about` i nettleseren
- Lag en link fra forsiden til `/about`

---

## 2. State (data som endrer seg)

Oppgaver:
- Lag en variabel `count` som starter på 0
- Vis `count` på siden
- Lag en knapp som øker `count` med 1 hver gang du trykker

Ekstra:
- Hvis `count` blir over 20, reset den til 0

---

## 3. Runes (Svelte 5)

Oppgaver:
- Endre state til å bruke `$state`
- Test at counter fortsatt fungerer
- Se om du merker forskjell i hvordan det skrives

---

## 4. Komponenter

Oppgaver:
- Lag en fil `src/lib/Button.svelte`
- Lag en knapp inni komponenten
- Bruk komponenten i en side
- Send inn tekst til knappen (props)

Eksempel:
```svelte
export let text = "Klikk meg";
```

---

## 5. Lister (each blocks)

Oppgaver:
- Lag en liste med minst 3 ting
- Vis listen på siden
- Bruk `{#each}` for å vise elementene
- Lag en knapp som legger til nye elementer i listen

---

## 6. Layout

Oppgaver:
- Lag `src/routes/+layout.svelte`
- Lag en enkel navbar
- Legg til `<slot />`
- Sjekk at navbar vises på alle sider

---

## 7. Mini-oppgave (sett alt sammen)

Lag en liten app som inneholder:
- teller
- liste
- komponent
- minst to sider

---

## Tips
- Test ofte i nettleseren
- Ikke stress med å bli ferdig
- Målet er å forstå, ikke å fullføre alt

# SvelteKit oppgaver

Du kan hoppe over oppgaver som virker for enkle.

---

## 1. Filstruktur og routing

I SvelteKit bestemmer filstrukturen hvilke sider som finnes. En fil på `src/routes/about/+page.svelte` blir automatisk tilgjengelig på `/about` i nettleseren. 

En side ser slik ut:

```svelte
<!-- src/routes/+page.svelte -->

<h1>Hei verden</h1>
<p>Dette er forsiden.</p>
```

En lenke mellom sider lages med en vanlig `<a>`tag:

```svelte
<a href="/about">Om oss</a>
```

### Oppgave 1: Se at det funker
Finn `src/routes/+page.svelte`. Endre overskriften til noe eget og lagre. Oppdaterer nettsiden seg?

### Oppgave 2: Lag en ny side
Lag filen `src/routes/about/+page.svelte` og skriv din egen tekst på den. Gå til `/about` i nettleseren og se om siden vises.

### Oppgave 3: Lenk mellom sider
Lag en lenke fra forsiden til `/about`, og en lenke fra `/about` tilbake til forsiden.

---

## 2. Reaktivitet med `$state`

I Svelte 5 bruker vi **runes** for å fortelle Svelte hvilke variabler som skal være reaktive. En reaktiv variabel oppdaterer automatisk det som vises i nettleseren når verdien endres.

`$state` er den vanligste runen. Du bruker den slik:

```svelte
<script>
  let count = $state(0);
</script>
```

Hvis du øker `count` vil teksten på nettsiden oppdateres automatisk. 

### Oppgave 4: Enkel teller
Lag en variabel `count` med `$state(0)`. Vis verdien på siden. Lag en knapp som øker `count` med 1 hver gang du trykker.

<details>
<summary>Løsningsforslag</summary>

```bash
<script>
    let count = $state(0);

    let increment = () => {
        count += 1
    }
</script>

<p>Count: {count}</p>

<button onclick={increment}>Increment</button>
```

</details>

### Oppgave 5: Flere knapper
Legg til en knapp som minker `count` med 1, og en knapp som nullstiller den til 0.

### Oppgave 6: Bonusoppgave
Hvis `count` går over 10, skal den automatisk nullstilles.

---

## 3. Layout

Når du vil at noe skal vises på alle sider, for eksempel en navbar, bruker du +layout. `src/routes/+layout.svelte` er i roten, og alt som legges der vises på alle undersider.

`<slot />` er plassholder for innholdet på siden:

```svelte
<!-- src/routes/+layout.svelte -->
<nav>
  <a href="/">Hjem</a>
  <a href="/about">Om oss</a>
</nav>

<slot />
```

### Oppgave 7: Lag en navbar
Lag `src/routes/+layout.svelte` med en enkel navbar og `<slot />`. Sjekk at navbaren vises på både forsiden og `/about`.

---

## 4. Komponenter

En komponent er en gjenbrukbar del av brukergrensesnittet. I stedet for å skrive samme knapp ti steder, lager du den én gang og bruker den overalt.

Komponenter lagres gjerne i `src/lib/components` og importeres der de skal brukes:

```svelte
<!-- src/lib/Button.svelte -->

<script>
  let { text = "Klikk meg" } = $props();
</script>

<button>{text}</button>
```

```svelte
<!-- src/routes/+page.svelte -->
<script>
  import Button from '$lib/Button.svelte';
</script>

<Button text="Send inn" />
<Button text="Avbryt" />
```

`$props()` er runen som brukes for å ta imot data. `text = "Klikk meg"` betyr at "Klikk meg" er standardverdien hvis ingenting sendes inn.

### Oppgave 8: Lag en komponent
Lag `src/lib/components/Button.svelte` med en knapp inni. Bruk komponenten på forsiden.

### Oppgave 9: Props
Legg til `$props()` slik at du kan sende inn tekst til knappen. Bruk samme komponent med to forskjellige tekster på samme side.

---

## 5. Lister med `{#each}`

Når du vil vise en liste med elementer bruker du `{#each}`:

```svelte
<script>
  let fruits = $state(["Eple", "Banan", "Appelsin"]);
</script>

{#each fruits as fruit}
  <p>{fruit}</p>
{/each}
```

Du kan legge til elementer i listen med `.push()`

```svelte
<button onclick={() => fruits.push("Mango")}>Legg til</button>
```

### Oppgave 10: Vis en liste
Lag en array med minst 3 ting og vis dem med `{#each}`.

### Oppgave 11: Legg til elementer
Lag en knapp som legger til et nytt element i listen hver gang du trykker.

### Oppgave 12: Bonusoppgave
Legg til en slett-knapp ved siden av hvert element som fjerner akkurat det elementet fra listen.

---

## Sluttoppgave

Lag en liten nettside som bruker alt du har lært:

- Minst to sider med fungerende lenker
- En navbar som vises på alle sider (layout)
- En teller med `$state`
- En liste med `{#each}`- ekstra: mulighet for å legge til eller ta bort elementer
- Minst én gjenbrukt komponent

---

## Tips

- Test i nettleseren underveis, ikke bare til slutt.
- husk å lagre filen med `cmd + s`
- Feilmeldinger i terminalen og i nettleserens konsoll er nyttige hvis ting ikke vises direkte på nettsiden.


#### Ønsker dere flere oppgaver eller forståelse om svelte, kan dere bruke svelte sin offisielle tutorial og guide her: [Svelte tutorial](https://svelte.dev/tutorial/svelte/welcome-to-svelte)

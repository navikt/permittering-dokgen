# permittering-dokgen

Denne tjenesten inneholder brevmaler som brukes av [permitteringsskjema-api](https://github.com/navikt/permitteringsskjema-api) til å generere brev relatert til ytelsen lønnskompensasjon.

Oppsettet for tjenesten er hentet fra [dokgen](https://github.com/navikt/dokgen) repoet til NAV IT.

### Forhåndsvise en PDF

For å forhåndsvise en PDF kan du gjøre et GET kall (f.eks. med Postman) mot

```bash
https://permittering-dokgen.intern.dev.nav.no/template/permittering/preview-pdf/testdata
```
Dette genererer et brev som bruker tekst fra template.hbs-filen inni mappen, og mock-data fra testdata-mappen sin testdata.json.

### Laste ned en PDF

For å laste ned en PDF kan du gjøre et POST kall (f.eks. med Postman) mot

```bash
$BASE_URL/template/{navnet på en mappe inni content/templates}/create-pdf
```

Eller se det som ren html

```bash
$BASE_URL/template/{navnet på en mappe inni content/templates}/create-html
```

Det kan hende at du må sende med en json body som inneholder dataen som variablene i template.hbs inni content/templates-mappen skal byttes ut med.
# tag-dokgen

Denne tjenesten inneholder brevmaler som brukes av [permittering-refusjon-journalforing](https://github.com/navikt/permittering-refusjon-journalforing) til å generere brev relatert til ytelsen lønnskompensasjon.

Oppsettet for tjenesten er hentet fra [dokgen](https://github.com/navikt/familie-dokgen-java) repoet til NAV IT.

## Generere PDF lokalt

### Starte applikasjonen

#### Alternativ 1

Start opp docker imaget med `./up.sh`

#### Alternativ 2

1. Start opp docker på din lokale maskin (dersom du bruker Colima kan du kjøre `sudo rm -rf /var/run/docker.sock && sudo ln -s /Users/$(whoami)/.colima/docker.sock /var/run/docker.sock && colima start`)
2. Kjør `docker-compose up`

### Forhåndsvise en PDF

For å forhåndsvise en PDF kan du gjøre et GET kall (f.eks. med Postman) mot

```bash
localhost:5913/template/{navnet på en mappe inni content/templates}/preview-pdf/testdata
```
(Alternativt så kan du bare gå inn på adressen over i nettleseren din)

Dette genererer et brev som bruker tekst fra template.hbs-filen inni mappen, og mock-data fra testdata-mappen sin testdata.json.

### Laste ned en PDF

For å laste ned en PDF kan du gjøre et POST kall (f.eks. med Postman) mot

```bash
localhost:5913/template/{navnet på en mappe inni content/templates}/create-pdf
```

Eller se det som ren html

```bash
localhost:5913/template/{navnet på en mappe inni content/templates}/create-html
```

Det kan hende at du må sende med en json body som inneholder dataen som variablene i template.hbs inni content/templates-mappen skal byttes ut med.

## Scripts

Gjøre scripts kjørbare:
`chmod +x *.sh`

### Deploy

script for å manuelt deploye til miljøene.

Basert på denne: https://doc.nais.io/deployment/manual

### Up

Enkel test for å se om docker-imaget kan bygges og starter riktig i containeren.

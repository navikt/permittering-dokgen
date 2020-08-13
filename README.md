# tag-dokgen

Brevmaler ifm. tiltaksavtaler.

## Importer maler i prosjekt

Bruker:

https://github.com/navikt/familie-dokgen-java

## Scripts

Gjøre scripts kjørbare:
`chmod +x *.sh`

### Deploy

script for å manuelt deploye til miljøene.

Basert på denne: https://doc.nais.io/deployment/manual

### Up

Enkel test for å se om docker-imaget kan bygges og starter riktig i containeren.

### Generere pdf lokalt

Start opp docker imaget med `./up.sh`

For å laste ned en pdf kan du gjøre et POST kall mot

```bash
localhost:5913/template/{template_endepunkt}/create-pdf
```

Eller se det som ren html

```bash
localhost:5913/template/{template_endepunkt}/create-html
```

###

# Henvendelser

## For Nav-ansatte

- Dette Git-repositoriet eies av [Team tiltak i Produktområde arbeidsgiver](https://navno.sharepoint.com/sites/intranett-prosjekter-og-utvikling/SitePages/Produktomr%C3%A5de-arbeidsgiver.aspx).
- Slack-kanaler:
  - [#arbeidsgiver-tiltak](https://nav-it.slack.com/archives/CCM9QUY3U)
  - [#arbeidsgiver-utvikling](https://nav-it.slack.com/archives/CD4MES6BB)
  - [#arbeidsgiver-general](https://nav-it.slack.com/archives/CCM649PDH)

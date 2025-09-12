# permittering-dokgen

Denne tjenesten inneholder brevmaler som brukes av [permitteringsskjema-api](https://github.com/navikt/permitteringsskjema-api) til å generere brev relatert til ytelsen lønnskompensasjon.

Oppsettet for tjenesten er hentet fra [dokgen](https://github.com/navikt/dokgen) repoet til NAV IT.

### Forhåndsvise en PDF

Du kan se permitteringsmeldingen i dev (krever naisdevice) her:
- [https://permittering-dokgen.intern.dev.nav.no/template/permittering/preview-pdf/permittering](https://permittering-dokgen.intern.dev.nav.no/template/permittering/preview-pdf/permittering).
- [https://permittering-dokgen.intern.dev.nav.no/template/permittering-trukket/preview-pdf/permittering](https://permittering-dokgen.intern.dev.nav.no/template/permittering-trukket/preview-pdf/permittering).

## Kjør lokalt

```
docker build -t permittering-dokgen . && docker run --rm -it -p 8080:8080 -e SPRING_PROFILES_ACTIVE=dev permittering-dokgen
```

Besøk så http://localhost:8080/template/permittering-trukket/preview-pdf/permittering eller http://localhost:8080/template/permittering/preview-pdf/permittering


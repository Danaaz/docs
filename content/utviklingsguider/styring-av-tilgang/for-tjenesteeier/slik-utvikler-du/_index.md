---
title: Slik utvikler du
description: Har du tjenester som du trenger å styre tilgangen til sparer du både tid og kostnader på å ta i bruk nasjonale felleskomponenter som allerede finnes. ID-porten verifiserer sluttbrukers identitet og Altinn kontrollerer at sluttbruker har tilgang til å bruke tjenesten.
weight: 10
---

Slik går dere frem:

1. **Opprette ny tjenesteeier i Altinn** Hvis det er første gang dere lager tjeneste i Altinn må tjensteeier opprettes i løsningen. Ta kontakt med din serviceleder eller tjenesteeier@altinn.no for å bistand til dette. 
2. **Definere brukerbehov og designe tjenesten** </br>Tenk nøye gjennom hele prosessen fra et brukerperspektiv. Hva er utfordringen og hvem skal den løses for? Hvilket behov skal tjenesten dekke? Er brukeren en person eller en organisasjon – eller kanskje begge deler? Hvilke data skal hentes inn, tilgjengeliggjøres, eller formidles til bruker? Lag gjerne en skisse til kommunikasjon med brukeren og test skissen på folk i målgruppen. God planlegging er nøkkelen til et godt resultat. Sjekk Guide: [Hvordan jobbe brukerorientert?](https://www.altinndigital.no/kom-i-gang/guide-kom-i-gang-med-altinn/hvordan-jobbe-brukerorientert/) for inspirasjon.
3. **Få tilgang til REST-API**</br>Har du ikke utviklet tjenester i Altinn før trenger du tilgang til våre løsninger. For å utvikle tjenesten får du tilgang til Altinn sin tjenesteutviklingsløsning. I tillegg trenger du API nøkkel for å kunne benytte REST-tjenester. Les [Kom i gang med utvikling](/docs/api/rest/kom-i-gang/). 
4. **Tilrettelegge for integrasjon mot ID-porten**</br>Har du ikke allerede en integrasjon mot ID-porten må dette etableres. Difi. har utarbeidet en guide som beskriver hvordan dette gjøres. Les om dette i Difi sin [Samarbeidsportal](https://samarbeid.difi.no/felleslosninger/id-porten/ta-i-bruk-id-porten).
5. **Tilrettelegge for integrasjon mot Maskinporten** For å bruke autorisasjonstjenester i REST må tjenesteeier autentisere seg. Vi anbefaler å bruke Maskinporten for dette, les [Autentisering med kun Maskinporten](/docs/api/rest/kom-i-gang/virksomhet/#autentisering-med-kun-maskinporten). 
6. **Opprette lenketjeneste i Altinn sin tjenesteutviklingsløsning**<br>For å bruke Altinn til tilgangsstyring må ressursen man tilgangsstyrer til registreres i vår løsning. Dette gjøres ved å opprette en Lenketjeneste i vår tjenesteutviklingsløsning. På tjenesten legges det inn informasjon om hvem som skal få lov til å bruke tjenesten og hvilken nettside sluttbruker skal rutes til når tilgangskontrollen er utført. Les mer om dette i [brukerveiledning for TUL](/docs/tul/).
7. **Tilrettelegge for integrasjon mot Altinn**<br>Altinn sitt [REST API for autorisasjon](/docs/api/tjenesteeiere/rest/autorisasjon/) benyttes til hente informasjon om ut hvem bruker kan opptre på vegne av og hvilke rettigheter vedkommende har. 
8. **Teste tjenestene** <br>Altinn har et eget [testmiljø](https://tt02.altinn.no/) hvor du kan teste om tjenester og grensesnitt virker som det skal. I testmiljøet bruker du fiktive testpersoner og organisasjoner. Når du har kommet så langt i utviklingen er det også viktig å brukerteste den endelige løsningen på reelle folk i målgruppen. Det vil sikre at det ikke er noen showstoppere for de som skal bruke tjenestene.
9. **Produksjonssette tjenesten**<br>Når tjenesten er testet ende til ende kan den produksjonssettes. Dette bestiller du hos oss. Det bør tas høyde for å verifisere at tjenesten fungerer tilfredsstillende i produksjonsmiljø før brukeren får tilgang til tjenesten.
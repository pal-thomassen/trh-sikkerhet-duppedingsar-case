# IoT-case for faggruppe sammenheng

I denne case-oppgaven skal vi jobbe med arkitektur for en fiktiv bedrift. Hensikten med dette er å trene på å lage ulike arkitekturer, med bokser og piler, men også å klare å identifisere hva som er viktig for denne spesielle casen og deres utfordringer og la arkitekturen gjenspeile dette.

Denne formen for case jobbing er inspirert av architecture katas fra boken [Software architecture](https://www.amazon.com/Fundamentals-Software-Architecture-Comprehensive-Characteristics/dp/1492043451) hvor de brukte dette som en måte å trene på å designe ulike software arkitekturer på. 

## Oppgaver

Oppgavene som skal løses i caset er som følger: 

1. Identifiser alle ikke-funksjonelle krav, dette er f.eks skalerbarhet, ytelse, sikkerhet, personvern, forvaltbarhet, brukervennlighet osv. Det er en lang liste med potensielle slike krav, men oppgaven er å identifisere noen få, maks 3-4 stk som er viktige å ha fokus på i arkitekturen. 

2. Designe en programvarearkitektur som ivaretar både de funksjonelle behovene, men også de ikke-funksjonelle behovene som er identifisert overfor. Ting å tenke på her er f.eks: Dataflyt, datalagre/databaser, cacher, frontend, kjøretidsmiljø, nettverkstrafikk, deployment osv.

3. Vi deler opp i grupper på 4-5 stk per gruppe, så kan hver gruppe utføre oppgavene overfor. Så samles vi til plenum diskusjon etterpå hvor hver gruppe får 10 minutter til å presentere sin arkitektur. 

## Case

### Thomassen hotness AS

Thomassen hotness AS er et nyoppstartet selskap som produserer smarte panelovner. De har allerede en generasjon med panelovner på markedet som ikke er smarte, men vanlige panelovner med termostat. Thomassen hotness ønsker nå å ta steget videre og utfordre sine konkurrenter som tilbyr smartovner med appstyring og integrasjon mot blant annet Tibber. Bekk er leid inn for å hjelpe Thomassen hotness til å utvikle sine egne smartovner som kan konkurrere med de andre i markedet. De ønsker hjelp å bistand med hele produktet, både sentral infrastruktur og programvare på selve panelovnene.

Selskapet er 2 år gammelt, men har utviklet en helt ny teknologi for panelovner som bruker nano-maskiner for å generere varme som bruker 30% mindre strøm enn tradisjonelle panelovner. Dette har gjort selskapet konkurransedyktig i et allerede etablert marked, men det har blitt stilt spørsmål ved brannsikkerheten ved disse ovnene og selskapet har hatt vanskeligheter med å bevise brannsikkerheten og robustheten mot allerede etablerte produkter.

#### Ønsket funksjonalitet

Siden konkurrentene til Thomassen hotness allerede har smarte panelovner ute på markedet, ønsker Thomassen Hotness at deres ovner minimum tilbyr det samme som konkurrentene. Konkurrentene har allerede smart styring av panelovner (natt, dag-senking og feriemodus) via app til både iOS og Android. Disse appene fungerer også selv om man ikke er hjemme, slik at man f.eks kan skru panelovnene sine i feriemodus selv om man ikke er hjemme.

På sikt ønsker Thomassen Hotness seg at panelovnene deres kan integreres med eksisternde plattformer, som f.eks Apple Homekit, Google Home og Amazon Alexa, men også være posisjonert til å ta i bruk nye muligheter som vil komme i framtiden. 

I framtiden er det også planlagt med flere produkter som skal kunne integreres med de smarte panelovnene, som smarte termometere, sikkerhetskameraer og mulige andre produkter. Alle disse produktene skal fungere sømløst sammen slik at man kan bruke ekstra termometer til å styre når en panelovn skal starte eller stoppe. 

Thomassen Hotness ser for seg at salgstallene vil akselerere etterhvert som flere oppdager deres nye teknologi og sikkerheten blir bevist overfor forbrukere og skeptikere og ser for seg at antall solgte panelovner vil få en eksponensiell vekst og ønsker også muligheter for å ekspandere internasjonalt dersom de har suksess hjemme i Norge.

**Dependency Management**  
Att hantera externa paket och deras versioner så att projektet körs likadant överallt. Görs via `package.json` och pakethanterare som npm/Yarn.

**Bundling**  
Att slå ihop många filer (JS, CSS, bilder) till färre paket för snabbare laddning. Exempel: Webpack, Rollup, Parcel.

**MD (Markdown)**  
Ett enkelt textformat som konverteras till HTML. Vanligt för README-filer och dokumentation.

**Monorepository (Monorepo)**  
Ett repo som innehåller flera projekt. Bra för gemensamma verktyg och delad kod, men kan bli tungt i stora organisationer.

**TTFHW (Time to First Hello World)**  
Mått på hur snabbt en utvecklare kan sätta upp och köra ett första exempel. Lågt värde = lätt att komma igång.

**Repository (Repo)**  
Plats där kod och historik lagras, ofta med Git. Kan vara lokalt eller på t.ex. GitHub.

**Webpack**  
En bundler som hanterar beroenden och skapar optimerade paket. Stöder code splitting, tree shaking och HMR.

**Package Manager**  
Verktyg som installerar och uppdaterar paket och beroenden (npm/Yarn). Säkerställer enhetlig miljö.

**WebMVC (Model-View-Controller)**  
Mönster som delar upp program i Model (data), View (UI) och Controller (logik). Gör koden modulär och underhållbar.

**Rollup**  
Bundler optimerad för ES-moduler. Vanlig för bibliotek där små, snabba paket behövs.

**Task Runner**  
Automatiserar återkommande uppgifter (build, test, lint). Exempel: Gulp, npm scripts.

**Continuous Monitoring**  
Kontinuerlig övervakning av prestanda, fel och säkerhet. Hjälper att upptäcka problem innan de drabbar användare.

**Interpreter (in comparison with Transpiler and Compiler)**  
Interpreter kör koden direkt rad för rad. Compiler gör maskinkod, transpiler översätter till annan högnivåkod.

**CI (Continuous Integration)**  
Varje commit byggs och testas automatiskt. Fångar fel tidigt och håller kodbasen stabil.

**Backlog**  
En prioriterad lista över uppgifter och funktioner. Används i agila metoder för planering.

**Github Actions**  
CI/CD-verktyg integrerat i GitHub. Automatiserar bygg, test och deployment vid händelser som push/PR.

**Version Control**  
System som sparar filändringar och historik, t.ex. Git. Möjliggör samarbete och återställning.

**README.md**  
Projektets huvuddokumentation. Innehåller info om syfte, installation och användning.

**Git Life Cycle**  
Flödet av kodändringar: ändra → stage → commit → push → PR → merge.

**Backend System**  
Serverdelen av en app. Hanterar logik, databaser och API:er.

**Component**  
En återanvändbar modul, t.ex. en React-komponent (UI) eller mikrotjänst (backend).

**YAML (YAML Ain't Markup Language)**  
Ett lättläst format för konfigurationsfiler. Vanligt i CI/CD och Docker.

**Obfuscation**  
Att göra koden svår att läsa för människor. Skyddar mot reverse engineering.

**Minification**  
Att ta bort onödig kod (mellanrum, kommentarer) för att minska filstorlek.

**Tree Shaking**  
Att ta bort oanvänd kod automatiskt vid bundling. Ger mindre paket.

**Component Testing**  
Att testa en enskild komponent isolerat för att verifiera dess beteende.

**Multi-Tier Architecture (n-Tier)**  
Arkitektur där systemet delas i lager, t.ex. presentation, logik, data. Ger separation av ansvar.

**Double Mock (Testing Double)**  
En mock verifierar att förväntade anrop görs med rätt argument. Används för beteendetester.

**Vite**  
Modernt byggverktyg. Snabb utvecklingsserver med HMR och effektiv produktion (via Rollup).

**Transpiler**  
Översätter kod mellan språkversioner, t.ex. ES6 till ES5. Exempel: Babel.

**Packaging**  
Att paketera kod och resurser till en distribuerbar enhet (paket, build, container).

**Staging Environment (Stage)**  
En miljö som speglar produktion för sista tester innan release.

**Build System**  
Verktyg som automatiserar kompilering, bundling och tester. Exempel: Webpack, Vite.

**Babel**  
En transpiler för modern JavaScript. Gör koden bakåtkompatibel.

**Linting**  
Automatisk kodanalys för att hitta fel och stilbrott. Exempel: ESLint.

**Continuous Delivery (CD)**  
Koden hålls alltid releasbar. Deployment kan ske snabbt och säkert.

**Compiler**  
Översätter högnivåkod till maskin- eller bytekod. Körs innan exekvering.

**Edge Computing**  
Kör beräkningar nära användaren eller datakällan. Minskar latens.

**RESTful (Representational State Transfer)**  
API-design med HTTP-metoder (GET/POST/PUT/DELETE) och stateless kommunikation.

**DRY (Don't Repeat Yourself)**  
Principen att undvika duplicerad kod. Ökar återanvändning och minskar fel.

**API (Application Programming Interface)**  
Ett gränssnitt för kommunikation mellan system eller komponenter.

**Frontend System**  
Klientdelen av en app. Hanterar UI, rendering och interaktion i webbläsaren.

**Self-Organizing Team**  
Ett team som själva fördelar arbete och ansvar. Vanligt i agila metoder.

**Test-Driven Deployment (TDD)**  
Att skriva test före kod (red → green → refactor). Ger säkrare lösningar.  
*(OBS: ofta står TDD för Test-Driven Development)*

**Serverless Computing**  
Kod körs i molnet utan att utvecklaren hanterar servrar. Skalning sker automatiskt.

**Persistency**  
Att data bevaras över sessioner och körningar. Exempel: databaser, filer.

**Microservice**  
En liten tjänst med eget ansvar. Deployas och skalas separat, pratar via API:er.

**Twelve Factor App**  
Tolv principer för att bygga moln-vänliga och skalbara appar.

**Cypress**  
Ett testverktyg för end-to-end-tester i webbläsaren.

**Integration Testing**  
Testar att flera komponenter fungerar tillsammans.

**Double Stub (Testing Double)**  
En stub returnerar fördefinierade svar. Bra för att isolera testobjektet.

**Jest**  
Ett testramverk för JavaScript/TypeScript. Vanligt i React-projekt.

**Doubles**  
Samlingsterm för dummy, fake, stub, spy, mock. Används i testning.

**Deploy**  
Att rulla ut en applikation till en miljö (test, stage, prod).

**Containerization**  
Att köra en app i isolerade containrar med alla beroenden. Exempel: Docker.

**Environment Variables**  
Konfigurationsvärden utanför koden. Styrs av miljön (dev/test/prod).

**Unit Testing**  
Test av minsta koddel (funktion/klass). Snabbt och isolerat.

**CommonJS**  
Ett modulsystem för Node.js. Import via `require()`, export via `module.exports`.

**Double Dummy (Testing Double)**  
En dummy används bara för att fylla parameterkrav. Har ingen logik.

**End User Testing (UAT)**  
Slutanvändare testar systemet innan release för att bekräfta krav.

**React Testing Library**  
Ett testbibliotek för React. Fokuserar på att testa ur användarperspektivet.

**Double Fake (Testing Double)**  
En förenklad men fungerande implementation, t.ex. en in-memory-databas.

**Double Spy (Testing Double)**  
Loggar hur en funktion används (anrop/argument). Används för verifiering.

**Client-Side Scripting**  
Kod (ofta JS) som körs i webbläsaren för interaktivitet.

**Hot Module Replacement (HMR)**  
Uppdaterar kod under utveckling utan att sidan laddas om.

**Require**  
Funktion i CommonJS för att ladda moduler. Används i Node.js.

**Node**  
JavaScript-runtime baserad på V8. Gör det möjligt att köra JS på serversidan.

**Express**  
Ett minimalistiskt ramverk för Node.js. Vanligt för API:er och webbservrar.

**Server-Side Scripting**  
Kod som körs på servern. Genererar svar till klienten.

**Import (ES6 Modules)**  
ES6-syntax för att importera/exportera kod. Möjliggör tree shaking.

**ECMAScript 6 (ES6)**  
JavaScript-standard från 2015. Introducerade bl.a. `let/const`, arrow functions och klasser.

**Prod Environment**  
Produktionsmiljön där appen körs för riktiga användare. Fokus på stabilitet.

**Dev Environment**  
Utvecklingsmiljö där kod skrivs och testas utan att påverka prod.

**Deployment Pipeline**  
Automatiserade steg från kod till produktion: build → test → release.

**Docker**  
Plattform för att bygga och köra containrar. Säkerställer samma miljö överallt.

**Merge Conflict**  
När Git inte kan slå ihop ändringar automatiskt. Måste lösas manuellt.

**Environment**  
En uppsättning resurser och konfiguration (dev/test/stage/prod) där appen körs.

**CommonJS**  
Modulsystem för Node.js. Import via `require()`, export via `module.exports`.

**Separation Of Concerns (SoC)**  
Princip att dela upp kod i separata delar (UI, logik, data). Ökar modularitet.

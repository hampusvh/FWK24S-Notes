## Bygg & Beroenden

**Dependency Management**
Beroendehantering i en React-applikation avser processen att hantera de bibliotek och paket som ditt projekt är beroende av, och att säkerställa att de är korrekt installerade, uppdaterade och konfigurerade. Detta hanteras vanligtvis via filen package.json, som listar alla beroenden som krävs för projektet. Verktyg som npm (Node Package Manager) eller Yarn används för att automatisera installation, uppdatering och borttagning av dessa beroenden, vilket gör det enklare att upprätthålla en konsekvent utvecklingsmiljö över olika datorer.

**Bundling**
Processen att kombinera flera filer, såsom JavaScript, CSS och andra tillgångar, till en enda eller ett fåtal utdatafiler. Detta görs för att minska antalet HTTP-förfrågningar som behövs för att ladda en webbsida, vilket kan förbättra laddningshastigheten och den övergripande prestandan för webbapplikationer. Bundlers som Webpack, Rollup och Parcel används ofta i modern webbutveckling för att hantera beroenden och optimera leveransen av kod.

**MD (Markdown)**
Ett lättviktigt märkspråk som används för att formatera text. Det är utformat för att vara lätt att läsa och skriva, med ren text-syntax som kan konverteras till HTML för webbinnehåll. Markdown används i stor utsträckning för att skriva dokumentation, README-filer, blogginlägg och annat innehåll där enkelhet och läsbarhet i klartext är viktigt.
(Nyckelfunktioner: Enkel syntax, lätt att konvertera, utbredd användning)

**Monorepository (Monorepo)**
En versionshanteringsstrategi där flera projekt eller komponenter lagras och hanteras i ett enda, enhetligt repository. Detta tillvägagångssätt gör att alla relaterade kodbaser kan samexistera, vilket möjliggör delad kod, konsekventa verktyg och centraliserad versionshantering. Även om en monorepo kan förenkla utvecklingen för mindre projekt genom att hålla allt på ett ställe, kan den bli svår att hantera när projektet skalas upp, vilket potentiellt leder till utmaningar med byggtider, beroendehantering och koordinering mellan team. Av den anledningen kan monorepos passa bättre för mindre eller enklare projekt än för stora, komplexa system.

**TTFHW (Time to First Hello World)**
Avser den tid det tar för en utvecklare att sätta upp ett projekt eller en miljö och nå punkten där hen kan köra ett grundläggande ”Hello World!”-program. Detta mått används ofta för att bedöma hur snabbt och enkelt en ny utvecklare kan komma igång med ett verktyg, ramverk eller projekt. Ett lägre TTFHW indikerar en mer användarvänlig setup och en smidigare onboarding-upplevelse.

**Repository (Repo)**
En central plats där kod och dess historik lagras och hanteras, vanligtvis med ett versionshanteringssystem som Git. Det fungerar som lagringsutrymme för alla filer, kataloger och relaterade resurser i ett projekt, tillsammans med deras versionshistorik, vilket möjliggör samarbete, spårning av versioner och hantering av kodändringar över tid. Repositories kan hostas lokalt på en utvecklares dator eller externt på plattformar som GitHub, GitLab eller Bitbucket.

**Webpack**
En populär modul-bundler för JavaScript-applikationer. Den tar moduler med beroenden och genererar statiska tillgångar som representerar dessa moduler. Webpack gör det möjligt att bunta och hantera tillgångar såsom JavaScript, CSS, bilder och typsnitt i en enda fil eller mindre filer, optimerade för webben. Den är mycket konfigurerbar och stöder avancerade funktioner som code splitting, tree shaking och hot module replacement (HMR).

**Package Manager**
Ett verktyg som automatiserar processen att installera, uppdatera, konfigurera och hantera mjukvarupaket eller bibliotek. Dessa paket är samlingar av kod, ofta delade av andra utvecklare, som tillhandahåller specifik funktionalitet eller verktyg för att underlätta utveckling. Paket-hanterare tar hand om komplexiteten i beroendehantering och säkerställer att rätt versioner av paket och deras beroenden installeras och är kompatibla med varandra. De är avgörande i modern mjukvaruutveckling, särskilt i miljöer som är starkt beroende av externa bibliotek eller moduler.

**WebMVC (Model-View-Controller)**
Ett designmönster som används i webbutveckling för att separera ansvar inom en applikation. Det delar upp applikationen i tre sammanlänkade komponenter: Model (som representerar data eller affärslogik), View (som representerar UI eller presentationslager) och Controller (som hanterar användarinmatning och uppdaterar Model och View). Mönstret används ofta i webb-ramverk för att organisera kod på ett sätt som främjar modularitet, skalbarhet och underhållbarhet.

**Rollup**
En modul-bundler för JavaScript-applikationer, främst använd för att bunta små koddelar till större, mer komplexa applikationer. Rollup är utformad för att fungera med ES6-moduler (ECMAScript 2015) och fokuserar på att producera minimala, effektiva paket genom att eliminera död kod (tree-shaking) och utnyttja de senaste JavaScript-standarderna. Den används ofta i moderna JavaScript-projekt, särskilt för att bygga bibliotek och verktyg där optimerade och kompakta paket är viktiga.

**Task Runner**
Ett verktyg som automatiserar repetitiva utvecklingsuppgifter såsom minifiering, kompilering, enhetstestning, lintning och filbevakning. Genom att automatisera dessa uppgifter hjälper task runners till att effektivisera utvecklingsprocessen, minska fel och spara tid. De är särskilt användbara i webbutveckling för att hantera byggprocessen och andra rutinuppgifter.

**Continuous Monitoring**
Praktiken att kontinuerligt spåra, analysera och rapportera prestanda, säkerhet och tillförlitlighet för en applikation eller ett system i realtid. Denna process hjälper till att identifiera och åtgärda problem innan de påverkar slutanvändare och säkerställer att applikationen körs smidigt. Kontinuerlig övervakning innebär vanligtvis att man följer mätvärden såsom systemhälsa, upptid, svarstider, felfrekvenser och säkerhetshot.

**Interpreter (in comparison with Transpiler and Compiler)**
En typ av program som direkt exekverar instruktioner skrivna i ett programmerings- eller skriptspråk utan att de först behöver kompileras till maskinkod. I stället för att översätta hela källkoden till ett lägre nivåspråk (som en kompilator gör) bearbetar en tolk koden rad-för-rad eller sats-för-sats, översätter och exekverar den löpande. Detta kan leda till långsammare exekvering jämfört med kompilerade språk, men erbjuder fördelen av omedelbar körning och enklare felsökning.

**CI (Continuous Integration)**
En mjukvaruutvecklingspraxis där utvecklare ofta integrerar sina kodändringar i ett delat repository, vanligtvis flera gånger per dag. Varje integration byggs och testas automatiskt för att upptäcka fel så tidigt som möjligt. CI syftar till att förbättra kodkvaliteten, minska integrationsproblem och möjliggöra snabb, sammanhållen utveckling.

**Backlog**
En prioriterad lista över uppgifter, funktioner och krav som ett utvecklingsteam behöver arbeta med. Den fungerar som teamets att-göra-lista, där objekt läggs till, förfinas och omprioriteras under projektets livscykel. Backloggen är central i agila metoder och hjälper team att fokusera på att leverera de mest värdefulla funktionerna först.

**Github Actions**
En kraftfull CI/CD-plattform som låter utvecklare automatisera uppgifter såsom bygg, test och driftsättning direkt från sina GitHub-repositories. Med GitHub Actions kan du skapa anpassade arbetsflöden som triggas av specifika händelser (som push, pull request eller skapande av issue) för att effektivisera utvecklingsprocessen.

**Version Control**
Ett system som registrerar ändringar i filer över tid så att du kan återkalla specifika versioner senare. Det gör det möjligt för flera utvecklare att samarbeta i ett projekt genom att spåra och hantera ändringar i kodbasen. Versionshanteringssystem (VCS) gör det möjligt att arbeta samtidigt på olika delar av ett projekt, hålla reda på varje ändring och återställa tidigare versioner vid behov.

**README.md**
En Markdown-fil som vanligtvis finns i rotkatalogen av ett programvaruprojekt. Den fungerar som projektets huvuddokumentation och ger nödvändig information om projektet, hur man installerar och använder det samt andra detaljer som utvecklare eller användare kan behöva för att förstå och bidra. Tillägget ”.md” står för Markdown, ett lättviktigt märkspråk som möjliggör enkel formatering av text med klartext-syntax.

**Git Life Cycle**
De steg som kodändringar går igenom när de utvecklas, commit-as och integreras i ett Git-repository. Att förstå Git-livscykeln är grundläggande för att effektivt hantera ändringar, samarbeta med andra och upprätthålla en ren projekthistorik.

**Backend System**
Avser applikationens server-side-infrastruktur som hanterar affärslogik, databasinteraktioner, användarautentisering och andra kärnfunktioner som sker bakom kulisserna. Det fungerar som applikationens ryggrad genom att behandla förfrågningar från frontend och skicka tillbaka lämpliga svar.

**Component**
I React är en Component en återanvändbar, självständig UI-enhet som kapslar in sin egen struktur, logik och stil. Komponenter kan vara funktionella eller klassbaserade och utgör byggstenarna i en React-applikation. De tar emot data via props och hanterar eget state för att rendera UI dynamiskt baserat på användarinteraktion eller databas förändringar. I ett bredare arkitektursammanhang kan en Component också avse en backend-mikrotjänst eller annan modulär del av ett system som utför en specifik funktion oberoende av andra. I sådana fall interagerar komponenter via väldefinierade gränssnitt, ofta genom API:er eller meddelandeköer, och bidrar till applikationens helhet.

**YAML (YAML Ain't Markup Language)**
Ett människoläsbart serialiseringsformat för data, ofta använt för konfigurationsfiler och datautbyte mellan språk med olika datastrukturer. Filändelsen .yml eller .yaml används för YAML-filer. YAML är känt för sin enkelhet och användbarhet, vilket gör det möjligt att definiera data på ett tydligt och strukturerat sätt utan komplexiteten i exempelvis XML eller JSON.

**Obfuscation**
Processen att medvetet göra källkod svår att förstå genom att omvandla den till en version som är funktionellt likvärdig men svårare för människor att läsa. Tekniken används ofta för att skydda immateriella rättigheter, förhindra omvänd ingenjörskonst och säkra känslig logik i applikationer. Obfuskering innefattar typiskt att byta namn på variabler och funktioner till meningslösa beteckningar, ta bort eller ändra kommentarer samt ändra kodens struktur utan att påverka beteendet.

**Minification**
Processen att ta bort onödiga tecken från källkod, såsom blanksteg, kommentarer och radbrytningar, utan att ändra funktionaliteten. Syftet är att minska kodens storlek, vilket förbättrar prestanda för webbapplikationer genom att minska datamängden som måste överföras och påskynda laddningstider.

**Tree Shaking**
En optimeringsteknik i moderna JavaScript-bundlers för att ta bort död eller oanvänd kod från den slutliga bundlen. Metaforen ”skaka trädet” syftar på att analysera projektets beroendeträd, identifiera kod som inte används och eliminera den. Resultatet är mindre, effektivare paket som laddar snabbare och använder mindre bandbredd.

**Component Testing**
Innebär att testa enskilda komponenter i en applikation isolerat för att säkerställa att de fungerar korrekt. Denna testtyp behandlar komponenten som en ”svart låda”, med fokus på indata och förväntade utdata utan att beakta interna implementationer. Den används ofta för UI-komponenter i ramverk som React, där man testar hur en specifik komponent beter sig under olika förutsättningar.

**Multi-Tier Architecture (also known as n-Tier Architecture)**
Ett mjukvaruarkitekturmönster som delar upp en applikation i flera separata lager eller ”tiers”, där varje lager ansvarar för specifika delar av applikationens funktionalitet. Denna ansvarsfördelning hjälper till att organisera kod, förbättra skalbarhet och hantera komplexitet genom att låta varje lager utvecklas oberoende. Den vanligaste formen är tre-skiktsarkitektur, men applikationer kan ha fler eller färre lager beroende på designkrav.

**Double Mock (Testing Double)**
En typ av test-double som inte bara simulerar beteendet hos riktiga objekt utan också registrerar interaktioner, såsom metodanrop och skickade argument. Mocks är särskilt användbara när du behöver verifiera att vissa metoder anropades under testets körning och granska specifika interaktioner mellan komponenter. Mocks kan förprogrammeras med förväntningar som definierar vilka metoder som ska anropas och med vilka parametrar, vilket gör dem mer sofistikerade än andra test-doubles som stubs eller dummies.

## Övrigt

**Vite**
Ett modernt frontend-byggverktyg som fokuserar på hastighet och prestanda. Vite förbättrar utvecklarupplevelsen med omedelbar serverstart, mycket snabb Hot Module Replacement (HMR) och optimerade byggprocesser. Det stöder både JavaScript och TypeScript och passar särskilt bra för moderna ramverk som React, Vue.js och Svelte. Vite utnyttjar ES-moduler, vilket gör det snabbare än traditionella bundlers som Webpack, särskilt i utvecklingsläge.

**Transpiler**
En typ av kompilator som översätter källkod från ett språk eller en syntax till ett annat på samma abstraktionsnivå. I webbutveckling används transpilers ofta för att konvertera modern JavaScript (ES6+) eller JSX (använt i React) till en version som är kompatibel med äldre webbläsare eller miljöer som inte har inbyggt stöd för nyare syntax.

**Packaging**
I mjukvaruutveckling avser packaging processen att slå samman eller paketera kod, resurser och beroenden i ett distribuerbart format. Detta kan vara ett paket, ett bibliotek, en körbar fil eller en container som enkelt kan delas, distribueras eller installeras i olika miljöer. Syftet är att säkerställa att programvaran kan distribueras pålitligt och användas med alla nödvändiga komponenter inkluderade.

**Staging Environment (Stage)**
En förproduktionsmiljö som fungerar som sista testyta innan driftsättning till produktionsmiljön. Staging är avsedd att spegla produktion så nära som möjligt, så att utvecklare och testare kan validera att applikationen fungerar som förväntat under förhållanden nära verklig användning. Miljön används för att fånga kvarvarande problem som inte identifierats i tidigare testfaser.

**Build System**
En uppsättning verktyg och processer som automatiserar kompilering, paketering och driftsättning av mjukvaruapplikationer. Den hanterar uppgifter som att omvandla källkod till körbara program, bunta resurser, köra tester och generera dokumentation. Ett byggsystem säkerställer att programvara kan byggas och distribueras konsekvent över olika miljöer.

**Babel**
En JavaScript-transpiler som gör det möjligt för utvecklare att skriva modern JavaScript (inklusive ES6 och senare) och konvertera det till en bakåtkompatibel version för äldre miljöer. En nyckelfunktion i Babel är möjligheten att tillåta kodning i olika modulsystem, såsom CommonJS, samtidigt som man riktar in sig på miljöer som använder ES6-moduler.

**Linting**
Processen att analysera källkod för att upptäcka och åtgärda potentiella fel, buggar, stilistiska problem och brott mot kodningsstandarder. En linter är verktyget som utför analysen. Genom att fånga problem tidigt bidrar linting till att upprätthålla kodkvalitet, konsekvens och läsbarhet i ett projekt.

**Continuous Delivery (CD)**
En mjukvaruutvecklingspraxis där kodändringar automatiskt förbereds för release till produktion. Efter att ha passerat alla automatiserade tester i CI-pipelines distribueras koden till staging eller produktion på ett sätt som säkerställer att den alltid är i ett releasbart tillstånd. CD syftar till att göra driftsättningar förutsägbara och tillförlitliga, och möjliggör frekventa och säkra releaser.

**Compiler**
Ett program som översätter kod skriven i ett högnivåspråk (som C, C++ eller Java) till ett lägre nivåspråk, vanligtvis maskinkod eller bytekod, som kan köras direkt av datorns hårdvara eller runtime-miljö. Huvudmålet är att optimera och producera effektiv körbar kod för målplattformen. En transpiler (som Babel) översätter också kod, men konverterar mellan språk eller versioner på samma abstraktionsnivå (t.ex. ES6 till ES5) snarare än till maskinnivå.

**Edge Computing**
Ett distribuerat beräkningsparadigm som för data- och beräkningsresurser närmare den plats där de behövs, vanligtvis vid nätverkets ”kant”, nära de enheter som genererar data. Detta minskar latens, sparar bandbredd och förbättrar prestanda, särskilt för applikationer som kräver realtidsbearbetning, genom att bearbeta data lokalt i stället för i ett centraliserat moln.

**RESTful (Representational State Transfer)**
En stil för webbservice-arkitektur som följer REST-principerna. RESTful-tjänster är stateless, skalbara och lättunderhållna, och gör det möjligt för system att kommunicera över webben med standardiserade HTTP-metoder som GET, POST, PUT, DELETE osv. RESTful API:er används ofta för att exponera data och funktionalitet i webbtjänster för andra system, såsom frontend-klienter eller andra backend-tjänster.

**DRY (Don't Repeat Yourself)**
Ett utvecklingsprincip som syftar till att minska upprepning av kod, logik eller data i ett system. DRY uppmuntrar till att abstrahera återkommande logik eller data till återanvändbara komponenter, funktioner eller moduler. Detta ger renare, mer underhållbar kod och minskar risken för fel genom att förändringar endast behöver göras på ett ställe.

**API (Application Programming Interface)**
Ett regelverk som gör det möjligt för olika mjukvaruapplikationer att kommunicera med varandra.

**Frontend System**
Avser samlingen av verktyg, bibliotek, ramverk och tekniker som används för att bygga den användarnära delen av en webbapplikation eller webbplats. Systemet ansvarar för allt som användare interagerar med direkt i webbläsaren, inklusive UI, navigering, renderat innehåll och dynamiskt beteende. Ett robust frontend-system säkerställer en responsiv, interaktiv och sömlös användarupplevelse på olika enheter och plattformar.

**Self-Organizing Team**
En grupp individer som självständigt organiserar sitt arbete och sina ansvar utan behov av centraliserad styrning eller mikromanagement. I ett självorganiserande team beslutar medlemmarna gemensamt hur uppgifter fördelas, hur mål uppnås och hur problem löses, genom att utnyttja sina färdigheter och sin expertis. Konceptet är centralt i agila metoder som Scrum och främjar samarbete, ansvarstagande och anpassningsförmåga.

**Test-Driven Deployment (TDD)**
En utvecklingsprocess där utvecklare skriver tester för ny funktionalitet innan den faktiska koden implementeras. TDD-cykeln innebär typiskt att skriva ett fallerande test, skriva minsta möjliga kod för att få testet att passera och därefter refaktorera koden samtidigt som alla tester fortsätter att gå igenom. TDD främjar renare och mer tillförlitlig kod genom att varje funktion är backad av motsvarande test.

**Serverless Computing**
En molnmodellen där molnleverantören automatiskt hanterar infrastrukturen, så att utvecklare kan fokusera enbart på att skriva och driftsätta kod. I en serverless-arkitektur abstraheras serverhantering och kapacitetsplanering bort, och leverantören allokerar resurser dynamiskt vid behov. Utvecklare driftsätter funktioner, små fristående kodbitar som körs som svar på specifika händelser. Populära plattformar är AWS Lambda, Azure Functions och Google Cloud Functions.

**Persistency**
I JavaScript avser persistens förmågan att lagra data så att den finns kvar över olika sessioner, omstarter av applikationen eller systemomstarter. Beständig lagring säkerställer att data inte går förlorad när en användare stänger webbläsaren eller när en server stängs ned, vilket är avgörande för att bevara state, användarinställningar och applikationsdata över tid.

**Microservice**
En arkitekturstil som strukturerar en applikation som en samling löst kopplade, oberoende driftsättbara tjänster. Varje mikrotjänst ansvarar för en specifik funktion, såsom autentisering, betalningshantering eller produktadministration, och kommunicerar med andra tjänster över nätverk, vanligtvis via HTTP/REST, gRPC eller meddelandeköer. Detta står i kontrast till monolitiska arkitekturer där all funktionalitet är tätt integrerad i en enda applikation.

**Twelve Factor App**
En metodik för att bygga moderna, skalbara och lättunderhållna SaaS-applikationer. Den introducerades av utvecklare på Heroku och beskriver tolv principer som täcker olika aspekter av utveckling, från kodbashantering till driftsättning och operativa frågor, med målet att göra applikationer enkla att driftsätta och skala i moln-miljöer.

**Cypress**
Ett modernt end-to-end-testverktyg för webbapplikationer. Det gör det möjligt att skriva tester som körs direkt i webbläsaren, simulerar användarinteraktioner och verifierar att applikationen beter sig som förväntat. Cypress är känt för snabb exekvering, realtids-reload och en inbyggd instrumentpanel med detaljerad insyn i testresultat. Det är särskilt populärt för komplexa JavaScript-appar byggda med ramverk som React, Angular och Vue.js.

**Integration Testing**
En nivå av mjukvarutestning där individuella enheter eller komponenter kombineras och testas som en grupp. Det primära målet är att identifiera problem som uppstår när komponenter interagerar, såsom formatmismatchar, felaktiga gränssnitt eller oväntat beteende vid integration. Denna testning säkerställer att systemets delar fungerar tillsammans som avsett och att deras interaktioner ger korrekta resultat.

**Double Stub (Testing Double)**
En typ av test-double som ersätter ett riktigt objekt eller metod med en förenklad version som ger fördefinierade svar. Till skillnad från mocks eller spies registrerar stubs inte interaktioner; de returnerar helt enkelt hårdkodade värden när de anropas. Stubs är användbara när du vill isolera komponenten under test genom att ta bort beroenden av externa system eller komplexa objekt.

**Jest**
Ett populärt JavaScript-testramverk utvecklat av Facebook, främst för att testa React-applikationer men även lämpligt för andra JavaScript-projekt. Jest erbjuder en kraftfull, flexibel och lättanvänd miljö för att skriva och köra tester. Det inkluderar noll-konfigurationssetup, lättförståelig syntax, inbyggt stöd för mocking samt snapshot-testning. Jest stöder även testning av asynkron kod och har ett rikt uppsättning matchers för assertioner.

**Doubles**
Dummy: Används för att fylla parametrar, används inte faktiskt. Fake: En förenklad fungerande implementation (t.ex. in-memory-databas). Spy: Registrerar metodanrop och parametrar för senare verifiering. Stub: Ger fördefinierade svar, används för isolerad testning. Mock: Verifierar interaktioner med förväntningar, används för att testa beteende.

**Deploy**
Driftsättning är processen att flytta en applikation eller dess komponenter från en miljö till en annan, vanligtvis från utveckling (dev) till test (test), staging (stage) och slutligen produktion (prod). Varje miljö har ett specifikt syfte: dev för aktiv utveckling, test för kvalitetssäkring och automatiserade tester, stage för slutlig verifiering i en miljö som nära speglar produktion och prod där applikationen görs tillgänglig för slutanvändare. Driftsättning kan innebära flera steg, inklusive att bygga applikationen, köra tester och överföra applikationen till målsystem.

**Containerization**
En lättviktig form av virtualisering som innebär att en applikation packas tillsammans med sina beroenden, bibliotek och konfigurationer i en portabel container. Denna container kan köras konsekvent över olika miljöer, från utveckling till produktion, oberoende av underliggande systemskillnader. Containrar är isolerade från varandra och värdsystemet, men delar värdens operativsystems-kärna, vilket gör dem mer resurseffektiva än traditionella virtuella maskiner.

**Environment Variables**
I React är Environment Variables särskilda variabler som används för att konfigurera olika aspekter av applikationen beroende på miljö (utveckling, produktion, test osv.). Dessa variabler kan styra exempelvis API-endpoints, feature-flaggor och andra inställningar som kan variera mellan miljöer. Miljövariabler i React definieras i en .env-fil och är typiskt prefixade med REACT_APP_ för att säkerställa att de känns igen och injiceras i applikationen vid build-tillfället.

**Unit Testing**
En testmetod där individuella enheter eller komponenter testas isolerat från resten av applikationen. Huvudsyftet är att verifiera att varje enhet fungerar korrekt på egen hand. Enhetstester skrivs och körs vanligtvis av utvecklare och är kända för att vara snabba och ge snabb återkoppling på kodens korrekthet under utveckling.

**CommonJS**
Ett modulsystem för JavaScript, främst använt på serversidan med Node.js. Det gör det möjligt att strukturera kod i återanvändbara moduler, vilket underlättar hantering av beroenden och underhåll av stora kodbaser. Moduler i CommonJS laddas synkront med funktionen require och exporterar funktionalitet via module.exports.

**Double Dummy (Testing Double)**
Inom mjukvarutestning är en Dummy en typ av test-double som används som platshållarobjekt som skickas runt men aldrig faktiskt används i testet. Dummies används när en metod kräver ett argument, men det specifika värdet saknar relevans för testets resultat. Huvudsyftet är att uppfylla funktionssignaturen utan att påverka testets utfall.

**End User Testing (also known as User Acceptance Testing or UAT)**
Den sista fasen i testprocessen där faktiska användare testar systemet i en verklig miljö för att säkerställa att det uppfyller deras behov och krav. Denna typ av testning fokuserar på att validera att programvaran fungerar som förväntat ur användarens perspektiv, med fokus på både funktionalitet och användbarhet innan produkten släpps till produktion.

**React Testing Library**
Ett lättviktsverktyg som tillhandahåller hjälpmedel för att testa React-komponenter. Till skillnad från traditionella testverktyg fokuserar React Testing Library på att testa komponenter ur slutanvändarens perspektiv, vilket gör testerna mer tillförlitliga och underhållbara genom att simulera användarinteraktioner och verifiera komponentens beteende som i en verklig miljö. Används ofta tillsammans med test-ramverk som Jest.

**Double Fake (Testing Double)**
En typ av test-double som ger en fungerande men förenklad implementation av en komponent eller tjänst. Till skillnad från dummies eller stubs, som inte utför verklig logik, efterliknar en fake beteendet hos ett riktigt objekt men med lägre komplexitet, vilket gör den lämplig för teständamål. Fakes används ofta när det riktiga objektet är för resurskrävande eller komplext för testmiljön, till exempel en databas eller extern API.

**Double Spy (Testing Double)**
En Spy är en typ av test-double som omsluter ett riktigt objekt eller en funktion och registrerar hur det används under testet, såsom metodanrop och skickade argument. Till skillnad från mocks eller stubs ersätter en spy inte originalfunktionaliteten; den övervakar och loggar interaktioner utan att ändra beteendet. Spies är användbara för att verifiera att vissa metoder anropades, hur många gånger och med vilka parametrar, samtidigt som den ursprungliga logiken körs.

**Client-Side Scripting**
Avser körning av skript, vanligtvis skrivna i språk som JavaScript, i användarens webbläsare snarare än på servern. Detta möjliggör dynamiska, interaktiva webbsidor som svarar på användarinmatning utan att sidan behöver laddas om. Vanliga uppgifter för klient-side-skript inkluderar formulärvalidering, DOM-manipulation och asynkrona serveranrop (AJAX).

**Hot Module Replacement (HMR)**
En funktion i moderna utvecklingsverktyg som gör det möjligt att uppdatera moduler i en applikation i webbläsaren utan full omladdning av sidan. Detta är särskilt användbart under utveckling då det möjliggör snabbare iteration genom att direkt tillämpa kodändringar samtidigt som aktuellt tillstånd bevaras.

**Require**
En funktion i Node.js, som del av CommonJS-modulsystemet, för att synkront ladda och använda moduler. Den gör det möjligt att importera funktionalitet från andra filer eller moduler till den aktuella filen. Till skillnad från ES6 import kan require anropas villkorligt och när som helst i koden, vilket gör den flexibel men synkron till sin natur. require används främst i Node.js-miljöer för att ladda CommonJS-moduler.

**Node**
Node.js är en öppen källkod, plattformsoberoende JavaScript-runtime som gör det möjligt att exekvera JavaScript på serversidan. Byggd på Chromes V8-motor är Node.js utformad för skalbara, högpresterande applikationer, särskilt sådana som kräver realtidsinteraktion, såsom webbservrar, API:er och strömningstjänster. Node.js använder en händelsedriven, icke-blockerande I/O-modell som gör den effektiv för applikationer med många samtidiga anslutningar.

**Express**
Express.js är ett minimalistiskt och flexibelt webbapplikationsramverk för Node.js. Det tillhandahåller robusta funktioner för att bygga webb- och mobilapplikationer, inklusive verktyg för routing, hantering av middleware samt HTTP-förfrågningar och svar. Express förenklar skapandet av server-side-applikationer så att utvecklare kan fokusera på affärslogik i stället för underliggande infrastruktur.

**Server-Side Scripting**
Processen att skriva kod som körs på en server i stället för i klienten (webbläsaren). Denna skriptning ansvarar för att generera dynamiskt webbinnehåll, interagera med databaser, hantera användarförfrågningar och sköta applikationslogik innan det slutliga resultatet skickas till klientens webbläsare. Vanliga serverspråk inkluderar PHP, Node.js (JavaScript), Python, Ruby och Java.

**Import (ES6 Modules)**
En sats i JavaScript som används för att hämta moduler och deras exporter från andra filer till den aktuella filen. Den är en del av ES6-modulsystemet, som är utformat för modulär programmering och återanvändbar kod. Till skillnad från require är import statiskt analyserad, vilket innebär att den hanteras innan resten av koden körs. import stödjer både namngivna och default-importer, och dynamiska importer är möjliga med import().

**ECMAScript 6 (ES6)**
ES6, även känd som ECMAScript 2015, är den sjätte utgåvan av ECMAScript-språkspecifikationen och introducerade betydande uppdateringar i JavaScript. ES6 lade till nya funktioner och syntax som förbättrade språkets kraft, läsbarhet och användbarhet, särskilt för att bygga komplexa applikationer. Browser support: Moderna webbläsare har i stor utsträckning antagit ES6-funktioner, men äldre webbläsare kan kräva transpilation (t.ex. med Babel) till ES5 för kompatibilitet.

**Prod Environment**
Produktionsmiljön (Prod) är den live-miljö där den slutliga versionen av en applikation driftsätts och görs tillgänglig för slutanvändare. Den är den mest kritiska miljön i livscykeln eftersom den betjänar riktiga användare och hanterar faktisk data. Produktion är optimerad för prestanda, tillförlitlighet och säkerhet, så att applikationen fungerar smidigt under verkliga förhållanden.

**Dev environment (Development Environment)**
Den miljö där utvecklare skriver, testar och felsöker sin kod. Den är typiskt isolerad från produktion och andra miljöer, så att förändringar kan göras utan att påverka slutanvändare. Dev-miljön är konfigurerad för att efterlikna förhållandena där koden slutligen ska köras, men är ofta mindre restriktiv och kan innehålla verktyg för debugging, detaljerade loggar och hot-reloading som gör utvecklingen snabbare.

**Deployment Pipeline**
En serie automatiserade steg som programvara går igenom på väg från utveckling till produktion. Pipen inkluderar vanligtvis bygg av applikationen, körning av enhets- och integrationstester, driftsättning till staging för vidare testning och slutligen driftsättning till produktion. Varje steg säkerställer att koden är grundligt testad och verifierad, vilket minskar risken att fel når produktion. Pipelines är centrala i CI/CD-praxis och möjliggör snabbare och mer tillförlitliga releaser.

**Docker**
En plattform för att utveckla, leverera och köra applikationer i lättviktiga, portabla containrar. Dessa containrar paketerar applikationskoden tillsammans med beroenden, bibliotek och konfigurationer, vilket säkerställer att applikationen körs konsekvent i olika miljöer—utvecklardatorer, on-prem-servrar eller moln. Docker förenklar driftsättning och undviker ”det funkar på min maskin”-problemet.

**Merge Conflict**
Uppstår när Git inte kan lösa skillnader mellan två grenar automatiskt vid en merge. Detta händer vanligtvis när ändringar gjorts i samma del av en fil i olika grenar och Git inte kan avgöra vilken ändring som ska prioriteras. Konflikter måste lösas manuellt innan mergningen kan slutföras.

**Environment**
Inom mjukvaruutveckling avser en Environment en särskild uppsättning hårdvara, mjukvara och konfigurationer där specifika steg i mjukvarans livscykel genomförs, såsom utveckling, test eller produktion. Olika miljöer används för att isolera och hantera förändringar i applikationen i olika skeden, och för att säkerställa korrekt beteende innan release.

**CommonJS**
Ett modulsystem för JavaScript, som främst används i server-side-utveckling med Node.js. Det gör det möjligt för utvecklare att strukturera sin kod i återanvändbara moduler, vilket underlättar hantering av beroenden och underhåll av stora kodbaser. Moduler i CommonJS laddas synkront med funktionen require och exporterar sin funktionalitet med module.exports.

**Separation Of Concerns (SoC)**
En designprincip inom programvaruteknik som förespråkar att ett program delas upp i tydliga sektioner, där varje sektion ansvarar för en specifik del av programmets funktionalitet. Genom att separera ansvar kan utvecklare hantera komplexitet mer effektivt, förbättra modularitet och öka underhållbarheten. Varje sektion, eller ”concern”, bör kapsla in en särskild funktionalitet, såsom användargränssnitt, affärslogik eller dataåtkomst, och interagera med andra sektioner genom väldefinierade gränssnitt.
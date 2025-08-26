# **Repetition**

1. **Nämn ett par npm kommandon kopplat till apphälsa/säkerhet och vad dem gör.**

npm outdated \- kontrollerar om dependencies har nya versioner tillgängliga

npm doctor \- hjälper att hitta vanliga fel såsom npm installationen, typ miljö/konfiguration relaterade problem också

npm audit \- analyserar projektets package-lock.json för sårbarheter

npm audit fix \- försöker åtgärda sårbarheter identifierade enligt ovan, man kan även lägga på flaggan \--force (kan innehålla breaking changes)

npm i \--ignore-scripts (flaggan kommer att säga åt dem dependencies du vill installera att INTE köra något tillhörande script som exempelvis skapar en konfigurationsfil, den/dem får du då skapa själv)

https://www.npmjs.com/package/npm-check  
https://www.npmjs.com/package/npm-check-updates

dessa paket kan du installera globalt på din dator, vilket gör att den inte är projektspecifik, exempelvis:

npm i \-g npm-check (titta i dokumentationen, nu får du ett kommando eller flera sådana du kan använda dig av, oavsett vart du öppnar din terminal/bash)

2.  **Nämn ett par best practices när det kommer till loggning på klientsidan.**

Undvik att logga känslig information (lösenord, JWT, userinfo, paymentinfo)

Vi kan använda en .env fil (read-only, körs i runtime minnet) som kan hålla statisk info typ API-nycklar, men dessa är fortfarande exponerade på klienten

Det finns även möjlighet att använda sig av conditional logging, likt vi har gått igenom under kursens gång med conditional rendering, så kan man titta på NODE\_ENV variabeln eller liknande (för development/production) så att förslagsvis produktion inte har några synliga klientloggar.

Lämpliga loggnivåer \- debug, warn, info, error, log \- enklare att filtrera loggar baserat på allvarligshetsgrad i främst felsökning.  
trött på att skriva specifika loggar för varje komponent? fixa en middleware/helper (se min föreläsning) som sätter upp loggformatet en gång och därefter kallar ni på den funktionen.

Logghanteringstjänster \- verktyg som ElasticSearch, Logstack, Kibana, LogRocket, New Relic, Sentry

3. **Vad är monitorering och varför är det en nyttig åtgärd att ta?**

Det finns olika verktyg för att monitorera, exempelvis Sentry (verktyg för att övervaka kodfel / stacktracing) 

Man kan övervaka användaren och se vilket specifikt fel dem har stött på, där förutsättningarna är helt unika baserat på vem som stött på dem (webbläsare, OS, specifikt användningsfall beroende på hur komplex applikationen är)

Om vi inte ser felet så kan den loggas och skickas upp till tjänsten istället för att vi utvecklare eller testresurs ska regressionstesta och hålla koll på applikationen.

regressionstesta \= testa det som redan finns i din applikation

Fler exempel: Prometheus, Application Insights (Azure), Redis 

4.  **Hur fungerar debouncing och varför ska man använda det? Inkludera ett kodexempel.**

Debouncing är en funktion där man medvetet lägger in en fördröjning för något som kommer kommunicera med servern (t.ex. via ett fetch-anrop) \- till exempel ett REST API \- och klienten är designad för att ta emot input utan en tydlig sökknapp, där varje tangenttryckning annars skulle utlösa ett API-anrop.

Det är ganska vanligt att man lägger in en rimlig fördröjning, ofta 300–500 millisekunder, som inte ökar för varje tangenttryckning \- utan istället återställs. På så sätt väntar funktionen tills du gör en paus i skrivandet, och först då skickas sökningen iväg.

Varför använda debouncing?

- Minskar onödiga API-anrop  
- Bättre prestanda  
- Minskar belastning på både klient och server  
- Förhindrar "flimrande" UI vid snabba uppdateringar

https://www.npmjs.com/package/use-debounce

npm i use-debounce   
const \[debouncedQuery\] \= useDebounce(query, 500\)  
const response \= await fetch(\`https://www.themealdb.com/api/json/v1/1/search.php?s=${debouncedQuery}\`)  
const data \= await res.json()  
// TODO: update useState with data

# **Netlify**

Netlify är en populär plattform för att publicera och hantera webbplatser, särskilt statiska hemsidor som byggs med moderna ramverk som React, Vite, Vue eller liknande. 

Den används ofta i samband med GitHub, eftersom Netlify kan kopplas direkt till ett Git-repo och automatiskt hämta och publicera nya versioner av din webbplats varje gång man pushar kod.

När man har kopplat ett repo till Netlify väljer man vilket build-kommando som ska köras (till exempel npm run build), och vilken mapp som ska användas för att visa den färdiga sajten (till exempel dist eller build). Resten sköts automatiskt av Netlify (bygger projektet och publicerar det direkt online).

En av de stora fördelarna är att det finns inbyggd CI/CD (Continuous Integration/Deployment), vilket innebär att varje ändring man gör i koden automatiskt leder till den nya versionen av webbplatsen \- utan att man behöver ladda upp något manuellt.

---

# **Känslig Data**

För att skydda känslig information i en React-applikation är det viktigt att använda någon form av kryptering \- och ett vanligt verktyg för detta är bcryptjs. Det hjälper till att säkra exempelvis användarlösenord så att de inte lagras i klartext och inte kan läsas av någon som får tillgång till databasen eller nätverkstrafiken.

I dagens digitala samhälle är kryptering avgörande för att bevara användarnas integritet och förhindra att deras uppgifter hamnar i fel händer. Genom att kryptera saker som lösenord, personliga uppgifter eller betalningsinformation minskar man risken för intrång, identitetsstölder och läckor.

# **bcrypt**

bcrypt är ett kraftfullt bibliotek för JavaScript som implementerar den beprövade bcrypt-algoritmen. Det används främst för att säkert hasha lösenord, men kan också appliceras på annan känslig data. 

En viktig del av säkerheten är att bcryptjs lägger till ett unikt "salt" varje gång ett lösenord hashas, vilket gör det mycket svårt för angripare att gissa sig till lösenord även om de ser hashen.

I en React-applikation används bcryptjs framför allt när användare registrerar sig eller loggar in. Lösenordet kan då hashas direkt i klienten innan det skickas till servern, eller så sker det på serversidan med Node.js. 

Det går även att använda bcryptjs för att hantera och skydda annan känslig data, beroende på behovet i applikationen.

För att använda det behöver man först installera biblioteket med kommandot:

**npm install bcryptjs**
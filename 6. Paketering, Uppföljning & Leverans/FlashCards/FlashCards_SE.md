# Flashcards (Förenklad version, översatt till svenska)

---

## Utvecklingsprocess & Metodik

* **CI (Continuous Integration):** Ofta slå ihop kod till gemensamt repo. Byggs och testas automatiskt för att hitta fel tidigt.  
* **Continuous Monitoring:** Övervakning i realtid av prestanda, säkerhet och tillgänglighet. Mätvärden: uptime, svarstid, fel.  
* **Self-Organizing Team:** Team som organiserar sitt arbete själv utan central styrning, vanligt i agila metoder.  
* **DRY (Don't Repeat Yourself):** Princip att undvika duplicerad kod genom återanvändning.  
* **Test-Driven Deployment (TDD):** Skriva tester innan kod, se att testet misslyckas, sedan koda tills det fungerar.  
* **Deployment Pipeline:** Automatiserade steg från utveckling till produktion (bygga, testa, staging, release).  
* **End User Testing (UAT):** Slutanvändare testar om systemet fungerar som de behöver innan release.  

---

## Arkitektur & Systemdesign

* **Microservice:** Applikation uppdelad i små, fristående tjänster som kan utvecklas och driftsättas separat.  
* **Twelve Factor App:** Metod med 12 principer för att bygga molnbaserade och skalbara applikationer.  
* **Multi-Tier Architecture:** System uppdelat i lager (t.ex. presentation, logik, data) för bättre struktur.  
* **Serverless Computing:** Kod körs i molnet utan att hantera servrar, resurser allokeras vid behov.  
* **Frontend System:** Tekniker för det användaren ser i webbläsaren, ex. UI, navigation, rendering.  
* **Environment (Dev/Prod):** Separata miljöer för utveckling, test och produktion.  

---

## Programmering & Kodning

* **Interpreter:** Kör kod rad för rad utan kompilering. Långsammare men enklare att debugga.  
* **API:** Regler för att olika system ska kunna kommunicera.  
* **Client-Side Scripting:** Kod (t.ex. JavaScript) som körs i webbläsaren för dynamik.  
* **Server-Side Scripting:** Kod som körs på servern för att generera svar till klienten.  
* **Persistency:** Att lagra data så den finns kvar över sessioner (cookies, databaser).  
* **ECMAScript 6 (ES6):** Nyare version av JavaScript med modernare syntax (import/export, let/const, arrow functions).  
* **CommonJS:** Äldre modulsystem i Node.js, använder `require` och `module.exports`.  
* **Import/Require:** Sätt att ladda in moduler i JavaScript.  
* **Node.js:** Kör JavaScript på serversidan. Byggt på V8-motorn, bra för realtidsappar.  
* **Express.js:** Minimal ramverk för att bygga webbservrar i Node.  
* **Hot Module Replacement (HMR):** Uppdaterar kod i realtid under utveckling utan att ladda om sidan.  

---

## Testning

* **Unit Testing:** Testar små delar av kod (funktioner/komponenter) isolerat.  
* **Integration Testing:** Testar att flera komponenter fungerar ihop.  
* **Component Testing:** Testar enskilda UI-komponenter i isolation.  
* **React Testing Library:** Testar React-komponenter från användarens perspektiv.  
* **Cypress:** Ramverk för end-to-end tester i webbläsaren.  
* **Jest:** Populärt testramverk för JavaScript/React.  
* **Test Doubles (Dummy, Fake, Stub, Mock, Spy):** Förenklade versioner av objekt/funktioner för att testa isolerat.  
  * **Dummy:** Endast en platshållare, används inte.  
  * **Fake:** Förenklad men fungerande version, ex. minnesdatabas.  
  * **Stub:** Returnerar fördefinierade värden, testar isolering.  
  * **Mock:** Kontrollerar att metoder anropas korrekt.  
  * **Spy:** Loggar anrop men låter riktig funktion köras.  

---

## Deployment & Infrastruktur

* **Dependency Management:** Hantering av externa bibliotek i projekt (npm, Yarn).  
* **Containerization:** Köra applikation i isolerade containers för portabilitet.  
* **Docker:** Plattform för att köra containers.  
* **Environment Variables:** Inställningar (API-nycklar, endpoints) beroende på miljö.  
* **Deploy:** Flytta kod mellan miljöer (dev → test → prod).  
* **Merge Conflict:** När Git inte kan avgöra vilka ändringar som ska behållas vid merge.  

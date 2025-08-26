1. **Vad är CAPTCHA, rättare sagt reCAPTCHA? Varför behövs det och hur gör man? Inkludera kodexempel**  
     
   CAPTCHA står för “Completely Automated Public Turing Test To Tell Computers And Humans Apart”. reCAPTCHA är ett sätt att motarbeta bottar/spam. Det är också ett sätt att motverka brute-force attacker (exempelvis mot ett inloggningsformulär för att testa användarnamn/lösenord flertalet ggr inom ett kort intervall)  
     
2. **Varför bör man sanitera innehållet man sätter via dangerouslySetInnerHTML? Hur gör man? Inkludera kodexempel**  
     
   Att använda detta attribut/funktionalitet kringgår Reacts inbyggda säkerhetsprinciper gällande att ta användarinput och parsa det som en sträng (detta försöker parsa det som HTML). 

   Att parsa ut HTMLen i DOMen så kan din applikation  bli utsatt för risk då det kan potentiellt innehålla skadliga script-taggar eller onödiga attribut/funktionalitet som påverkar sidans design.   
     
3. **Vad är CSP för något, och hur går man tillväga för att sätta upp en sådan? Inkludera exempel**  
     
   CSP står för Content-Security-Policy och den sätter upp begränsningar på vad för resurser (JavaScript, bilder, typsnitt, API-anrop) får köras / laddas på sidan.  
     
   Istället för att tillåta “vad som helst” så säger du exakt vad som får köras, exempelvis då via en meta-tagg i HTMLen.  
     
4. **Hur fungerar useEffecten hooken och vad är dess syfte? Inkludera kodexempel**

	useEffect är en hook som tar in: 

- funktion  
- cleanup (när komponenten “dör” \- rensa eventhandlers eller globala setTimeouts / setIntervals här)   
- dependency array (som avgör när den körs)  
    
  Dependency arrayen har ett viktigt syfte \- och kan tendera att vara lite “dold” men viktigt att man tänker på.   
    
  useEffect syfte? Hantera sidoeffekter i ens komponent. Du styr alltså, i funktionella komponenter, när saker ska ske i ens komponents livscykel. Det ser annorlunda ut i klasskomponenter, men när det år 2025 och vi kör inte sådana längre. 




**NPM-säkerhet**

**Vad är NPM?**

NPM är ett verktyg som används för att ladda ner, installera och dela JavaScript-paket.  
 I stället för att kopiera kod mellan projekt kan man skapa egna bibliotek och publicera dessa som i sin tur kan installeras av andra med npm install.

**Risker**

Om man glömmer att ignorera känsliga filer (som .env) när man publicerar paket, kan de råkas publiceras av misstag.

**Att komma ihåg**

- .npmignore bestämmer vad som inte ska följa med när paketet publiceras.  
- Om både .gitignore och .npmignore finns används bara .npmignore och det kan bli förvirrande.

Det är bra att alltid dubbelkolla att man inte råkar ladda upp privata filer.

När man installerar paket skapas en lockfil (package-lock.json eller yarn.lock),  
som ser till att exakt samma versioner används varje gång. Detta är väldigt viktigt inom produktion.

**Automatiska script**

Vissa paket kör automatiskt skript när de installeras \- det kan vara praktiskt, men också farligt.

Ondsinta paket kan utnyttja detta för att köra skadlig kod.   
För att undvika detta kan man köra:

npm install \<paket\> \--ignore-scripts

En långvarig lösning är att lägga till det i .npmrc

**Fler tips:** 

- npm outdated visar vilka paket som är gamla och kan uppdateras.  
- npm doctor kontrollerar att din npm-miljö är frisk.  
- npm audit (Den kollar igenom dina beroenden och varnar för kända sårbarheter)

**Typosquatting** är en attack där någon laddar upp ett paket med ett namn som nästan ser ut som ett populärt paket (t.ex. react-domm istället för react-dom).

Detta kan vara lätt att missa så det är viktigt att kolla noga. 

**Logging & Monitoring**

Att bara använda console.log() funkar ofta bra för att felsöka när man utvecklar. Men det finns bättre sätt att logga, särskilt om man vill ha ordning på vad som händer i appen längre fram.

**Tips**

- Använd olika nivåer, t.ex. info, warn, error, debug. Då vet man hur allvarligt det är direkt.  
- Lägg till sammanhang – vad hände, var, och kanske vilken användare? Det gör det lättare att förstå loggen.  
- Ha ett konsekvent format – t.ex. med en hjälpfunktion som loggar på samma sätt varje gång.  
- Skicka loggar till molnet – då kan man felsöka även efteråt, t.ex. om något kraschat i produktion.

**Conditional logging** (logga bara vissa saker vid behov, t.ex. bara i utvecklingsläge)

**Monitoring**

Monitoring handlar om att övervaka appen löpande och upptäcka problem så tidigt som möjligt. Det räcker inte att bara logga lokalt, man behöver samla in data på ett ställe där man kan se mönster och fel.

Det finns flera riktigt bra verktyg för att övervaka fel, prestanda och användarbeteenden.

- **Sentry** (spårar JavaScript-fel i frontend)  
- **New Relic** (övervakar prestanda och laddtider)  
- **Rollbar** (upptäcker fel och skickar notiser)  
- **TrackJS**  (fångar problem i webbläsaren)